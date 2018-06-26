# Reader Input Plugin

The `reader` plugin reads and parses files every interval.  Reader will always begin at the top of each file.

Reader supports all data_format formats

### Configuration

```toml
## Files to parse each interval.
## These accept standard unix glob matching rules, but with the addition of
## ** as a "super asterisk". ie:
##   /var/log/**.log     -> recursively find all .log files in /var/log
##   /var/log/*/*.log    -> find all .log files with a parent dir in /var/log
##   /var/log/apache.log -> only tail the apache log file
files = ["/var/log/apache/access.log"]

## The dataformat to be read from files
## Each data format has its own unique set of configuration options, read
## more about them here:
## https://github.com/influxdata/telegraf/blob/master/docs/DATA_FORMATS_INPUT.md
data_format = ""
```