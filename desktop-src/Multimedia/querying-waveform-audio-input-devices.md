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
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367735"
---
# <a name="querying-waveform-audio-input-devices"></a>Interrogation Waveform-Audio périphériques d’entrée

Avant d’enregistrer l’audio de la forme d’onde, vous devez appeler la fonction [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) pour déterminer les fonctionnalités d’entrée Waveform-Audio du système. Cette fonction remplit une structure [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) avec des informations sur les fonctionnalités d’un appareil spécifié. Ces informations incluent les identificateurs de fabricant et de produit, un nom de produit pour l’appareil et le numéro de version du pilote de périphérique. En outre, la structure **WAVEINCAPS** fournit des informations sur les formats audio Waveform standard pris en charge par l’appareil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement de la forme d’onde](recording-waveform-audio.md)
</dt> </dl>

 

 