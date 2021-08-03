# abeillerelayhat

![Capture d’écran 2021-08-03 à 17 51 48](https://user-images.githubusercontent.com/8549674/128046691-9f86af3c-0eb2-48c8-8252-899b3f3f93f4.png)

Work in progress

## Documentation

Ce plugin permet de controler les 4 relais de la carte Seeed Relay Hat.
Il faut activer le bus I2C sur le RPI par l intermediaire de la commande:

sudo raspi-config

### Installation

https://wiki.seeedstudio.com/Raspberry_Pi_Relay_Board_v1.0/

#### Activer l I2C

raspi-config

![Capture d’écran 2021-08-03 à 17 48 51](https://user-images.githubusercontent.com/8549674/128046460-4aabcb8f-22ec-46b6-aea5-8137c23ed04f.png)

![Capture d’écran 2021-08-03 à 17 49 00](https://user-images.githubusercontent.com/8549674/128046484-57aefd20-dff8-471c-a42d-20be8f09bb75.png)

![Capture d’écran 2021-08-03 à 17 49 08](https://user-images.githubusercontent.com/8549674/128046514-968349a2-244e-4ab6-98b3-53c9a798f9b4.png)

![Capture d’écran 2021-08-03 à 17 49 15](https://user-images.githubusercontent.com/8549674/128046535-eb8a132c-8828-482f-a92e-c0eb81fadafa.png)


#### Verifier que l on voit la carte

i2cdetect -y -r 1

![Capture d’écran 2021-08-03 à 17 54 04](https://user-images.githubusercontent.com/8549674/128047007-d5e7b542-f9b1-4e79-9786-b6ccd60bf2bc.png)

Visible à l adresse 0x20.

## Changelog



## Support

Ouvrez des issues dans https://github.com/KiwiHC16/abeillerelayhat_Support/issues si vous souhaitez du support.
