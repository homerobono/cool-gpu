# cool-gpu

A script hack for GPU fan control on headless GPU nodes

## How to Use

Check the original [project document](https://github.com/homerobono/cool-gpu/blob/e179cb834b8556228c97d820ed08dce10e3ab5e7/Nvidia%20GPU%20Coolness%20-%20Homepage%20of%20Axel%20Kohlmeyer.pdf) for further details on steps 1 and 2.

0. Generate the dfp-edid.bin file through the NVIDIA Settings panel button 'Acquire EDID'

0. Create a xorg.conf file that fit your setup

0. Put this entire folder wherever you like (e.g.: /opt/set-gpu-fans);

0. Edit 'cool_gpu' file: change the first line to the directory you choosed;

0. Create a link to 'cool_gpu' in the executable files folder (e.g.: ln
/opt/set-gpu-fans/cool_gpu /usr/local/bin/cool_gpu)

0. Run 'cool_gpu' with a number argument to set this speed (40-100), or with 'stop' to return to 
GPU default state, e.g.:

```
    cool_gpu 85         set fans to 85%
    cool_gpu stop       stops the program and return GPU to its default state
    cool_gpu            set fan to a temperature dependent value
```

This was based on [Axel Kohlmayer](https://sites.google.com/site/akohlmey/welcome-to-my-homepage)'s original work taken from his homepage a while ago. The project full description is included on the PDF.
