---
title: Modification du volume de Audio-Devices auxiliaires
description: Modification du volume de Audio-Devices auxiliaires
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- audio Wave, modification du volume du périphérique audio auxiliaire
- modification du volume du périphérique audio auxiliaire
- audio auxiliaire, modification du volume de l’appareil
- interface audio auxiliaire
- périphériques audio auxiliaires, modification du volume
- audio auxiliaire, interface
- audio auxiliaire, appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02ca4ceaf8e8a8b2f84ea69be437145f0f92b375904a0121c17abc7870fa831
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808109"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a>Modification du volume de Audio-Devices auxiliaires

Windows fournit les fonctions suivantes pour interroger et définir le volume des périphériques audio auxiliaires.



| Fonction                             | Description                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | Récupère le paramètre de volume actuel du périphérique de sortie auxiliaire spécifié. |
| [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | Définit le volume du périphérique de sortie auxiliaire spécifié.                      |



 

Tous les périphériques audio auxiliaires ne prennent pas en charge les modifications de volume. Certains appareils peuvent prendre en charge des modifications de volume individuelles sur les canaux gauche et droit.

Le volume est spécifié dans une valeur de mot double, comme avec les fonctions Wave-audio et de contrôle de volume MIDI. Lorsque le format audio est stéréo, les 16 bits supérieurs spécifient le volume relatif du canal droit et les 16 bits inférieurs spécifient le volume relatif du canal de gauche. Pour les appareils qui ne prennent pas en charge le contrôle du volume de canal droit et gauche, les 16 bits de poids faible spécifient le niveau de volume et les 16 bits supérieurs sont ignorés.

Les valeurs au niveau du volume sont comprises entre 0x0 (silence) et 0xFFFF (volume maximal) et sont interprétées de façon logarithmique. L’augmentation du volume perçu est la même lors de l’augmentation du niveau de volume de 0x5000 à 0x6000, comme c’est le cas de 0x4000 à 0x5000.

 

 