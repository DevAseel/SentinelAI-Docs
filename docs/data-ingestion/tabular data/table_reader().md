---
sidebar_position: 7
---

# table_reader()

`table_reader()` class is used to read the content of a table by passing the JSON file which contains the details of the cells. The method utilizes EasyOCR for Optical Character Recognition (OCR) and returns the parsed content of the table.


<img src="https://sentinel-ai-docs.vercel.app/img/table_reader.png" />

## Usage

- Find the execution file at `./table_reader.py` and run the following command:

```bash
    python table_reader.py --img-path <path-to-your-image> --json-path <path-to-json-file>
```

- To specify languages for OCR, you can provide an array of languages. Example:

```bash
    python table_reader.py --img-path <path-to-your-image> --json-path <path-to-json-file> --languages en ar

```

- To output the results as a json file, you can use the following command:

```bash
    python table_reader.py --img-path <path-to-your-image> --json-path <path-to-json-file> --json true
```

- To specify an output path for the json file, you can use the following command:

```bash
    python table_reader.py --img-path <path-to-your-image> --json-path <path-to-json-file> --json true --output-path <path-to-json-output-directory>
```


| Parameter      | Description                                                                     | Type    | Required | Default                        | Options                                         |
|----------------|---------------------------------------------------------------------------------|---------|----------|--------------------------------|-------------------------------------------------|
| \--img-path    | the relative path of the image                                                  | string  | ✓        | \_                             | \_                                              |
| \--json-path   | the relative path of the JSON file containing the cells result                  | string  | ✓        | \_                             | \_                                              |
| \--languages   | an array of languages that has to be supported to read the document             | list    | ✗        | `['en']`                       | \_                                              |
| \--json        | set true to save output as a json file                                          | boolean | ✗        | `false`                        | `true`, `false`                                 |
| \--output-path | specify the output path of the json file                                        | string  | ✗        | `./outputs/parsed_tables_json` | \_                                              |
| \--log-level   | the level of the log messages you would like to display when executing the file | string  | ✗        | `info`                         | `debug`, `info`, `warning`, `error`, `critical` |
