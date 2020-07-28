# P_INR_OSC_MODE_DA
PRISMA-INR Data analysis for the long oscillogram taking operation mode

PRISMA-INR is a electron-neutron detector (en-detector) array operated in Moscow in the Institute for Nuclear Research Russian Academy of Sciences.
The array consists of 16 en-detectors and uses CAEN FADC DT5740D for data aquisition system.
The data aquisition system can work in 2 different operational modes:
1) The first mode is recording each individual pulse above the threshold of ~ 7 mV measuring variations and searching for the coincidences using the software. Inside the coincidence there are the delayed neutron pulses those are found inside a time gate of 20/10/5 ms using timestamps obtained from the FADC. Time of each digitized pulse is ~ 2 mcs. 
The advantages of that mode:
  - simultaneous variations and EAS recording: solving two independent tasks by one instrument
  - good pulse shape selection important for both tasks
  - excellent background observations
It's disadvantages:
  - the first pulse cannot be recalculated using it's shape in the case of overflow
  - the neutrons situated on the negative tail of the first pulse will have a higher relative threshold for recording than ones found on the 0 base line.
2) The second mode uses coincidences from the FADC and records long 3/6/12 ms oscillograms for each coincidential (EAS) event. Each 5/1 minute special software trigger is started to observe the chance neutron background.
Advantages and disadvantages of that mode are definitely opposite to ones of the first mode.

The current repository includes a code for operational analysis for the data obtained using the second mode.
