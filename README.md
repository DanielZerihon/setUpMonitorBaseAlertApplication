# Monitor Program

This repository contains scripts and configurations to set up a monitoring system using a Python Flask application, Prometheus, Prometheus alert manager, Telegraf, and Ansible.
the user need to only run the 'program/execudeProgram.sh' and it will do the rest. 

- `program/`: Contains Python script `alertCapture.py`, Bash script `execudeProgram.sh` and folder `numOfSessionOnEachNode` that will conatin a txt file with the lines:
	a numberOfSession: X. 
	b status: Y.
- `prometheusFiles/`: Placeholder for Prometheus configuration files.
- `telegrafPlugins/`: Placeholder for Telegraf plugin files.
- `Ansible`: README for ansible located at: Ansible/addServerToMonitorStack.

## Scripts

### program/execudeProgram.sh

Main Script,This Bash script provides instructions and prompts the user to input the VM name and PEM file name. It then checks SSH connection, updates the hosts file, and executes the Ansible playbook.

### program/alertCapture.py

This Python script sets up a Flask application to capture alerts, parse JSON data, and update files based on received alerts.

### telegrafPlugins/vm_metrics.py

This Python script collects various system metrics such as CPU usage, RAM usage, RAM available, and the number of active sessions.
