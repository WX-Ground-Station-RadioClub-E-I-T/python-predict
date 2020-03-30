# Actually a python propagator

Due predict have some errors, I decide to create my own propagator using [orbit_predictor](https://github.com/satellogic/orbit-predictor)

With this propagator there is no overlaping problem. If two passes coincide pass with worst elevation is discard.

This script propagate every sat with valid TLE on `file` parameter.

## Install

Using python3. Consider use a virtualenv.

```
pip install orbit-predictor
```

## Usage

```
python predict.py --location 40.452591 -3.7286226 666 weather.tle
```

## Licence

GNU GPL V3