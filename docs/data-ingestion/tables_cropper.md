---
sidebar_position: 3
---

# tables_cropper()

`tables_cropper()` method is used to crop the scanned tables from the PDF image and save the table as a standalone image.

<img src="https://sentinel-ai-docs.vercel.app/img/tables_cropper.png" />

## Usage

- Find the execution file at `./tables_cropper.py` and run the following command:

```bash
    python tables_cropper.py --log-level debug --img-path <path-to-image> --json-path <path-to-json-file> 
```

- To sepcify a custom path to save the cropped table, you can simply add an argument of `output_path`:

```bash
    python tables_marker.py --log-level debug --img-path <path-to-image> --json-path <path-to-json-file> --output-dir <output-img-path>
```

- For advanced usage, you can also specify `tokens`, `class_thresholds`, and `padding` for the cropped table. 


## Parameters

| Parameter          | Description                                                                                                                | Type   | Required | Default                                                        | Options                                         |
|--------------------|----------------------------------------------------------------------------------------------------------------------------|--------|----------|----------------------------------------------------------------|-------------------------------------------------|
| --img-path         | the path to the pdf image which contains the table to be cropped                                                           | string | &check;  | _                                                              | _                                               |
| --json-path        | the path to the json file containing the boundry box of the scanned table                                                  | string | &check;  | _                                                              | _                                               |
| --output-dir       | the output path of the cropped table                                                                                       | string | &cross;  | `./outputs/tables`                                             | _                                               |
| --tokens           | contains a list of words and their bounding boxes in image coordinates.                                                    | string | &cross;  | `[]`                                                           | _                                               |
| --class_thresholds | threshold for each class `table`, `table rotated`, and `no object`. If class is below its threshold, object is ignored.    | string | &cross;  | `{"table": 0.5, "table rotated": 0.5, "no object": 10}`        | _                                               |
| --padding          | the specified padding for cropping the table.                                                                              | string | &cross;  | `10`                                                           | _                                               |
| --log-level        | the level of the log messages you would like to display when executing the file                                            | string | &cross;  | `info`                                                         | `debug`, `info`, `warning`, `error`, `critical` |
