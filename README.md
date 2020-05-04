# Machine learning notebook

Machine learning notebook.



## How To Use

Install dependencies:

```bash
virtualenv --system-site-packages -p python3 ./venv
source ./venv/bin/activate
python -m pip install -r requirements.txt
```

Download datasets

```bash
## Auto-mpg
kaggle datasets download -d 'uciml/autompg-dataset' \
    && SOURCE='autompg-dataset.zip' \
    && DIST='data/auto-mpg' \
    && mkdir -p "${DIST}" \
    && unzip -d "${DIST}" "${SOURCE}" \
    && rm "${SOURCE}"

## Fasion MNIST
kaggle datasets download -d 'zalando-research/fashionmnist' \
    && SOURCE='fashionmnist.zip' \
    && DIST='data/fashion-mnist' \
    && mkdir -p "${DIST}" \
    && unzip -d "${DIST}" "${SOURCE}" \
    && rm "${SOURCE}"

## Shakespeare Dataset
DIST='data/shakespeare' \
    && SOURCE='https://homl.info/shakespeare' \
    && mkdir -p "${DIST}" \
    && curl -fsSL -o "${DIST}/data.txt" "${SOURCE}"
```

Run the notebook:

```
source ./venv/bin/activate
jupyter notebook
```

Open 'http://localhost:8888' in a browser.



## License

The source code is provided under the terms of [the MIT license][license].

[license]:http://www.opensource.org/licenses/MIT
