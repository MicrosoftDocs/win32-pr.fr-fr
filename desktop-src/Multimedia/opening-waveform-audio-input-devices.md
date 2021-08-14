---
title: Ouverture de Waveform-Audio périphériques d’entrée
description: Ouverture de Waveform-Audio périphériques d’entrée
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- sons Waveform, ouverture des périphériques d’entrée
- Waveform-interface audio, ouverture des périphériques d’entrée
- enregistrement de la forme d’onde audio, ouverture des appareils d’entrée
- ouverture de périphériques d’entrée Waveform-Audio
- waveInOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6391ca5bfe0690d2235504057865fb588f08d0359417ccbcc04b6a7e5eb082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802306"
---
# <a name="opening-waveform-audio-input-devices"></a>Ouverture de Waveform-Audio périphériques d’entrée

Utilisez la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) pour ouvrir un appareil d’entrée Waveform-Audio pour l’enregistrement. Cette fonction ouvre l’appareil associé à l’identificateur de périphérique spécifié et retourne un handle de l’appareil ouvert en écrivant le handle d’un emplacement de mémoire spécifié.

Certains ordinateurs multimédias possèdent plusieurs périphériques d’entrée Waveform-Audio. À moins que vous ne sachiez que vous souhaitez ouvrir un périphérique d’entrée Wave-Audio spécifique dans un système, vous devez utiliser la \_ constante du mappeur Wave pour l’identificateur de l’appareil lorsque vous ouvrez un appareil. La fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) choisit l’appareil dans le système le plus approprié pour enregistrer le format de données spécifié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement de la forme d’onde](recording-waveform-audio.md)
</dt> </dl>

 

 