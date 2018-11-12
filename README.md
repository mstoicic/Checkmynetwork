# Checkmynetwork
Scheduled ping checks and speedtests with data persistence.

Tested on Windows 10 and Ubuntu. Other Linux OSs will almost certainly work, macOS maybe.

&nbsp;

### Setup
  Requires `arrow` and `speedtest-cli` modules.


&nbsp;
### Usage
  Requires `Python 3.6+` and `pipenv`

  To install required dependencies and run the program use commands:

    pipenv install
    pipenv run python Checkmynetwork.py
&nbsp;
    
    python netcheck.py
        --ping-host [www.google.com] ~ Hostname or ip to ping
        --ping-count [25] ~ Number of pings to perform during each test
        --run-console-loop (Y/n) ~ Run in a loop that pretty-prints output. "n" allows for the use of other task schedulers.
        --test-delay [10] ~ Delay between each test, in minutes
        --timezone [Europe/Zagreb] ~ Timezone to use for log timestamps
        --timestamp-format [YY/MM/DD HH:mm:ss] ~ Timezone format for logs. Excluding seconds (ss) may cause database errors.
        --db-filename [connection_data.sqlite] ~ Database filename
        --dump-csv ~ Dump database to CSVs and exit
  
  Exit with ctrl+c, then the data will be dumped to two tab-delimited CSVs files