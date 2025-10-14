| Campo | Tipo | Descripción | Fuente | Ejemplo |
|--------|------|-------------|--------|----------|
| flight_id | string | Identificador único del vuelo (concatenación de aerolínea, número y fecha) | Derivado | AA1234_2025-01-05_JFK_LAX |
| airline_iata | string | Código IATA de la aerolínea | S1_airlines.csv | AA |
| flight_number | string | Número de vuelo | S2_flights.csv | 1234 |
| origin_iata | string | Código IATA del aeropuerto de origen | S1_airports.csv | JFK |
| dest_iata | string | Código IATA del aeropuerto de destino | S1_airports.csv | LAX |
| sched_dep_utc | datetime | Hora programada de salida (UTC) | S2_flights.csv | 2025-01-05T14:30:00Z |
| actual_dep_utc | datetime | Hora real de salida (UTC) | S2_raw-flight-data.csv | 2025-01-05T14:45:00Z |
| sched_arr_utc | datetime | Hora programada de llegada (UTC) | S2_flights.csv | 2025-01-05T18:00:00Z |
| actual_arr_utc | datetime | Hora real de llegada (UTC) | S2_raw-flight-data.csv | 2025-01-05T18:25:00Z |
| dep_delay_min | int | Retraso en minutos en la salida | Derivado | 15 |
| arr_delay_min | int | Retraso en minutos en la llegada | Derivado | 25 |
| status | string | Estado del vuelo | S2_raw-flight-data.csv | Departed / Cancelled / Delayed |
| distance_km | float | Distancia entre aeropuertos en km | Calculado | 3970.4 |
| country_origin | string | País del aeropuerto de origen | S1_airports.csv | United States |
| country_dest | string | País del aeropuerto de destino | S1_airports.csv | United States |
| on_time_flag | boolean | Indicador de puntualidad (1 si retraso < 15 min) | Derivado | 0 |