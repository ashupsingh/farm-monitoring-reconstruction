# Farm monitoring: methodology

Status: researched reconstruction / proposed evaluation, prepared 23 October 2026. Not a recovered lab notebook.

## Existing account

Uses soil moisture, temperature/humidity, and PIR sensing with a NodeMCU/ESP8266 and the Blynk app for remote agricultural monitoring.

The account above comes from the existing portfolio and is not independent verification. Listed stack: NodeMCU/ESP8266, DHT11, Soil Sensor, PIR Sensor, Blynk. Exact components and versions still need confirmation.

## System architecture

PIR/soil/temperature sensing -> ESP8266 -> virtual datastreams -> Blynk display

## Proposed engineering workflow

1. Confirm DHT11 versus DS18B20 wiring and which measurements each supplied.
2. Schedule independent acquisition intervals and debounce PIR events.
3. Map values and units to documented Blynk datastreams.
4. Buffer or mark data gaps during Wi-Fi failure and reconnect without flooding updates.

## Evaluation plan, not results

Record: Sensor agreement; reconnect duration; false PIR events; stale-data indication. Use explicit units, test conditions, a baseline where relevant, repeated observations and a timestamped log. Report failure cases alongside successes. No numerical result is available from this reconstruction.

## Limitations and claim boundaries

DS18B20 appears in the description but not the original stack list. Resolve that discrepancy before listing it as installed hardware.

## Design questions for an interview

- Explain the input, decision and output paths in the architecture above.
- What concrete fault would invalidate the output, and how would you detect it?
- Which design decision did you personally make, and what evidence do you retain?
- Which part of this proposed workflow differs from what you actually built?

## Research basis

[Blynk virtual pins](https://docs.blynk.io/en/blynk-library-firmware-api/virtual-pins) — consulted 23 October 2026. This source supports the underlying engineering topic, not the historical implementation. Workflow and evaluation proposals above are original analysis for this project.
