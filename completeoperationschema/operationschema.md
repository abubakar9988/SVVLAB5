

| ID | Precondition | Events/Inputs | Post-condition |
|---|---|---|---|
| OP01 | System is powered on. | Power-on event; sensor and control-device status signals. | All essential sensors are checked. If all sensors are OK, the system enters **MONITORING** mode. Otherwise, conservation remains blocked and the fault is reported. |
| OP02 | Self-check passed; artifact is placed inside the chamber; artifact identification and limits are available. | Artifact placed; artifact ID; required temperature and humidity limits. | Artifact ID and environmental profile are stored, and monitoring of the artifact begins. |
| OP03 | Self-check passed; system is in **MONITORING** or a later active mode. | Periodic readings: temperature, humidity, light, vibration, door status, and power availability. | Latest sensor values are made available to all other operations. |
| OP04 | Artifact profile is loaded; door is closed; no vibration or protection response is active. | Door-closed signal; profile-loaded flag. | Normal conservation monitoring and environmental control begin. |
| OP05 | Environmental monitoring is active; artifact profile is loaded. | Current temperature and humidity readings; permitted environmental limits. | Actual readings are compared with the artifact's permitted ranges, and any violation is identified. |
| OP06 | Temperature or humidity is outside the permitted range. | Out-of-range sensor reading; environmental-control command. | Environmental-control mechanisms are activated to bring temperature and humidity back within the permitted limits. |
| OP07 | A correction action has been activated. | Updated temperature and humidity readings; recovery timer. | The system confirms through sensor readings that environmental conditions have returned to the permitted range within the recovery period. |
| OP08 | Environmental conditions fail to recover within the required time. | Recovery timeout; continued out-of-range readings. | Artifact protection is activated, including reduced light exposure and additional environmental controls. |
| OP09 | An abnormal or protection-level condition is detected. | Fault condition; protection activation; recovery failure. | An alert is generated and the museum operator is notified. |
| OP10 | Significant vibration is detected while conservation is active. | Vibration reading above the defined threshold. | Risky activities are suspended to reduce the possibility of damage to the artifact. |
| OP11 | Vibration-related activities have been suspended. | Continuous vibration readings; stabilization timer. | The system confirms that vibration remains below the threshold for the complete stabilization period before activities can resume. |
| OP12 | Conservation operation is active and the chamber door is opened. | Door-open signal. | Normal environmental operation is immediately suspended until the chamber door is safely closed. |
