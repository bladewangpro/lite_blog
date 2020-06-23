---
name: Project Short-term Summary
use_math: true
heading1: Project Short-term Summary
motivation: Someday it will all make sense.
about: TF
--- 

Project Short-term Summary

## Smart Drill Machine


### Why

Drilling holes on CFRP board is a hard process. We are unable to make sure the quality of each holes.
Then our first step is find the characteristics of the bad holes then we can predict the quality of 
current hole depending on the whole force curves and roughness curve. 

### Targets

Find the <u>bad</u> holes from a bunch of holes
build relationship between two force curves and roughness coefficients such as $R_a$, $R_v$ and $R_z$

### Type of Problems

classification problem, let machine can recognize the bad holes from the thrust curve and torque curve

> We didn't use the **roughness** curve yet. Till now, for roughness, just roughness coefficients have been
used in our experiment.

### What do we have now

1. roughness data   
  * qc: 0, 45, 90, -45, -90
  * vc: 0, 90, -45, -90
  * original: roughness coefficients, roughness curve
  * computed: average roughness data

2. force data
  * qc and vc
  * original: torque curve and force curve
  * computed: 5 segments of thrust force curve and torque --> (stage1 and stage2 are the most important parts)

3. qc thrust force adjustment
  * $[21~40]$    Thrust force * 1.6
  * $[41~80]$    Thrust force * 1.9
  * After that, the average thrust force should be an increasing straight line.

4. the information of driller on making qc holes process
  * the speed of drill bits: 7.62mm/s
  * the depth of holes: 7.6mm


### The process

* extract the data of time, force and torque from the orignal xls files, then reserve in csv file which is under "original" folders
* stage the whole force-time curve with two different methods. (manually and rdp)
* update the qc thrust force curve with the information provided by Dave Kim

#### For the thrust force part (stage 2):
![](/images/smart_drill/stage_rdp.png)
![](/images/smart_drill/stage_manually.png)

#### For the torque part:
![](/images/smart_drill/stage_rdp_torque.png)
![](/images/smart_drill/stage_manually_torque.png)

**Obviously, the update operation fits thrust force really well, but doesn't fit with the torque curve.**

* apply fft on all the holes

#### FFT

	* chop the curve of stage 2
	* fix the length of fft
	* 

##### inside fft logic
		* get the first 720 data points from stage 2 of each drill holes
		* set the size of output of fft as 256*2
		* chop the first 6 point out
		* normalize the whole output result fft --> fft_data = fft_data[6:256]/fft_data[6:256].sum()
		* set the window size of np.fft.fftfreq as 256*2, and sample rate as 1/1024
		* output fft_data[6:256] as rows and fftfreq[6:256] as columns into dataframe