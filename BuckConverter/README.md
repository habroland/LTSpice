Simulation of buck converter based on these [notes](http://web.stanford.edu/class/ee152/resources/ee152_notes.pdf). Note that this particular converter switches to "ground" instead of a "high-impedance" in the OFF state. In this way, the current through the inductor can be continuous even with an ideal switch.


<p align="center">
<img src="Buck.png" width="1000" />
</p>

In the figure you see the steady state operation of the buck converter. The current oscillates around 0 and the voltage around 22.5 V for an input of Vcc=50 V and a duty cycle of D=1/2. Note that this simulation differs from the ideal calculations:

* The steady state voltage is lower than the expected Vcc * D
* The voltage and the current are dephased, instead of in-phase

You will have to download the files and set the correct path for the buck file to find the switch.
If you want to make it on your own:
The simulation contains a homemade SPDT switch which I made following [these instructions](https://forum.digikey.com/t/making-switches-in-ltspice-circuit-configurations/3285).
Note that the voltage-controlled switch "SW" component in LTSpice needs to be configured with a script to let the run know what are the switching parameters. You will  have to do [this](https://www.analog.com/en/technical-articles/ltspiceiv-voltage-controlled-switches.html)
I made a symbol for this switch as told in the instrucions. You can learn how to make a symbol [in this video](https://www.analog.com/en/education/education-library/videos/5579253506001.html)

I used [IrFanView](https://www.irfanview.com/) to take the screenshot with the cursor
