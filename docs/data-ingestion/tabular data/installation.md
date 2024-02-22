---
sidebar_position: 1
---

# Installation

To install SentinelAI Table Indexer:

- Navigate to the application files:

```bash
    cd ./components/tableIndexer
```
- Create your python environment:

```bash
    python -m venv myenv
```

or if you are using conda:

```bash
    conda create --name myenv
```
- Activate your environment:

on Windows:

```bash
    myenv\Scripts\activate
```

on MacOS & Linux:

```bash
    source myenv/bin/activate
```

for conda:

```bash
    conda activate myenv
```

- Install requirements:

```bash
    pip install -r requirements.txt
```

- The component is utilizing poppler under the hood & it's a dependecy to run the component, you can install the component by doing the following:

on Windows:

```bash
    sudo apt install poppler-utils
```

on MacOS & Linux:

```bash
    brew install poppler
```
