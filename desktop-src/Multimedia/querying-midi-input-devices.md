---
title: Interrogation des périphériques d’entrée MIDI
description: Interrogation des périphériques d’entrée MIDI
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Interface MIDI (Musical Instrument Digital Interface), appareils d’entrée
- MIDI (Musical Instrument Digital Interface), appareils d’entrée
- enregistrement de données audio MIDI, appareils d’entrée
- Périphériques d’entrée MIDI
- Interface MIDI (Musical Instrument Digital Interface), interrogation des périphériques d’entrée
- MIDI (Musical Instrument Digital Interface), interrogation des périphériques d’entrée
- enregistrement d’un fichier audio MIDI, interrogation d’appareils d’entrée
- interrogation des périphériques d’entrée MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81340f767c1ef3acf3105f78d2cef000f7548361b387e6887ecc4136437dbe6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371931"
---
# <a name="querying-midi-input-devices"></a>Interrogation des périphériques d’entrée MIDI

Avant d’enregistrer l’audio MIDI, vous devez utiliser la fonction [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) pour déterminer les fonctionnalités de l’appareil d’entrée MIDI qui est présent dans le système. Cette fonction prend une adresse d’une structure [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) , qu’elle remplit avec des informations sur les fonctionnalités de l’appareil donné. Ces informations incluent les identificateurs de fabricant et de produit, un nom de produit pour l’appareil et le numéro de version du pilote de périphérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement d’un fichier audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 