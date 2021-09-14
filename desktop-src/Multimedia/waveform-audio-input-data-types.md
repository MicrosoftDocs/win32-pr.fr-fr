---
title: Types de données d’entrée Waveform-Audio
description: Types de données d’entrée Waveform-Audio
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- audio Waveform, types de données d’entrée
- Waveform-interface audio, types de données d’entrée
- enregistrement de l’audio de forme d’onde, types de données d’entrée
- Handle HWAVEIN
- WAVEFORMATEX, structure
- WAVEHDR, structure
- WAVEINCAPS, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011705"
---
# <a name="waveform-audio-input-data-types"></a>Types de données d’entrée Waveform-Audio

Les types de données suivants sont définis pour les fonctions d’entrée Waveform-Audio.



| Type                                 | Description                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEIN**                          | Handle d’un périphérique d’entrée Waveform-Audio ouvert.                                                                                                                  |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Structure qui spécifie les formats de données pris en charge par un périphérique d’entrée Waveform-Audio particulier. Cette structure est également utilisée pour les périphériques de sortie Waveform-Audio. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Structure utilisée comme en-tête d’un bloc de données d’entrée Waveform Audio. Cette structure est également utilisée pour les périphériques de sortie Waveform-Audio.                             |
| [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | Structure utilisée pour se renseigner sur les fonctionnalités d’un périphérique d’entrée Waveform-Audio particulier.                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement de la forme d’onde](recording-waveform-audio.md)
</dt> </dl>

 

 