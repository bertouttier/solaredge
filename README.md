# Solaredge
API wrapper for Solaredge monitoring service.

See https://www.solaredge.com/sites/default/files/se_monitoring_api.pdf

## Create a new connection by supplying your Solaredge API key
``` python
s = solaredge.Solaredge("APIKEY")
```

## API Requests
11 API requests are supported. The methods return the parsed JSON response as a dict.

``` python
def get_list(self, size=100, startIndex=0, searchText="", sortProperty="", sortOrder='ASC', status='Active,Pending'):

def get_details(self, site_id):

def get_data_period(self, site_id):

def get_energy(self, site_id, startDate, endDate, timeUnit='DAY'):

def get_time_frame_energy(self, site_id, startDate, endDate, timeUnit='DAY'):

def get_power(self, site_id, startTime, endTime):

def get_overview(self, site_id):

def get_power_details(self, site_id, startTime, endTime, meters=None):

def get_energy_details(self, site_id, startTime, endTime, meters=None, timeUnit="DAY"):

def get_current_power_flow(self, site_id):

def get_storage_data(self, site_id, startTime, endTime, serials=None):
```

## TODO
* Add support for bulk requests
* Add API documentation
