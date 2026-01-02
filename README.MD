# 1.  Install ESPHome
1.  Install Python 3.13.x . Current release of ESPHome is not comopatible with Python 3.14+
2. Install `wheel` dependency: `pip3 install wheel`
3. Install `esphome` : `pip3 install esphome`
4. Verify `esphome` installation: `esphome --version`
5. Ensure python scripts path is added to PATH `C:\Users\xxxxx\AppData\Local\Programs\Python\Python313\Scripts\`

# 2. Config wifi settings
1. Create `secrets.yaml` in the same location as the main config yaml file
2. Fill out these entries :
```
wifi_ssid: "<put your wifi router's ssid>"
wifi_password: "<put your wifi router's password>"
```

# 3. Type `esphome run <main config file>.yaml`
 This should initiate the code gen routines, compile, create binary and flash it on the target device. <br> 
 
 >[!NOTE]
>
 > - Use `esphome -v run <main config file>.yaml` for verbose or set environment > variable `ESPHOME_VERBOSE` to `true`.<br>
 > `export ESPHOME_VERBOSE=true`<br>
 > - Use `--device` option to specify com port connected.<br>
 > Ex:
 > `esphome -v run <main config file>.yaml --device COM12`
 >  `esphome -v run <main config file>.yaml --device /dev/ttyUSB0`<br>
 > - Refer [cli reference](https://esphome.io/guides/cli/)




    