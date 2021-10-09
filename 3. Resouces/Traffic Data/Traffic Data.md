# List of sources of traffic data in Scotland
## Here  API
More details here :) on the [[Traffic Speed Bot]]

test

## 
[Traffic Scotland  Public Transport Information](https://trafficscotland.org/publictransport/)


[Quarterly traffic estimates (TRA25)](https://www.gov.uk/government/statistical-data-sets/tra25-quarterly-estimates)

TRA0401: [Pedal cycle traffic (vehicle miles and kilometres) in Great Britain](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/981991/tra0401.ods) (ODS, 19.1KB)

## Traffic volume in miles (TRA01)

TRA0101: [Road traffic (vehicle miles) by vehicle type in Great Britain](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/981969/tra0101.ods) (ODS, 22.2KB)

TRA0102: [Motor vehicle traffic (vehicle miles) by road class in Great Britain](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/981970/tra0102.ods) (ODS, 24.8KB)

TRA0103: [Motor vehicle traffic (vehicle miles) by road class, region and country in Great Britain](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/981971/tra0103.ods) (ODS, 199KB)

TRA0104: [Road traffic (vehicle miles) by vehicle type and road class in Great Britain](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/981972/tra0104.ods) (ODS, 59.4KB)

TRA0105: [Change in traffic on major roads by region and country in Great Britain, from 10 years ago to latest year](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/981973/tra0105.ods) (ODS, 23.1KB)

TRA0106: [Motor vehicle traffic (vehicle miles) by vehicle type, region and country in Great Britain](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/981974/tra0106.ods) (ODS, 132KB)

TRA8901: [Motor vehicle traffic (vehicle miles) by local authority in Great Britain](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/982024/tra8901.ods) (ODS, 66.9KB)

TRA8902: [Motor vehicle traffic (vehicle miles) by local authority and selected vehicle type in Great Britain](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/982025/tra8902.ods) (ODS, 160KB)

TRA8905: [Motor vehicle traffic (vehicle kilometres) by local authority and selected vehicle type in Great Britain](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/982028/tra8905.ods) (ODS, 169KB)

[Road traffic statistics - Local authority Glasgow City](https://roadtraffic.dft.gov.uk/local-authorities/3)

1.70 billion vehicle miles were travelled on roads in Glasgow City in 2020.

Whilst historically significant, the long term trends can be misleading in most cases due to the extraordinary circumstances observed as a result of the coronavirus pandemic. Vehicle miles travelled in Great Britain have had year-on-year growth in each year between 2010 and 2019. However, the sharp decrease in 2020 has resulted in traffic estimates that are lower than the 2010 levels. Therefore, to say traffic has fallen over the last decade would misconstrue, as the overall decrease is entirely due to the decline in traffic levels observed in the 2020 estimates.

Traffic estimates for the period since 2010 have been revised to take into account the minor road benchmarking exercise. Further details available on GOV.UK: [Road traffic statistics: minor road benchmarking](https://www.gov.uk/government/publications/road-traffic-statistics-minor-road-benchmarking)



 Count points
  Count points in Glasgow City details.
  [JSON](https://roadtraffic.dft.gov.uk/api/count-points?filter[local_authority_id]=3)| [CSV](https://storage.googleapis.com/dft-statistics/road-traffic/downloads/countpoints/local_authority_id/dft_countpoints_local_authority_id_3.csv) 
                                                                                                                                           
Traffic

Traffic is calculated by multiplying AADF by the corresponding length of road and by the number of days in the given year.

28

[JSON](https://roadtraffic.dft.gov.uk/api/traffic/local-authorities?filter[local_authority_id]=3) | [CSV](https://storage.googleapis.com/dft-statistics/road-traffic/downloads/traffic/local_authority_id/dft_traffic_local_authority_id_3.csv)

Average annual daily flow

Number of vehicles that travel past the count point (in both directions) on an average day of the year.

3,537

[JSON](https://roadtraffic.dft.gov.uk/api/average-annual-daily-flow?filter[local_authority_id]=3) | [CSV](https://storage.googleapis.com/dft-statistics/road-traffic/downloads/aadf/local_authority_id/dft_aadf_local_authority_id_3.csv)

Average annual daily flow by direction

Number of vehicles that travel past the count point on an average day of the year, by direction of travel.

6,285

[JSON](https://roadtraffic.dft.gov.uk/api/average-annual-daily-flow-by-direction?filter[local_authority_id]=3) | [CSV](https://storage.googleapis.com/dft-statistics/road-traffic/downloads/aadfbydirection/local_authority_id/dft_aadfbydirection_local_authority_id_3.csv)

Raw counts

Vehicle counts recorded at this count point.

17,232

[JSON](https://roadtraffic.dft.gov.uk/api/raw-counts?filter[local_authority_id]=3) | [CSV](https://storage.googleapis.com/dft-statistics/road-traffic/downloads/rawcount/local_authority_id/dft_rawcount_local_authority_id_3.csv)

[Glasgow traffic report  TomTom Traffic Index](https://www.tomtom.com/en_gb/traffic-index/glasgow-traffic/)

[The effects of the lockdown on traffic in Glasgow](https://www.ubdc.ac.uk/news-media/2020/april/the-effects-of-the-lockdown-on-traffic-in-glasgow/)

Glasgow Real Time Data
[Changelog](https://gcc.developer.azure-api.net/api-changelog#api=55c36a318b3a0306f0009483)

Access to real time traffic and parking information from around Glasgow using the DATEX II protocol.

[Traffic Scotland](https://trafficscotland.org/datex/)

More information can be found at https://trafficscotland.org/datex/

Traffic locations - https://gcc.azure-api.net/traffic/locations?format=json

Traffic - https://gcc.azure-api.net/traffic/movement?format=json

Car Parks - https://gcc.azure-api.net/traffic/carparks?format=json

People counting
[UBDC - Avenues project api](https://api.ubdc.ac.uk/cctv/)

-   [/counts](https://api.ubdc.ac.uk/cctv/counts/)
-   response example:`{"0": {"timestp_UTC": "2019-11-30 04:30:01.428000", "location": "Argyle_St_@_Oswald_St(static)", "car": 2, "person": 0, "bicycle": 0, "motorcycle": 0, "bus": 0, "truck": 0}, "1": {"timestp_UTC": "2019-11-30 04:30:01.431000", "location": "Sauchiehall_St_@_Pitt_St", "car": 5, "person": 0, "bicycle": 0, "motorcycle": 0, "bus": 0, "truck": 0}}`
-   [Download all counts](https://api.ubdc.ac.uk/cctv/download)


