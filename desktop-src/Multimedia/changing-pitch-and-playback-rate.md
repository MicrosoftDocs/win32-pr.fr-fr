---
title: Modification du pas et de la vitesse de lecture
description: Modification du pas et de la vitesse de lecture
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- sons Waveform, pas de tonalité
- Waveform-interface audio, inclinaison
- audio Wave, vitesse de lecture
- Waveform-interface audio, vitesse de lecture
- son de forme d’onde, modification du pas
- Waveform-interface audio, modification du pas
- audio Wave, modification de la vitesse de lecture
- Waveform-interface audio, modification de la vitesse de lecture
- modification de la vitesse de lecture Waveform-Audio
- modification du ton de la forme d’onde-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367612"
---
# <a name="changing-pitch-and-playback-rate"></a>Modification du pas et de la vitesse de lecture

Certains périphériques de sortie Waveform-Audio peuvent varier le pas et la vitesse de lecture des données audio Waveform. Tous les périphériques audio Waveform ne prennent pas en charge la tonalité et les changements de vitesse de lecture. Pour plus d’informations sur la façon de déterminer si un périphérique Wave-Audio particulier prend en charge les changements de taux de lecture et de tonalité, consultez [périphériques et types de données](devices-and-data-types.md).

Les différences entre la variation du pas et la vitesse de lecture sont les suivantes :

-   La modification de la vitesse de lecture est effectuée par le pilote de périphérique et ne nécessite pas de matériel spécialisé. Le taux d’échantillonnage n’est pas modifié, mais le pilote interpole en ignorant ou en synthétisant les exemples. Par exemple, si la vitesse de lecture est modifiée par un facteur de deux, le pilote ignore chaque autre échantillon.
-   La modification du pas à pas nécessite un matériel spécialisé. La vitesse de lecture et le taux d’échantillonnage ne sont pas modifiés.

Windows fournit les fonctions suivantes pour interroger et définir le taux de lecture et le ton de la forme d’onde audio.



| Fonction                                                 | Description                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | Récupère le pas du périphérique de sortie Waveform-Audio spécifié.         |
| [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | Récupère la vitesse de lecture pour le périphérique de sortie Waveform-Audio spécifié. |
| [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | Définit le pas du périphérique de sortie Waveform-Audio spécifié.              |
| [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | Définit la vitesse de lecture pour le périphérique de sortie Waveform-Audio spécifié.      |



 

Les taux de pas et de lecture sont modifiés par un facteur spécifié avec un nombre à virgule fixe compacté dans une valeur de mot double. Les 16 bits supérieurs spécifient la partie entière du nombre ; les 16 bits de poids faible spécifient la partie fractionnaire. Par exemple, la valeur 1,5 est représentée sous la forme 0x00018000L. La valeur 0,75 est représentée sous la forme 0x0000C000L. Une valeur de 1,0 (0x00010000) signifie que le pas à pas ou la vitesse de lecture est inchangée.

 

 