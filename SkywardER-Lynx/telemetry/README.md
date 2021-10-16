## Telemetry
`hr_tm.csv` contains high-rate telemetry from the rocket in CSV format.

Note: due to missing GPS fix, gps data and navigation system data are mostly meaningless


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