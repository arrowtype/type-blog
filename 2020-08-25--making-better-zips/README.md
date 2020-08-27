# Making better zip files for Windows by excluding unnecessary .DS_Store & MACOSX files

## The Problem

Something unexpected that I learned recently: if you are on a Mac and make a zip of a folder in a regular way (e.g. by right-clicking a folder, then selecting ‘compress’, or with a basic usage of the `zip` command-line utility), it includes obnoxious, unnecessary files for folks that decompress those zips on Windows computers.

1. The top level will have an empty `MACOSX` folder
2. Every other level will have an unnecessary `.DS_Store` file

![top level with empty 'MACOSX' folder](assets/2020-08-25-17-16-16.png)

![Main folder with '.DS_Store' file](assets/2020-08-25-17-16-31.png)

My vague understanding of these files is that they somehow help macOS deal will making backups. However, these aren’t helpful in zipped folders, and if you send these zips to Windows users, they are especially unhelpful.

## A command-line solution

To avoid this, you can compress a folder on the command line. Use `cd` to navigate to its parent directory, then use this command (replacing arrowtype-name_sans-v03 with the appropriate folder name):

```
zip arrowtype-name_sans-v03.zip -r 'arrowtype-name_sans-v03' -x '*/.DS_Store'
```

This command is somewhat unintuitive and may not work as expected if you change or leave out the single quotes. The best way to be sure it worked as you expect is to try opening it in Windows (whether on an actual PC or via a virtual machine using software like VMWare or Parallels). 

One good way to avoid remembering this or worrying about syntax is by automating it with a shell function in your shell profile.

### Automating it with a function

The function below will make a clean zip if you call if with a path, like `zipit path/to/folder`.

```bash
function zipit {
  zip $1.zip -r $1 -x '*/.DS_Store'
  echo "zip made of " $1
}
```

Of course, you have to make sure the terminal has this function in memory for it to work, so you should store this in your `.bash_profile` file (or `.bashrc`, [depending on your approach](https://scriptingosx.com/2017/04/about-bash_profile-and-bashrc-on-macos/)). Then, you can call it from any terminal session.

## The Result

When you exclude the `.DS_Store` files, it avoids both problems, and the result is much cleaner:

![Folder without the '.DS_Store' file](assets/2020-08-25-17-17-17.png)

## An easier solution

I mentioned this article in a [Twitter thread](https://twitter.com/ArrowType/status/1298375103152107520), and several people mentioned the approaches they take to this problem.

A notable easy solution is [Keka](https://apps.apple.com/us/app/keka/id470158793?mt=12), which is a native Mac app which can make clean zips, password-protected zips, and more. So, if you have $2.99 and you want a solution available via right-click or drag-and-drop, this is probably worth it.

Of course, if you are already using a shell script to set up a build, the function may be the simplest & most efficient way to do this. Or, if you are using a Python-based build flow, that also [got a reply](https://twitter.com/mass_driver_tm/status/1298377561869819905?s=20) in the thread.

Happy zipping!