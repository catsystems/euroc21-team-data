# Lynx Flight Data (Roccaraso)
## Folder structure

- `./data/deathstack`: SRAD electronics logs, both on micro SD and telemetry (raw and csv)
- `./data/easymini`: COTS electronics logs (raw and csv)

## Telemetry
`data/deathstack/telemetry/csv/hr_tm.csv` contains high-rate telemetry from the rocket in CSV format.

| Column | Data Type | Unit | Description |
| ----------- | ----------- |  ----------- | ----------- |
| timestamp | uint64_t | ms | Timestamp in milliseconds |
| ada_state | uint8_t | - | ADA Controller State |
| fmm_state | uint8_t | - | Flight Mode Manager State |
| dpl_state | uint8_t | - | Deployment Controller State |
| ab_state | uint8_t | - | Aerobrake FSM state |
| nas_state | uint8_t | - | Navigation System FSM State |
| pressure_ada | float | Pa | Atmospheric pressure estimated by ADA |
| pressure_digi | float | Pa | Pressure from digital sensor |
| pressure_dpl | float | Pa | Pressure from deployment vane sensor |
| airspeed_pitot | float | m/s | Pitot airspeed |
| msl_altitude | float | m | Altitude above mean sea level |
| ada_vert_speed | float | m/s | Vertical speed estimated by ADA |
| ada_vert_accel | float | m/s^2 | Vertical acceleration estimated by ADA |
| acc_x | float | m/s^2 | Acceleration on X axis (body) |
| acc_y | float | m/s^2 | Acceleration on Y axis (body) |
| acc_z | float | m/s^2 | Acceleration on Z axis (body) |
| gyro_x | float | rad/s | Angular speed on X axis (body) |
| gyro_y | float | rad/s | Angular speed on Y axis (body) |
| gyro_z | float | rad/s | Angular speed on Z axis (body) |
| mag_x | float | uT | Magnetic field on X axis (body) |
| mag_y | float | uT | Magnetic field on Y axis (body) |
| mag_z | float | uT | Magnetic field on Z axis (body)|
| gps_fix | uint8_t | - | GPS fix (1 = fix, 0 = no fix) |
| gps_lat | float | deg | Latitude |
| gps_lon | float | deg | Longitude |
| gps_alt | float | m | GPS Altitude |
| vbat | float | V | Battery voltage |
| vsupply_5v | float | V | Power supply 5V |
| temperature | float | degC | Temperature |
| pin_launch | uint8_t | - | Launch pin status (1 = connected, 0 = disconnected) |
| pin_nosecone | uint8_t | - | Nosecone pin status (1 = connected, 0 = disconnected) |
| servo_sensor | uint8_t | - | Servo sensor status (1 = actuated, 0 = idle) |
| ab_angle | float | deg | Aerobrakes angle |
| ab_estimated_cd | float | Estimated drag coefficient |
| nas_x | float | deg | Navigation system estimated X position (longitude) |
| nas_y | float | deg | Navigation system estimated Y position (latitude) |
| nas_z | float | m | Navigation system estimated Z position |
| nas_vx | float | m/s | Navigation system estimated north velocity |
| nas_vy | float | m/s | Navigation system estimated east velocity |
| nas_vz | float | m/s | Navigation system estimated down velocity |
| nas_roll | float | deg | Navigation system estimated attitude (roll) |
| nas_pitch | float | deg | Navigation system estimated attitude (pitch) |
| nas_yaw | float | deg | Navigation system estimated attitude (yaw) |
| nas_bias0 | float | - | Navigation system bias |
| nas_bias1 | float | - | Navigation system bias |
| nas_bias2 | float | - | Navigation system bias |
| logger_error | int8_t | - | Logger error (0 = no error, -1 otherwise) |

## Logs

### Sensors
| File | Description |
| ----------- | ----------- |
| imu_accel_gyro.csv | BMX160 Accelerometer and Gyroscope (1600 Hz) |
| imu_compass.csv | BMX160 Magnetometer (100 Hz) |
| imu_temperature.csv | BMX160 Thermometer |
| pressure_ms5803.csv | MS5803 Digital Barometer (66.6 Hz) |
| pressure_static_port.csv | MPXHZ6130A analog Pressure sensor (connected to a static pressure port)  (42 Hz) |
| pressure_deployment_bay.csv | SSCDANN030PAA analog pressure sensor measuring pressure inside the deployment bay (42 Hz) |
| pitot.csv | Pressure and airspeed data from the SSCDRRN015PDA differential pressure sensor, connected to the pitot tube (42 Hz) |
| battery.csv | 3S LiPo voltage |
| apogeedetectionfilter.csv | Data from the Kalman filter used for apogee detection |
| statemachine.csv | Main computer state machine (9=Armed, 10=Ascent, 11=Drogue deployed, 12=Main chute deployed|
