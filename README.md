# innovationday LV 2024 Q1 features

things to install

- JKI dragon  https://dragon.vipm.io/
- LV 2024 Q1
- ni-daqmx driver

about the example VI:

- Create couple of Simulated DAQ devices in MAX(which can output signal on physical channel), I created CDAQ chassis and CDAQ modules
  ![image](https://github.com/ni-sujain/innovationday/assets/98735487/68df53b1-24a7-45e3-8306-f4bfb8b4f5d0)


- Then test https://github.com/ni-sujain/innovationday/blob/main/LabVIEW%20demo/Main.vi.
- Main VI opens two references to ContinuousVoltageAcq.vi, activates the FP and runs call by ref on both the references(example of Open VI ref accepting a VI ref).
- ContinuousVoltageAcq.vi is just a simple DAQ acq task. It configures the channel, clock etc and acquires signals and plots them in a graph. I have add some custom dummy logging in a while loop. The logging library(logo book toolkit) is from VIPM.
- This also has two browse for Path methods(example of invoking browse for pth dialog while running the VI) for selecting log folder paths. By default they are off. Turn on this with given boolen button.
- the .dragon file is an example of package dependency stuff. It will mention the dependency on VIPM package(step_at_lib_logbook_toolkit) as well as NIPM package(ni-daqmx)



