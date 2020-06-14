## Configuring WIFI

Open the wpa supplicant file (nano installed by default)

```
sudo nano /etc/wpa_supplicant/wpa_supplicant.conf
```

Add a network by following the following format

**Read comments**

```
network={
    ssid="testing"

    scan_ssid=1             # If network is hidden

    psk="testingPassword"   # If WPA network
    key_mgmt=NONE           # If unprotected network

    country=US              # If 5ghz enabled network

    priority=1              # If other networks 
}
```

Save and exit nano (Ctrl+X, Y, Enter)

Update settings

```
wpa_cli -i wlan0 reconfigure
```

Check network connection (usually takes a minute to authenticate)

```
ifconfig wlan0
```

### Encrypting psk

Run the following command and enter the password when prompted

```
wpa_passphrase <ssid>
```