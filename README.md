# Abeille Relay Hat

![Capture d’écran 2021-08-03 à 17 51 48](https://user-images.githubusercontent.com/8549674/128046691-9f86af3c-0eb2-48c8-8252-899b3f3f93f4.png)

Work in progress

## Documentation

Ce plugin permet de controler les 4 relais de la carte Seeed Relay Hat.
Le plugin ne prend pas en compte l'installation au niveau systeme de la carte et vous devez le faire manuellement.


### Installation

https://wiki.seeedstudio.com/Raspberry_Pi_Relay_Board_v1.0/

#### Activer l I2C

sudo raspi-config

![Capture d’écran 2021-08-03 à 17 48 51](https://user-images.githubusercontent.com/8549674/128046460-4aabcb8f-22ec-46b6-aea5-8137c23ed04f.png)

![Capture d’écran 2021-08-03 à 17 49 00](https://user-images.githubusercontent.com/8549674/128046484-57aefd20-dff8-471c-a42d-20be8f09bb75.png)

![Capture d’écran 2021-08-03 à 17 49 08](https://user-images.githubusercontent.com/8549674/128046514-968349a2-244e-4ab6-98b3-53c9a798f9b4.png)

![Capture d’écran 2021-08-03 à 17 49 15](https://user-images.githubusercontent.com/8549674/128046535-eb8a132c-8828-482f-a92e-c0eb81fadafa.png)


#### Verifier que l on voit la carte

sudo apt install -y i2c-tools
sudo i2cdetect -y -r 1

![Capture d’écran 2021-08-03 à 17 54 04](https://user-images.githubusercontent.com/8549674/128047007-d5e7b542-f9b1-4e79-9786-b6ccd60bf2bc.png)

Visible à l adresse 0x20.

#### smbus

sudo pip install smbus

#### Controle du premier relai

```shell
cd /var/www/html/plugins/abeillerelayhat/3rdparty/seeed-studio-relay-v2
sudo python seeed_relay_test.py
(saisir 1on et 1off pour faire basculer le relai et finir avec un ctrl-C)
input: 1on
ON_1...
input: 1off
OFF_1...
input: ^CALL OFF...
```

### Installation plugin

Maintenant que la carte fonctionne, on peut installer le plugin depuis le market de façon classique.

Puis activer le plugin.

![Capture d’écran 2021-08-04 à 10 58 56](https://user-images.githubusercontent.com/8549674/128153142-b30c5a93-3668-41c9-b81f-9480d89ebb5c.png)

### Creation equipement

Ensuite aller dans les equipements:

![Capture d’écran 2021-08-04 à 10 59 25](https://user-images.githubusercontent.com/8549674/128153219-7444f55b-2023-4caf-9273-bfb284ffbc0b.png)

pour créer un nouveau en lui donnant un nom:

![Capture d’écran 2021-08-04 à 10 59 49](https://user-images.githubusercontent.com/8549674/128153271-92fbb740-2ecc-4f81-9c4c-562560ce224b.png)

Rattachez le à un objet (ici: Home) et indiquez l'adresse I2C de la carte:

![Capture d’écran 2021-08-04 à 11 00 59](https://user-images.githubusercontent.com/8549674/128153425-d9c19431-601d-4f3e-83bd-88a03a2a5ffd.png)

Sauvegardez.

Le widget de controle de la carte doit maintenant être visible sur le dashboard:

![Capture d’écran 2021-08-04 à 11 02 04](https://user-images.githubusercontent.com/8549674/128153573-1034b430-5598-4d09-b17c-f5a2ff562258.png)

Vous pouvez l utiliser.

## Changelog



## Support

Ouvrez des issues dans https://github.com/KiwiHC16/abeillerelayhat_Support/issues si vous souhaitez du support.
