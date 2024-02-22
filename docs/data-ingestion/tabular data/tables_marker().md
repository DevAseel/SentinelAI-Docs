---
sidebar_position: 4
---

# tables_marker()

`tables_marker()` method is used to mark the scanned tables within the document by highlighting the boundries of the table which are detected from `tables_scanner()` method.

<img src="https://sentinel-ai-docs.vercel.app/img/tables_marker.png" />

## Usage

- Find the execution file at `./tables_marker.py` and run the following command:

```bash
    python tables_marker.py --log-level debug --img-path <path-to-image> --json-path <path-to-json-file> 
```

- To sepcify a custom path to save the marked table, you can simply add an argument of `output_path`:

```bash
    python tables_marker.py --log-level debug --img-path <path-to-image> --json-path <path-to-json-file> --output-path <output-img-path>
```


## Parameters

| Parameter          | Description                                                                     | Type   | Required | Default                   | Options                                         |
|--------------------|---------------------------------------------------------------------------------|--------|----------|---------------------------|-------------------------------------------------|
| --img-path         | the path to the scanned image which contains the table to be marked             | string | &check;  | _                         | _                                               |
| --json-path        | the path to the json file containing the boundry box of the scanned table       | string | &check;  | -                         | _                                               |
| --output-path      | the output path of the marked image                                             | string | &cross;  | `./outputs/marked_tables` | _                                               |
| --log-level        | the level of the log messages you would like to display when executing the file | string | &cross;  | `info`                    | `debug`, `info`, `warning`, `error`, `critical` |
