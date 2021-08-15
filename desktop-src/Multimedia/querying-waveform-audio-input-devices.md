---
title: Interrogation Waveform-Audio périphériques d’entrée
description: Interrogation Waveform-Audio périphériques d’entrée
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- audio Wave, interrogation des périphériques d’entrée
- Waveform-interface audio, interrogation des périphériques d’entrée
- enregistrement de la forme d’onde audio, interrogation des périphériques d’entrée
- interrogation des périphériques d’entrée Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd22a2b65746202a831d475fcde38b31259619dbc645a5cbca3b91d03ff6e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371921"
---
# <a name="querying-waveform-audio-input-devices"></a>Interrogation Waveform-Audio périphériques d’entrée

Avant d’enregistrer l’audio de la forme d’onde, vous devez appeler la fonction [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) pour déterminer les fonctionnalités d’entrée Waveform-Audio du système. Cette fonction remplit une structure [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) avec des informations sur les fonctionnalités d’un appareil spécifié. Ces informations incluent les identificateurs de fabricant et de produit, un nom de produit pour l’appareil et le numéro de version du pilote de périphérique. En outre, la structure **WAVEINCAPS** fournit des informations sur les formats audio Waveform standard pris en charge par l’appareil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement de la forme d’onde](recording-waveform-audio.md)
</dt> </dl>

 

 