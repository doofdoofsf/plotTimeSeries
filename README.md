# plot_time_series

The plot_time_series is a simple utility for plotting a time_series graph using R
with some flexibility. This is handy for e.g. plotting KPI values over time.

## Requirements

To use this script, you need to [install R](http://cran.r-project.org/mirrors.html) and then get the `getopt` package. 
To install the `getopt` package, fire up R (type R in your terminal) and type in something like:

    install.packages('getopt', repos='http://cran.us.r-project.org')

## Usage

    NAME
          plot_time_series
    
    SYNOPSIS
           Usage: ../plot_time_series [-[-verbose|v]] [-[-help|h]] [-[-show_gridlines|g]] [-[-remove_outliers|o]] [-[-csv_filename|c] <character>] [-[-output_filename|f] <character>] [-[-title|t] <character>] [-[-y_title|y] <character>] [-[-y_unit|s] <character>] [-[-x_spacing|x] [<character>]] [-[-smoothness|m] [<double>]] [-[-width|w] [<integer>]] [-[-height|u] [<integer>]] [-[-point_color|p] [<character>]] [-[-sunday_point_color|z] [<character>]] [-[-axis_color|a] [<character>]]
    
    DESCRIPTION
          The plot_time_series is a simple utility for plotting a time series graph using R
          This is useful for e.g. plotting KPI values over time.
          The graph is drawn as a scatterplot with a LOESS fit line of variable smoothness
    
    OPTIONS
          The options are as follows:
    
          --verbose            Get a little chatty?
          --width              The width of the graph in pixels
          --height             The height of the graph in pixels
          --csv_filename       A CSV containing input data with columns date,value (example below)
          --output_filename    The file that the graph is written to
          --title              The title shown above the graph
          --y_title            The title shown on the y axis of the graph
          --y_unit             A string appended to the y axis values e.g. MM
          --x_spacing          How the x-axis is spaced e.g. day, 3 days, week, month, 2 weeks, 2 months
          --point_color        The color to draw points in
          --sunday_point_color The color to draw sunday points in
          --axis_color         The color to use for the axis
          --smoothness         How much to smooth the LOESS fit line. Float between 0 and 1
          --remove_outliers    Automagically remove outlying points?
          --show_gridlines     Show gridlines?
    
    EXAMPLES
          $ plot_time_series --width=800 --height=400 --x_spacing=month --csv_filename=test_data/unbranded_organic_registrations.csv --output_filename=output/unbranded_organic_registrations.png --title="Unbranded Organic Registrations: %s to %s" --y_title="Number Registrations"
    
    
    EXAMPLE INPUT FILE
          date,value
          03/06/2012,6347.04
          03/07/2012,9990.23
          03/08/2012,6773.41
    
    COLOR
          Available colors documented at: http://www.stat.columbia.edu/~tzheng/files/Rcolor.pdf
    

## Testing

There is a test directory with some lovely testy stuff in it:

    test/test_data - a directory with some test csv files in it
    test/output    - a directory that the test script dumps images into
    run_test       - a bash script that calls plot_time_series to generate a few graphs

    $ cd test
    $ ./run_test 
    $ ls output/*.png

## Examples

Example graphs are shown below. These are produced by from the data in the `test` directory

#### A simple graph showing registrations by time
![registrations by time](https://raw.github.com/doofdoofsf/plotTimeSeries/master/test/output/acme_registrations_thumb.png)

#### The same graph with a bit more detail
![registrations by time](https://raw.github.com/doofdoofsf/plotTimeSeries/master/test/output/acme_registrations.png)
