---
title: Modification du volume de Waveform-Audio lecture
description: Modification du volume de Waveform-Audio lecture
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- audio Wave, modification du volume de lecture
- Waveform-interface audio, modification du volume de lecture
- audio Wave, volume de lecture
- Waveform-interface audio, volume de lecture
- modification du volume de lecture Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59bca6dbc168d2c327c46e4d934d4abb3afa73cc8ef2cae8b1a6c283bd92c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807989"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a>Modification du volume de Waveform-Audio lecture

Windows fournit les fonctions suivantes pour interroger et définir le niveau de volume des périphériques de sortie waveform-audio.



| Fonction                                     | Description                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | Récupère le niveau de volume actuel du périphérique de sortie Waveform-Audio spécifié. |
| [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | Définit le niveau de volume du périphérique de sortie Wave-audio spécifié.              |



 

Tous les périphériques audio Waveform ne prennent pas en charge les modifications de volume. Certains périphériques prennent en charge le contrôle de volume individuel sur les canaux gauche et droit. Pour plus d’informations sur la façon de déterminer les capacités de contrôle de volume des périphériques Wave-audio, consultez [périphériques et types de données](devices-and-data-types.md).

Certaines applications permettent à l’utilisateur de contrôler le volume de tous les périphériques audio d’un système. (De nombreuses applications de ce type utilisent les services de mixage audio. pour plus d’informations, consultez [mixages audio](audio-mixers.md)). À moins que votre application ne soit en capacité de prendre en charge ce type de contrôle de volume principal, vous devez ouvrir un périphérique audio avant de modifier son volume. Vous devez également interroger le niveau de volume avant de le modifier et restaurer le niveau de volume précédent le plus rapidement possible.

Le volume est spécifié dans une valeur de mot double. Lorsque le format audio est stéréo, les 16 bits supérieurs spécifient le volume relatif du canal droit et les 16 bits inférieurs spécifient le volume relatif du canal de gauche. Pour les appareils qui ne prennent pas en charge le contrôle du volume de canal droit et gauche, les 16 bits de poids faible spécifient le niveau de volume et les 16 bits supérieurs sont ignorés.

Les valeurs au niveau du volume sont comprises entre 0x0 (silence) et 0xFFFF (volume maximal) et sont interprétées de façon logarithmique. L’augmentation du volume perçu est la même lors de l’augmentation du niveau de volume de 0x5000 à 0x6000, comme c’est le cas de 0x4000 à 0x5000.

 

 