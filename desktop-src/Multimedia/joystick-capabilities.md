---
title: Fonctionnalités de la manette de jeu
description: Fonctionnalités de la manette de jeu
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- entrée multimédia, joysticks
- joysticks, déplacement sur deux axes
- joysticks, déplacement sur trois axes
- manettes, boutons
- joysticks, plages de mouvement
- joysticks, fréquences d’interrogation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110873"
---
# <a name="joystick-capabilities"></a>Fonctionnalités de la manette de jeu

Les manettes peuvent prendre en charge le déplacement sur deux ou trois axes et jusqu’à quatre boutons. Les joysticks prennent également en charge différentes plages de *fréquences d’interrogation* et *de mouvement* . La plage de mouvement est la distance à laquelle un handle de manette de jeu peut passer de sa position de repos à la position la plus éloignée de sa position de repos. La fréquence d’interrogation est l’intervalle de temps entre les requêtes de manette de jeu.

Les pilotes de manette de jeu peuvent prendre en charge une ou deux manettes. Vous pouvez déterminer le nombre de joysticks pris en charge par un pilote de manette de jeu à l’aide de la fonction [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) . Cette fonction retourne un entier non signé qui contient le nombre de joysticks pris en charge ou zéro s’il n’y a pas de prise en charge de la manette de jeu. La valeur de retour n’indique pas le nombre de joysticks attachés au système.

Vous pouvez déterminer si une manette de jeu est attachée au système à l’aide de la fonction [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Cette fonction retourne \_ l’erreur JOYERR si l’appareil spécifié est attaché. Sinon, elle retourne JOYERR \_ débranché.

Chaque manette de jeu offre plusieurs fonctionnalités qui sont disponibles pour votre application. Vous pouvez récupérer les fonctionnalités d’une manette de jeu à l’aide de la fonction [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) . Cette fonction remplit une structure [**JoyCaps**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) avec des fonctionnalités de manette de jeu telles que les valeurs minimale et maximale de son système de coordonnées, le nombre de boutons sur la manette de jeu et les fréquences d’interrogation minimale et maximale.

 

 