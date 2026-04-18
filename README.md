# Telegraf json_v2 Parser for Shelly Energy Values

This Telegraf configuration demonstrates how to parse energy values from:

- **Shelly 3EM** via `http://<your-ip>/rpc/Shelly.GetStatus`
- **Shelly PM Mini** via `http://<your-ip>/rpc/Shelly.GetStatus` (same RPC endpoint, different payload structure per device)[web:62][web:64]

Below is an example JSON response for a **Shelly 3EM**.

## Example JSON: Shelly 3EM (`Shelly.GetStatus`)

```json
{
  "ble": {},
  "bthome": {},
  "cloud": {
    "connected": true
  },
  "em:0": {
    "id": 0,
    "a_current": 0.868,
    "a_voltage": 233.6,
    "a_act_power": 112.1,
    "a_aprt_power": 203,
    "a_pf": 0.55,
    "a_freq": 50,
    "b_current": 0.44,
    "b_voltage": 233.3,
    "b_act_power": 54.4,
    "b_aprt_power": 102.5,
    "b_pf": 0.52,
    "b_freq": 50,
    "c_current": 0.083,
    "c_voltage": 234.1,
    "c_act_power": 1.9,
    "c_aprt_power": 19.4,
    "c_pf": 0.1,
    "c_freq": 50,
    "n_current": null,
    "total_current": 1.391,
    "total_act_power": 168.449,
    "total_aprt_power": 324.873,
    "user_calibrated_phase": []
  },
  "em0": {
    "id": 0,
    "a_total_act_energy": 432377.89,
    "a_total_act_ret_energy": 117.49,
    "b_total_act_energy": 50809.89,
    "b_total_act_ret_energy": 82641.07,
    "c_total_act_energy": 44890.98,
    "c_total_act_ret_energy": 0.68,
    "total_act": 528078.77,
    "total_act_ret": 82759.23
  },
  "modbus": {},
  "mqtt": {
    "connected": false
  },
  "ws": {
    "connected": false
  }
}

