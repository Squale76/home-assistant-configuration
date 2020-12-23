# Mes cartes

### Sommaire

- [La météo](#la-météo)
- [Les consos](#les-consos)
- [Les températures](#les-températures)
- [Les hygrométries](#les-hygrométries)
- [Les batteries](#les-batteries)

## La météo

<details><summary>Météo France</summary>

```yaml
type: 'custom:meteofrance-weather-card'
entity: weather.tancarville
number_of_forecasts: '7'
name: Tancarville
rainChanceEntity: sensor.tancarville_rain_chance
uvEntity: sensor.tancarville_uv
cloudCoverEntity: sensor.tancarville_cloud_cover
freezeChanceEntity: sensor.tancarville_freeze_chance
snowChanceEntity: sensor.tancarville_snow_chance
alertEntity: sensor.76_weather_alert
rainForecastEntity: sensor.tancarville_next_rain
```

</details>

## Les consos

<details><summary>Conso EDF</summary>

  ```yaml
align_icon: left
color_thresholds:
  - color: '#11f13a'
    value: 600
  - color: '#11f13a'
    value: 800
  - color: '#f0da11'
    value: 1000
  - color: '#ef5a0f'
    value: 3000
  - color: '#ef1d0f'
    value: 5000
entities:
  - sensor.puissance
hours_to_show: 24
hour24: true
more_info: false
name: Conso EDF
points_per_hour: 2
animate: true
show:
  labels: true
  name: true
type: 'custom:mini-graph-card'
  ```

</details>

<details><summary>Conso EDF par heure</summary>

  ```yaml
align_icon: left
color_thresholds:
  - color: '#11f13a'
    value: 30
  - color: '#f0da11'
    value: 60
  - color: '#ef5a0f'
    value: 90
  - color: '#ef1d0f'
    value: 120
entities:
  - sensor.index_wh
unit: Wh
aggregate_func: delta
hours_to_show: 1
hour24: true
more_info: false
name: Conso EDF par heure
points_per_hour: 60
animate: true
show:
  labels: true
  name: true
  state: false
type: 'custom:mini-graph-card'
  ```

</details>

<details><summary>Conso EDF par jour</summary>

  ```yaml
align_icon: left
color_thresholds:
  - color: '#11f13a'
    value: 900
  - color: '#f0da11'
    value: 1800
  - color: '#ef5a0f'
    value: 2700
  - color: '#ef1d0f'
    value: 3600
entities:
  - sensor.index_wh
unit: Wh
aggregate_func: delta
hours_to_show: 24
hour24: true
more_info: false
name: Conso EDF par jour
points_per_hour: 2
animate: true
show:
  labels: true
  name: true
  state: false
type: 'custom:mini-graph-card'
  ```

</details>

<details><summary>Conso EDF par semaine</summary>

  ```yaml
align_icon: left
color_thresholds:
  - color: '#11f13a'
    value: 1800
  - color: '#f0da11'
    value: 3600
  - color: '#ef5a0f'
    value: 5400
  - color: '#ef1d0f'
    value: 7200
entities:
  - sensor.index_wh
unit: kWh
hours_to_show: 168
hour24: true
more_info: false
name: Conso EDF par semaine
points_per_hour: 1
animate: true
show:
  labels: true
  name: true
  state: false
type: 'custom:mini-graph-card'
  ```

</details>

## Les températures

<details><summary>Température chambre</summary>

  ```yaml
align_icon: left
color_thresholds:
  - color: '#1da4f2'
    value: 18
  - color: '#11f13a'
    value: 20
  - color: '#f0da11'
    value: 22
  - color: '#ef5a0f'
    value: 24
  - color: '#ef1d0f'
    value: 25
entities:
  - sensor.aquara_1_temperature
hours_to_show: 24
hour24: true
line_color: '#1da4f2'
more_info: false
name: Chambre Morgane
points_per_hour: 2
show:
  labels: true
  name: true
type: 'custom:mini-graph-card'
  ```

</details>

## Les hygrométries

<details><summary>Hygrométrie chambre</summary>

  ```yaml
align_icon: left
color_thresholds:
  - color: '#ef1d0f'
    value: 40
  - color: '#ef5a0f'
    value: 45
  - color: '#11f13a'
    value: 60
  - color: '#ef5a0f'
    value: 65
  - color: '#ef1d0f'
    value: 70
entities:
  - sensor.aquara_1_humidity
hours_to_show: 24
hour24: true
line_color: '#1da4f2'
more_info: false
name: Chambre Morgane
points_per_hour: 2
show:
  labels: true
  name: true
type: 'custom:mini-graph-card'
  ```

</details>

## Les batteries

<details><summary>Batterie Aquara</summary>

  ```yaml
type: gauge
entity: sensor.aquara_1_battery
min: 0
max: 100
severity:
  green: 80
  yellow: 40
  red: 20
name: Aquara 1
  ```

</details>

<details><summary>Batterie Control Center</summary>

  ```yaml
type: gauge
entity: sensor.controlcenter_niveau_de_batterie
min: 0
max: 100
severity:
  green: 80
  yellow: 50
  red: 30
name: Control Center
  ```

</details>

<details><summary>Batterie Samsung A8</summary>

  ```yaml
type: gauge
entity: sensor.sm_a530f_sg_niveau_de_batterie
min: 0
max: 100
severity:
  green: 80
  yellow: 30
  red: 10
name: A8 (Sylvain)
  ```

</details>
