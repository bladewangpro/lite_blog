---
name: Turn off Turbo Boost on Ubuntu
use_math: false
heading1: Turn off Turbo Boost on Ubuntu
motivation: Someday it will all make sense.
about: SHELL
--- 

Turn off Turbo Boost on Ubuntu

## How to turn off Turbo Boost on Ubuntu

1. If your system is using the intel\_pstate frequency scaling driver:
```shell
$ cat /sys/devices/system/cpu/cpu*/cpufreq/scaling_driver
intel_pstate
intel_pstate
intel_pstate
intel_pstate
intel_pstate
intel_pstate
intel_pstate
intel_pstate
```

2. Then you can inquire as to the turbo enabled or disabled status:
   Where 0 means turbo is enabled and 1 means it is disabled. And you can change it by writting (as sudo) to the same location.
```shell
cat /sys/devices/system/cpu/intel_pstate/no_turbo
sudo su
echo "1" > /sys/devices/system/cpu/intel_pstate/no_turbo
exit
``` 

3. We can add this startup option into the system list with chrontab
	* chrontab
		We can let one machine running on a specific time
		```shell
		sudo su
		chrontab -e # -r means remove current task list, -l means check all the chrontab tasks list
		# create a new script file under /opt/ folder, cuz /opt/ and /user/local, both of them are really safe to use, wont cause the system crash
		mkdir -p /opt/blade_src/
		echo "echo \"1\" > /sys/devices/system/cpu/intel_pstate/no_turbo"
		# add the following line into that file, then reserve the content and exit root account
		@reboot bash /opt/blade_src/shutdown_boost.sh
		# ---------------
		mins hours dates month "everyday of the week (from 0~6, 0 means Sunday)"
		# such as every Thursday 2 am, execute /opt/shutdown_boost.sh
		00 02 * * 1 bash /opt/blade_src/shutdown_boost.sh
		```
