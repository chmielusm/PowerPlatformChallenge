# Building Permit Inspections

The City of Santa Monica publishes their [Building Permit Inspection Schedule as open data](https://data.smgov.net/Permits-Licenses/Permit-Inspections-Schedule/xird-2kxi).  Building inspectors need to travel to various locations throughout the day to inspect building that are under construction.  Building inspector supervisors need to ensure timely delivery of services and analyze overall trends.  The solution is about to help the Building and Safety Division manage their requests for building permit inspections.

## Solution

The solution has been built on top of [Microsoft Dynamics 365 Field Service](https://dynamics.microsoft.com/en-us/field-service/overview/?&ef_id=Cj0KCQjwz96WBhC8ARIsAATR2521WDJPBJvC-ocw6fq6Q0_xx2023YD3RcseFMRT2EBQJJRvt_MVbZEaAhl_EALw_wcB:G:s&OCID=AIDcmm3ddy0xh5_SEM_Cj0KCQjwz96WBhC8ARIsAATR2521WDJPBJvC-ocw6fq6Q0_xx2023YD3RcseFMRT2EBQJJRvt_MVbZEaAhl_EALw_wcB:G:s&gclid=Cj0KCQjwz96WBhC8ARIsAATR2521WDJPBJvC-ocw6fq6Q0_xx2023YD3RcseFMRT2EBQJJRvt_MVbZEaAhl_EALw_wcB) and contains of following components:

-   Santa Monica Open Data Custom Connector

-   Load Data Power Automate

-   Amended Field Service tables, i.e: Work Order

All above are included in the Power Apps solution named Building Permit Inspection.


## Assumptions

Below is the list of assumptions taken into consideration:

* Field Service has capabilities to manage a schedule of dispatches and its mobile application can help inspectors to confirm inspections in certain buildings
* Custom connector supports fetching requests from Santa Monica open data service
* Power Automate (flow) has been used to load a data from Santa Monica service.
* The solution matches Service Account by geospatial data (longitude, latitude)

## Open questions and a roadmap

However there are still some questions to be addressed:

* What is the ultimate source system? Assumed Santa Monica Building Permit Inspection Schedule open data service therefore would need to sync updated Work Orders and Bookings in certain interval.
* Custom connector would need to support fetching specifc inspection request from Santa Monica open data service along with upserting if necessary.
* How to match request from the service with Service Account?
* Consider building DataFlow to sync data instead of Power Automate (flow)
* Extend solution to update Work Order records based upon last sync date along with Bookings
* Wouldn't be worth to integrate with Teams in order to [collaborate with inspectors](https://docs.microsoft.com/en-us/dynamics365/field-service/field-service-teams-collaboration)?


## Installation Guildline

1 Install [Microsoft Dynamics 365 Field Service](https://docs.microsoft.com/en-us/dynamics365/field-service/install-field-service)

2 Install Building Permit Inspection solution
