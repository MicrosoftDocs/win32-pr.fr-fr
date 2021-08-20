---
title: Position de la manette de jeu
description: Position de la manette de jeu
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- joysticks, position
- manettes, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e5664166d20f9195a33d03534f792a4262b291bc3db34194fd05e06681563a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140303"
---
# <a name="joystick-position"></a>Position de la manette de jeu

Vous pouvez interroger une manette de jeu pour obtenir des informations sur la position et le bouton à l’aide de la fonction [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) . Par exemple, une application peut interroger la manette de jeu à la recherche de valeurs de position de ligne de base. La feuille de propriétés du panneau de configuration de la manette de jeu utilise cette technique lors de l’étalonnage du joystick.

Vous pouvez également interroger une manette de jeu ou un autre appareil disposant de fonctionnalités étendues à l’aide de la fonction [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .

 

 