---
title: Mixer Requêtes d’appareil
description: Mixer Requêtes d’appareil
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- audio multimédia, requêtes d’appareil de mixage
- audio, requêtes d’appareil de mixage
- mixages audio, requêtes d’appareil
- mixages, requêtes d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369199"
---
# <a name="mixer-device-queries"></a>Mixer Requêtes d’appareil

Les services de mixage fournissent des fonctions permettant de déterminer le nombre d’appareils de mixage présents dans le système et les fonctionnalités des appareils. Vous pouvez également utiliser une fonction de service de mixage pour déterminer l’identificateur d’appareil pour un appareil de mixage.

Vous pouvez utiliser la fonction [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) pour déterminer le nombre de périphériques de mixage présents dans le système. les appareils Mixer sont identifiés par un identificateur d’appareil. Les identificateurs d’appareil sont déterminés implicitement à partir du nombre d’appareils présents dans un système donné. Elles sont comprises entre zéro et un de moins que le nombre d’appareils présents.

Avant d’utiliser un appareil de mixage, vous devez déterminer ses fonctionnalités. Les fonctionnalités audio peuvent varier d’un ordinateur multimédia à un autre, de sorte que les applications doivent fonctionner avec un large éventail de matériel audio.

Vous pouvez utiliser la fonction [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) pour déterminer les fonctionnalités des appareils de mixage. Cette fonction remplit une structure [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) avec des informations sur les fonctionnalités d’un appareil spécifié.

La fonction [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) récupère l’identificateur d’appareil de mixage audio associé à un handle de périphérique spécifié. Par exemple, vous pouvez utiliser cette fonction pour récupérer l’identificateur d’appareil pour un mélangeur audio, puis utiliser l’identificateur d’appareil pour ajuster le volume ou pour afficher un autre contrôle.

 

 