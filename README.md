This is a temporary repo for first data.

It uses RIDS, so clone the rids repo from HERA_Team (https://github.com/HERA-Team/rids) and `python setup.py install`

To view the spectrum analyzer data, go into the instek sub-directory and use the `rdhandle.py` script from rids.  Use `rdhandle.py -h` to see options.

To look at the entire water-fall of the 12-hour data set use

```rdhandle.py sa_SpectrumPeak.20180526-200103.n33768.None.ridz --wf val```

and use the magnifier to move around.

You can limit the freq and time ranges, e.g.

```rdhandle.py sa_SpectrumPeak.20180526-200103.n33768.None.ridz --wf val -f 100,200 -t1,2```

(the freq[-f] and time[-t] limits are in the units of the full waterfall plot)

You can look at stacked spectra, e.g.

```rdhandle.py sa_SpectrumPeak.20180526-200103.n33768.None.ridz --stack val -f 100,200 -t 1,1.5```

You can look at time streams, e.g.

```rdhandle.py sa_SpectrumPeak.20180526-200103.n33768.None.ridz --stream val -f 70,80```

To look at the the maxhold data, you need to find the keys* - to view the week-long one:

```rdhandle.py A12_SpectrumPeak.20180716-173654.n7.None.ridz --stack maxhold --keys data.20180725-133149.E --legend```

If you want to see the header, use the `specpeak.py` script with `-i`

```specpeak.py A12_SpectrumPeak.20180716-173654.n7.None.ridz -i```

*To see the feature_set keys
```specpeak.py A12_SpectrumPeak.20180716-173654.n7.None.ridz --show_keys```