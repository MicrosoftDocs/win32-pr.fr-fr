---
title: Périphériques DirectInput et XUSB
description: le pilote de la classe XUSB (Xbox Common Controller class) sur Windows implémente l’interface en mode noyau pour la DLL XINPUT.
ms.assetid: 8bf47b07-a1b6-7721-2136-3853e72c71ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f06bb814fcf7a4eeffe76258f3f5689512cba60ca2e517ec7f0cff9870f353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926369"
---
# <a name="directinput-and-xusb-devices"></a>Périphériques DirectInput et XUSB

le pilote de la classe XUSB (Xbox Common Controller class) sur Windows implémente l’interface en mode noyau pour la DLL XINPUT. Pour fournir une bonne expérience pour les titres hérités qui utilisent l’API [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) avec l’appareil de contrôleur commun, le pilote exporte également une interface de classe HID (Human Interface Device), qui est récupérée par DirectInput. Nous avons choisi le mappage de XUSB à HID en fonction d’un comportement classique dans un ensemble d’applications de jeu pour la version d’origine de XINPUT, et nous avons mis à jour le mappage des sous-types plus récents. Cette rubrique décrit le mappage.

## <a name="human-interface-device-hid"></a>Périphérique d’interface utilisateur (HID)

Le standard HID est une norme du Comité USB (Universal Serial Bus) proposé à l’origine par Microsoft pour généraliser les protocoles des périphériques d’entrée. Il se compose d’un langage de description de code octet et peut exprimer des boîtiers, des souris, des joysticks, des accélérateurs et des commandes de gouvernail, ainsi que des contrôleurs à plusieurs axes. Étant donné que cette norme est si généralisée, il se peut que vous ayez des difficultés à écrire des logiciels qui consomment des entrées provenant d’appareils arbitraires. Par conséquent, pour l’API [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) axée sur les jeux, nous avons développé un sous-mappage spécifique de types pour encourager les fabricants de matériel à prendre en charge via leurs pilotes.

- [Définition de classe de périphérique USB pour HID v 1.11](https://www.usb.org/document-library/device-class-definition-hid-111)

> [!Important]
> Vous pouvez également accéder aux périphériques d’entrée HID via l' [API RawInput](../inputdev/about-raw-input.md) et traiter les rapports d’entrée via une [API HID](/windows-hardware/drivers/hid/introduction-to-hid-concepts) de bas niveau, mais les commentaires sur les vibrations ne fonctionneront pas comme avec [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="mappings"></a>Mappages

Le pilote XUSB implémente une interface de classe XUSB et une interface de classe HID pour les périphériques afin de prendre en charge à la fois l’utilisation de XINPUT et de [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) . Ce mappage est basé sur les informations de sous-type XUSB. Le pilote implémente quatre groupes distincts de mappages.

| Sous-type XUSB                                      | Mappage                     |
|---------------------------------------------------|-----------------------------|
| \_Boîtier XInput DEVSUBTYPE \_ (sous-type 1)           | Boîtier de commande                     |
| XINPUT \_ DEVSUBTYPE \_ Wheel (sous-type 2)             | Roulette                       |
| XINPUT \_ DEVSUBTYPE \_ arcade \_ Stick (sous-type 3)     | Boîtier de l’arcade/arcade     |
| XINPUT \_ DEVSUBTYPE \_ Flight \_ Stick (sous-type 4)     | Manche                |
| XINPUT \_ DEVSUBTYPE \_ danse \_ (sous-type 5)        | Valeur par défaut pour tout nouveau sous-type |
| XINPUT \_ DEVSUBTYPE \_ guitare (sous-type 6)            | Guitare                      |
| \_Alternative XInput DEVSUBTYPE \_ guitare \_ (sous-type 7) |                             |
| \_ \_ Kit tambour XInput DEVSUBTYPE \_ (sous-type 8)         |                             |
| XINPUT \_ DEVSUBTYPE \_ guitare \_ Bass (sous-type 11)     |                             |
| XINPUT \_ DEVSUBTYPE \_ arcade \_ (sous-type 19)      |                             |

> [!Note]  
> Les mappages HID suivants sont statiques. Cela signifie que même si le rapport des fonctionnalités de l’appareil indique qu’un bouton ou un axe spécifique n’est pas pris en charge, le mappage l’inclura toujours, mais signalera toujours un état désactivé ou une valeur centrale.

## <a name="gamepad"></a>Boîtier de commande

Il s’agit du mappage par défaut qui est conçu autour du boîtier de commande standard Xbox Common Controller, et il est exposé en tant que type d’utilisation HID de *boîtier* de commande.

| Contrôler                      | Nom d’utilisation HID | Page utilisation | ID d’utilisation   |
|------------------------------|----------------|------------|------------|
| Stick gauche                   | X, Y           | 0x01       | 0x30, 0x31 |
| Stick droite                  | RX, Ry         | 0x01       | 0x33, 0x34 |
| Déclencheur gauche + déclencheur droit | Z\*            | 0x01       | 0x32       |
| Touche D-haut, vers le haut, gauche, droite  | Commutateur Hat     | 0x01       | 0x39       |
| A                            | Bouton 1       | 0x09       | 0x01       |
| B                            | Bouton 2       | 0x09       | 0x02       |
| X                            | Bouton 3       | 0x09       | 0x03       |
| O                            | Bouton 4       | 0x09       | 0x04       |
| LB (embosseur gauche)             | Bouton 5       | 0x09       | 0x05       |
| RB (contre-choc droit)            | Bouton 6       | 0x09       | 0x06       |
| RETOUR                         | Bouton 7       | 0x09       | 0x07       |
| ÉCRAN D’ACCUEIL                        | Bouton 8       | 0x09       | 0x08       |
| LSB (bouton stick gauche)      | Bouton 9       | 0x09       | 0x09       |
| RSB (bouton en forme de levier droit)     | Bouton 10      | 0x09       | 0x0A       |

> [!Note]  
> ( \* ) : Ceci est combiné afin que Z affiche le comportement de centrage attendu par la plupart des titres pour la rotation. cela signifie qu’il n’est pas possible de voir toutes les valeurs de combinaison possibles via [DIRECTINPUT](/previous-versions/windows/desktop/ee416842(v=vs.85)) et HID.

## <a name="arcade-stickarcade-pad"></a>Boîtier de l’arcade/arcade

Il s’agit du mappage conçu autour du contrôleur Arcade Stick. il est exposé en tant que type d’utilisation HID de *boîtier* de commande. La tablette arcade est très similaire à un bâton d’arcade, mais dans un plus petit facteur de forme. Ces conceptions remplacent le déclencheur analogique gauche et le déclencheur de droite par des boutons numériques qui indiquent la valeur minimale et maximale de l’axe.

| Contrôler                     | Nom d’utilisation HID | Page utilisation | ID d’utilisation |
|-----------------------------|----------------|------------|----------|
| Touche D-haut, vers le haut, gauche, droite | Commutateur Hat     | 0x01       | 0x39     |
| A                           | Bouton 1       | 0x09       | 0x01     |
| B                           | Bouton 2       | 0x09       | 0x02     |
| X                           | Bouton 3       | 0x09       | 0x03     |
| O                           | Bouton 4       | 0x09       | 0x04     |
| LB (embosseur gauche)            | Bouton 5       | 0x09       | 0x05     |
| RB (contre-choc droit)           | Bouton 6       | 0x09       | 0x06     |
| RETOUR                        | Bouton 7       | 0x09       | 0x07     |
| ÉCRAN D’ACCUEIL                       | Bouton 8       | 0x09       | 0x08     |
| Déclencheur gauche                | Bouton 9       | 0x09       | 0x09     |
| Déclencheur droit               | Bouton 10      | 0x09       | 0x0A     |

Ces appareils peuvent ou non prendre en charge des contrôles supplémentaires, mais ceux-ci ne sont pas exposés par le mappage HID : Left Stick, Right Stick, LSB (bouton gauche Stick) et RSB (bouton Stick à droite).

## <a name="wheel"></a>Roulette

Ce mappage est conçu à travers la roue de course Xbox et est exposé en tant que type d’utilisation HID de *boîtier* de commande.

| Contrôler                                                        | Nom d’utilisation HID | Page utilisation | ID d’utilisation |
|----------------------------------------------------------------|----------------|------------|----------|
| Roue (Stick X gauche)                                           | X              | 0x01       | 0x30     |
| Pédale d’accélérateur (déclencheur de droite) + pédale de frein (déclencheur gauche) | Z\*            | 0x01       | 0x32     |
| Touche D-haut, vers le haut, gauche, droite                                    | Commutateur Hat     | 0x01       | 0x39     |
| A                                                              | Bouton 1       | 0x09       | 0x01     |
| B                                                              | Bouton 2       | 0x09       | 0x02     |
| X                                                              | Bouton 3       | 0x09       | 0x03     |
| O                                                              | Bouton 4       | 0x09       | 0x04     |
| LB (embosseur gauche)                                               | Bouton 5       | 0x09       | 0x05     |
| RB (contre-choc droit)                                              | Bouton 6       | 0x09       | 0x06     |
| LSB (bouton stick gauche)                                        | Bouton 7       | 0x09       | 0x07     |
| RSB (bouton en forme de levier droit)                                       | Bouton 8       | 0x09       | 0x08     |
| RETOUR                                                           | Bouton 9       | 0x09       | 0x09     |
| ÉCRAN D’ACCUEIL                                                          | Bouton 10      | 0x09       | 0x0A     |

> [!Note]  
> ( \* ) : Ceci est combiné de sorte que Z présente le comportement de centrage attendu par la plupart des titres pour les contrôles de frein et d’accélérateur ; cela signifie qu’il n’est pas possible de voir toutes les valeurs de combinaison de pédales possibles via [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="flight-stick"></a>Manche

Ce mappage est conçu autour du manche de avion Xbox et est exposé comme un type d’utilisation HID de *manette* de jeu.

| Contrôler                     | Nom de l’utilisation | Page utilisation | ID d’utilisation   |
|-----------------------------|------------|------------|------------|
| Volant de vol (stick gauche)   | X, Y       | 0x01       | 0x30, 0x31 |
| Bouton PDV (droite)       | RX, Ry     | 0x01       | 0x33, 0x34 |
| Limitation (déclencheur Right)    | Z          | 0x01       | 0x32       |
| Gouvernail (déclencheur gauche)       | Rz         | 0x01       | 0x35       |
| Touche D-haut, vers le haut, gauche, droite | Commutateur Hat | 0x01       | 0x39       |
| Arme principale (A)          | Bouton 1   | 0x09       | 0x01       |
| Arme secondaire (B)        | Bouton 2   | 0x09       | 0x02       |
| X                           | Bouton 3   | 0x09       | 0x03       |
| O                           | Bouton 4   | 0x09       | 0x04       |
| LB (embosseur gauche)            | Bouton 5   | 0x09       | 0x05       |
| RB (contre-choc droit)           | Bouton 6   | 0x09       | 0x06       |
| RETOUR                        | Bouton 7   | 0x09       | 0x07       |
| ÉCRAN D’ACCUEIL                       | Bouton 8   | 0x09       | 0x08       |
| LSB (bouton stick gauche)     | Bouton 9   | 0x09       | 0x09       |
| RSB (bouton en forme de levier droit)    | Bouton 10  | 0x09       | 0x0A       |

> [!Note]  
> Cela est basé sur la conception finale du bâton de vol. Étant donné que cela diffère des premières définitions du Memory Stick, de nombreux appareils disposent d’un commutateur de mode qui prend en charge l’ancien et le nouveau modèle. Ce mappage suppose le nouveau modèle.