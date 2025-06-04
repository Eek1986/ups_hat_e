This fork from: [Orgjvr/ups_hat_e](https://github.com/Orgjvr/ups_hat_e). Thank him very much

*** HomeAssistant integration for the [Waveshare Pi UPS Hat (E)](https://www.waveshare.com/wiki/UPS_HAT_(E)).

Instructions:
1) Copy component from git to HA "/homeassistant/custom_components". Connect on ssh:
   ```bash
   $ cd /homeassistant/custom_components
   $ wget https://github.com/Eek1986/ups_hat_e/archive/refs/heads/master.zip
   $ unzip master.zip
   $ rm master.zip
   ```
2) Config component in configuration.yaml
   ```
   #
   # https://github.com/Eek1986/ups_hat_e
   #
   ups_hat_e:
     scan_interval: 10         # Required, second
     name: UPS                 # Optional, default=HA Pi UPS
     unique_id: ups_hat_e      # Optional, default=ha_pi_ups
     battery_capacity: 5000    # Optional (mAh), default=4800
     addr: 0x2d                # Optional, default=0x2d
   ```
3) Reboot HA.

P.S. [Custom Integration: Waveshare UPS for Raspberry Pi](https://community.home-assistant.io/t/custom-integration-waveshare-ups-for-raspberry-pi/577833) ([rpi_waveshare_ups](https://github.com/uvjim/rpi_waveshare_ups)) and the analogs did not work with UPS HAT(E).
