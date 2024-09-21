# Flight-Arrival-Schedule
The `train-data.txt` file contains flight data, with each line representing a record. Each record includes the following fields:

1. **ID**: The unique identifier of the aircraft.
2. **Flight Altitude**: The altitude of the aircraft (unit: unknown).
3. **Return Airspace**: The return airspace code of the aircraft.
4. **Requested Takeoff Time**: The time the aircraft requested to take off.
5. **Requested Landing Time**: The time the aircraft requested to land.
6. **Local Flight**: Indicates whether the flight is a local flight (`local` or 'external').
7. **End of Current Sorting History**: Indicates whether this record ends the current sorting history (`0` means not ended, `1` means ended).

# Train Data for Fine-Tuning

The `train.jsonl` file contains flight data used for fine-tuning machine learning models. Each line in the file is a JSON object that includes a `prompt` and a `response`. The `prompt` provides the input data, and the `response` provides the expected output.

1. **flight_info**: Contains information about the flight.
   - **id**: The unique identifier of the aircraft.
   - **type**: The type of the aircraft (e.g., J, B, Y).
   - **requested_slot**: The requested time slot for the flight.
   - **done**: Indicates whether the flight has completed its current sorting history (`0` means not done, `1` means done).

2. **history_info**: Contains historical information about previous flights.
   - **requested_slot**: The requested time slot for the previous flight.
   - **real_slot**: The actual time slot assigned to the previous flight.
   - **flight_id**: The unique identifier of the previous flight.
   - **delay**: The delay in minutes for the previous flight.
   - **ep_done**: Indicates whether the previous flight has completed its current sorting history (`false` means not done, `true` means done).

