# Actually a python propagator

Due predict have some errors, I decide to create my own propagator using [orbit_predictor](https://github.com/satellogic/orbit-predictor)

With this propagator there is no overlaping problem. If two passes coincide pass with worst elevation is discard.

This script propagate every sat with valid TLE on `file` parameter.

Output is like

```
$ python predict.py --location 40.452591 -3.7286226 666 weather.tle
04:52 03/30/20 1585536768 15 786 NOAA 19
06:32 03/30/20 1585542757 72 947 NOAA 19
07:22 03/30/20 1585545726 53 899 NOAA 15
07:59 03/30/20 1585547967 33 882 METEOR-M 2
08:19 03/30/20 1585549160 14 760 NOAA 18
09:02 03/30/20 1585551743 21 791 NOAA 15
09:39 03/30/20 1585553981 32 864 METEOR-M 2
09:59 03/30/20 1585555145 76 937 NOAA 18
11:40 03/30/20 1585561256 11 683 NOAA 18
```

**TIME DATE TIMESTAMP MAX_ELEVATION DURATION SATELLITE**

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