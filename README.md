# Solaredge

API wrapper for Solaredge monitoring service.

See <https://www.solaredge.com/sites/default/files/se_monitoring_api.pdf>

## Create a new connection by supplying your Solaredge API key

```
s = solaredge.Solaredge("APIKEY")
```

## API Requests

14 API requests are supported. The methods return the parsed JSON response as a dict.

```
def get_list(self, size=100, startIndex=0, searchText="", sortProperty="", sortOrder='ASC', status='Active,Pending'):

def get_details(self, site_id):

def get_dataPeriod(self, site_id):

def get_energy(self, site_id, startDate, endDate, timeUnit='DAY'):

def get_timeFrameEnergy(self, site_id, startDate, endDate, timeUnit='DAY'):

def get_power(self, site_id, startTime, endTime):

def get_overview(self, site_id):

def get_powerDetails(self, site_id, startTime, endTime, meters=None):

def get_energyDetails(self, site_id, startTime, endTime, meters=None, timeUnit="DAY"):

def get_currentPowerFlow(self, site_id):

def get_storageData(self, site_id, startTime, endTime, serials=None):

get_componentList(self, site_id):

get_inventory(self, site_id):

def get_invertorDetails(self, site_id, invertor_id, startTime, endTime):
```

## TODO

- Add support for bulk requests
- Add API documentation
