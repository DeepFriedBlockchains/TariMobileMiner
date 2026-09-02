# Tari Android Miner

A high performance and open-source application for mining Tari (XTM) on Android mobile devices using the TariRx algorithm.

<p align="left">
  <img src="https://tari.com/assets/img/mobile-miner.png" width="350" title="Tari Mobile Miner">
</p>

## Supported CPU instruction sets
- **arm64-v8a**
- **armeabi-v7a**
- **x86_64**

## Features		
- AMAYC machine-learning algorithm to protect the device
- Temperature display
- QR code feature to capture wallet address
- Completely redesigned UI
- Refactored framework
- Payout widget
- Live Pool statistics for pools based on nodejs-pool cryptonote-nodejs-pool frameworks

## Miner
This application is built upon TariRx, the official Tari (XTM) CPU miner.
- Miner: [TariRx](https://github.com/tari-project/tarix)
- Algorithm: [TariRx](https://www.tari.com/)
- Coin: Tari (XTM)

## Usage
### Settings
#### Pool
When opening the application for the first time, you have to specify the pool that you want to use to mine XTM. Some predefined pools have been configured to make it easier for you. You can still [add your own pool](https://github.com/tari-project/tarix) if needed.

The 'Worker name or pool options' field can be left blank if the pool doesn't use any options/password. In this case, the worker name will be set to your device type (make and model) by default.

#### Wallet Address
Specifies the Tari wallet address that will be used with the mining pool. A validation has been added to this field to make sure you enter a valid address. You can also use the provided QR code feature to scan your wallet address.

#### Hardware Settings
##### CPU Cores
The application automatically detects your device's number of CPU cores. Use less cores if you want to prevent your device from overheating or to keep using other applications while mining.

##### CPU Temperature
Defines the maximum temperature that you want your device's CPU to reach. If your device has no CPU temperature sensor, this setting will be ignored.

##### Battery Temperature
Defines the maximum temperature that you want your device's battery to reach. If your device has no Battery temperature sensor, this setting will be ignored.

##### Cooldown Threshold
Defines the temperature at which the application will resume the mining process. Both the CPU and Battery temperatures must have reached the safe level for the miner to resume.

##### Disable Temperature Control
This application implements two layers of protection for your device. The first one is the As-Much-As-You-Can (AMAYC) machine learning algorithm that can predict when your device will overheat and stops mining preemptively. The second layer is a maximum temperature threshold.

#### Options
##### Mining Goal
The mining goal should reflect the pool payout setting, but you can also specify a custom value for your device. The default value is the minimum payout value of the specified mining pool.

##### Pause mining on battery power
Enable this feature to pause mining when your device is not charging.

When saving the settings, you will be redirected automatically to the Miner page. Just hit 'Start' to start mining.

### Miner

The Payout Widget which is at the top of the screen displays the current balance for the selected pool and the progression toward the defined mining goal. If the specified pool does not provide an API, a manually configured payout will be used.

The stats about the hashrate and the accepted shares are then presented in the Device Widget. All the information is extracted from TariRx. The hashrate information comes from the 15s/30s/60s hash rate averages provided by the miner.

You can use the buttons at the bottom of the application to display the hashrate in the log ('H'), to pause the miner ('P') and to resume the miner ('R'). You cannot resume the miner when the device has not reached the cooldown threshold temperature.

The application will keep mining even when your device is on standby mode. So keep in mind that even if your phone screen is off, your device may still be running.

## Future development
- Push notifications
- Wallet integration
- Unified design for the all-in-one application

## Donations
Donations setting has been set to 0% in the TariRx lib embedded within the application.
* XTM: ""
* BTC: ""
* ETH: ""

## Credits
* Forked from [Scala MobileMiner](https://github.com/scala-network/MobileMiner)
* Originally forked from [Mine2gether](https://github.com/Mine2Gether/m2g_android_miner)
* Original code from [MoneroMiner](https://github.com/upost/MoneroMiner)

## Contacts
* [Tari Website](https://www.tari.com/)
* [Tari Discord](https://discord.gg/tari)
* [Tari GitHub](https://github.com/tari-project/tari)

# License

TariRx and Tari Mobile Miner is licensed as GPLv3, thus this derivative work also is. You need to consider this if you plan to publish an Android application. You'd probably need to make it GPLv3 also.
