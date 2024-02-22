1. initial_data_cleaning.ipynb
   - Fix convert the datetime column to datetime type
   - Add a column for date of week of checkout
   - Add a column for the different bins, we defined for the checkout time
     -  0: 00:00AM - 5:00AM
     -  1: 5AM-10AM
     -  2: 10AM-2PM
     -  3: 2PM-6PM
     -  4: 6PM-10:30PM
     -  5: 10:30PM-00:00AM

2. add_kiosk_coordinates.ipynb
   - Add coordinates of the Checkout and return kiosk
     - Get coordinates from heartland_bikeshare
     - add columns for coordinates of the Checkout and return kiosk 

   **Important** Some of the kiosk coordinates are not present, check the set difference between the kiosk names in the heartland_bikeshare and the kiosk names in the kiosk dataset.