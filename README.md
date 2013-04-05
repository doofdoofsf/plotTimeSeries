## Examples

Example graphs are shown below. These are produced by from the data in the `test` directory

#### A simple graph showing registrations by time
!["registrations thumb"](https://raw.github.com/doofdoofsf/plotTimeSeries/master/test/output/acme_registrations_thumb.png)

     ../plot_time_series --width=500 --height=400 --x_spacing=month 
     --csv_filename=test_data/acme_registrations.csv --point_color=gray80 --sunday_point_color=gray80 
     --remove_outliers --smoothness=0.8

#### A detailed graph showing registrations by time
!["registrations graph"](https://raw.github.com/doofdoofsf/plotTimeSeries/master/test/output/acme_registrations.png)

     ../plot_time_series --width=1200 --height=700 --x_spacing=week 
     --csv_filename=test_data/acme_registrations.csv --show_gridlines --title="Acme Registrations: %s to 
     %s" --y_title="Number Registrations" --remove_outliers

#### A simple graph showing revenue by time
!["revenue thumb"](https://raw.github.com/doofdoofsf/plotTimeSeries/master/test/output/acme_revenue_thumb.png)

     ../plot_time_series --width=500 --height=400 --x_spacing="2 months" 
     --csv_filename=test_data/acme_revenue.csv --point_color=gray80 --sunday_point_color=gray80 
     --remove_outliers --smoothness=0.8

#### A detailed graph showing revenue by time
!["revenue graph"](https://raw.github.com/doofdoofsf/plotTimeSeries/master/test/output/acme_revenue.png)

     ../plot_time_series --width=1200 --height=700 --x_spacing=week 
     --csv_filename=test_data/acme_revenue.csv --show_gridlines --title="Acme Revenue: %s to %s" 
     --remove_outliers

#### A detailed graph showing revenue by time with targets
!["revenue graph with targets"](https://raw.github.com/doofdoofsf/plotTimeSeries/master/test/output/acme_revenue_targets.png)

     ../plot_time_series --width=1200 --height=700 --x_spacing=week 
     --csv_filename=test_data/acme_revenue.csv --show_gridlines --title="Acme Revenue: %s to %s" 
     --remove_outliers --special_points_filename=test_data/acme_revenue_targets.csv 
     --special_points_color=cornflowerblue --point_color=gray80 --sunday_point_color=gray80

#### A simple graph showing registrations by time from August to September
!["registrations thumb"](https://raw.github.com/doofdoofsf/plotTimeSeries/master/test/output/acme_registrations_thumb_dates.png)

     ../plot_time_series --width=500 --height=400 --x_spacing=month 
     --csv_filename=test_data/acme_registrations.csv --point_color=gray80 --sunday_point_color=gray80 
     --remove_outliers --smoothness=0.8 --x_range=04/01/2012:09/01/2012 --y_range=50:250
