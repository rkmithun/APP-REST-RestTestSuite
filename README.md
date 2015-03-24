
##Name : 
  APP::REST::RestTestSuite

##Description:
    Rest Test Suite is a program that helps to automate the testing of Restfull Web services. 
    This Distribution is packaged with a CLI utility (rest-client)
    rest-client is the test automation CLI tool for testing restful web services
 
##Usage: 
    rest-client [options] command [...]

``` 
Options:
  -h,--help                 Display this usage. 
  -V,--version              Print the version of the tool. 
  -c,--configfile=<file>    Input the config file with full path.
  -l,--logdir=<dir>         Input full path of the directory where you want to log the test results.
  -t,--test-load=n          Test the average response time by simulating 'n' number of requests on the web server.
 
Commands:
  -r,--run-test-suite       Test the configured web services defined in the config file.
  -g,--get-sample-config    Get a sample config file to configure your web services as test suite. 
 
***Note: 
By default tool uses the sample-config file. You need to get that and configure the suite.
 
Examples:
  rest-client --get-sample-config           
                # Get sample config file for configuring web services in the current directory.
 
  rest-client --run-test-suite --configfile=<rest_config_file> 
                # Execute the test suite against the supplied config file. 
                # Supply the full path of config file if it is not present in current directory.
 
  rest-client --test-load=10 --configfile=<rest_config_file> 
                # Send parallel requests (10* number of web services configured in config file). 
                # Give average response time by simulating huge traffic in the web server.
 
  rest-client --run-test-suite --configfile=<rest_config_file>  --logdir=<log-directory-path>
  rest-client --test-load=10   --configfile=<rest_config_file>  --logdir=<log-directory-path>
                # Create LOG files in the path specified by executing the test cases. 

```
