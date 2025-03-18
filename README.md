# Rustmarks

Rustmarks is a command-line tool for managing bookmarks and navigating through them.

It is written in Rust and uses SQLite as its database.

![Gif of Rustmarks](https://github.com/Promptorium/rustmarks/blob/main/media/rustmarks.gif)

## Features

- Add, remove, and edit bookmarks
- Search bookmarks
- Navigate through bookmarks using the `bk` command
- Quickly move between bookmarked directories
- Open bookmarked files in the default editor

## Installation

To install Rustmarks, run the following command:
```bash
bash <(curl -s https://raw.githubusercontent.com/Promptorium/rustmarks/main/install.sh)
```
It will download it using apt if you are using a debian based system, otherwise it will download the binary directly and place it in `/usr/local/bin`.

## Usage

After installing Rustmarks, run `rustmarks init` to initialize rustmarks. From now on, you can use the `bk` to interact with your bookmarks.

> This step is optional, but is needed if you want to use the navigation features.

Well done! Now you can use the `bk` command to navigate through your bookmarks. 

### Adding Bookmarks

Rustmarks uses a SQLite database to store bookmarks.
To add a bookmark, use the `add` command:

```bash
bk add /path/to/bookmark <name> <description>
```
or 
```bash
bk add /path/to/bookmark
```

If you don't specify a name, the bookmark will be named after the directory.

### Removing Bookmarks
![Deleting a bookmark](https://github.com/Promptorium/rustmarks/blob/main/media/delete.gif)

You can remove a bookmark from the UI by selecting it and pressing `Ctrl+D`. This will open a prompt asking you to confirm the deletion.


You can also use the `delete` command:
```bash
bk delete <path>
```

