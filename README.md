# Original Project
Based on the project: https://github.com/swar/Swar-Chia-Plot-Manager

Thank you **SWAR** for your hard work.
<br/>

# How to Install

1. Download and Install Python 3.7 or higher: https://www.python.org/
2. `git clone` this repo or download it.
3. Open CommandPrompt / PowerShell / Terminal and `cd` into the main library folder.
   * Example: `cd C:\plotManager`
4. Install the required modules: `pip install -r requirements.txt`
	* If you plan on using Notifications or Prometheus then run the following to install the required modules: `pip install -r requirements-notification.txt`
5. Copy `config.yaml.default` and name it as `config.yaml` in the same directory.
6. Edit and set up the config.yaml to your own personal settings. There is more help on this below.
	* You will need to add the `chia_location` as well! This should point to your chia executable.
7. Run the Manager: `python manager.py start`
   * This will start a process in the background that will manage plots based on your inputted settings.
8. Run the View: `python manager.py view`
   * This will loop through a view screen with details about active plots.
<br/>

# Changelog
* v0.1.0b@5
   1. Added thread usage information in view command (`python manager.py view`).

* v0.1.0b@4
  
  1. Added thread count column (-r) in view command (`python manager.py view`).

* v0.1.0@3
  
  1. Added history command (`python manager.py history`), shows a list containing information about the completed plots.<br/>
   Thank you **@ConnorChristie** for this feature.

  2. Added job parameter `plots_to_trigger`. It controls how many plots are started when the time comes, usefull to start more than 1 plot per stagger.

  3. Added job parameter `plot_automatically_optimization` and `optimization_max_threads`. Used when there are no plots in phases higher than 1, it fully uses the number of threads informed in  `optimization_max_threads`.