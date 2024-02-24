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

3. google_travel_time.ipynb
  - I am using the `Kiosks_Data.csv` to calculate the travel time matrix between the kiosks.
  - One of the kiosk is from `PA` so i removed it before calculating the travel time matrix and all the help desks whose coordinates are `(0,0)`.
  - We are calculating the travel time for the bins we separated in the `initial_data_cleaning.ipynb` file.
    ``` {python}
          mode = ['bicycling', 'transit']
          hours = [
            datetime(2024, 2, 26, 7, 30, 0), # 5AM-10AM
            datetime(2024, 2, 26, 12, 00, 0), # 10AM-2PM
            datetime(2024, 2, 26, 16, 00, 0), # 2PM-6PM
            datetime(2024, 2, 26, 20, 15, 0) # 6PM-10:30PM
           ]
     ```


---
I am using `.env` file. Put this file on the root of the project. the current version of the `.env` file is:
```
GOOGLE_MAPS_API_KEY_1 = "google_maps_api_key"

MOHAMMAD_SHARED_PATH = "path to the folder shared by mohammad"

OUTPUT_PATH = "path to the folder where the output files will be saved"
```