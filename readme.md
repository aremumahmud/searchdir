# SEARCHDIR CLI Tool

The `searchdir` is a simple command-line utility that allows you to search for a substring in files within a directory and its subdirectories.

## Installation

To install `searchdir` Tool globally, you can use npm:

```bash
npm install -g search_dir_cli
```

## Usage

After installing, you can use `searchdir` Tool from the command line to search for a substring in files within a directory. Here's the basic usage:

```bash
searchdir <folderPath> <substring>
```

Replace `<folderPath>` with the path to the directory you want to search and `<substring>` with the substring you want to search for.

### Options

- `-e, --exclude <folders...>`: Exclude specific folders from the search.

### Example

```bash
searchdir backend "status(200).send" -e node_modules
```

This command will search for the substring "status(200).send" in files within the "backend" directory and exclude the `node_modules` directory in its search.

## Output

The output will display the files containing the specified substring along with the line numbers where the substring was found. For example:

```
Searching: backend\package.json
Files containing the substring:
backend\index.js:
  Line 62:         res.status(200).send('Message stored and broadcasted successfully.');
  Line 82:         res.status(200).send('Message stored and broadcasted successfully.');
```

## Contributing

If you encounter any issues or have suggestions for improvements, feel free to open an issue or submit a pull request on GitHub.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
