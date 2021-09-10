---
title: Interrogation des périphériques de sortie MIDI
description: Interrogation des périphériques de sortie MIDI
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- Appareil de sortie MIDI (Musical Instrument Digital Interface)
- MIDI (Musical Instrument Digital Interface), périphériques de sortie
- Jeux de fichiers MIDI, périphériques de sortie
- Périphériques de sortie MIDI
- Interface MIDI (Musical Instrument Digital Interface), interrogation des périphériques de sortie
- MIDI (Musical Instrument Digital Interface), interrogation des périphériques de sortie
- exécution de fichiers MIDI, interrogation des périphériques de sortie
- interrogation des périphériques de sortie MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292fbacbb4acf182d566e8c98832dfb0f993ea2b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364487"
---
# <a name="querying-midi-output-devices"></a>Interrogation des périphériques de sortie MIDI

Avant de lancer un fichier MIDI, vous devez utiliser la fonction [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) pour déterminer les fonctionnalités du périphérique de sortie MIDI qui est présent dans le système. Cette fonction prend une adresse d’une structure [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) , qu’elle remplit avec des informations sur les fonctionnalités de l’appareil donné. Ces informations incluent les identificateurs de fabricant et de produit, un nom de produit pour l’appareil et le numéro de version du pilote de périphérique (respectivement spécifié dans les membres **wMid**, **wPid**, **szPname** et **vDriverVersion** ).

Les périphériques de sortie MIDI peuvent être des synthétiseurs internes ou des ports de sortie MIDI externes. Le membre **wTechnology** de la structure **MIDIOUTCAPS** spécifie la technologie de l’appareil.

Si l’appareil est un synthétiseur interne, des informations supplémentaires sur l’appareil sont disponibles dans les membres **wVoices**, **wNotes** et **wChannelMask** . Le membre **wVoices** spécifie le nombre de voix que l’appareil prend en charge. Chaque voix peut avoir un son ou un timbre différent. Les voix sont organisées en canaux MIDI. Le membre **wNotes** spécifie la *polyphonie* de l’appareil, c’est-à-dire le nombre maximal de notes qui peuvent être lues simultanément. Le membre **wChannelMask** est une représentation binaire des canaux MIDI auxquels l’appareil répond. Par exemple, si l’appareil répond aux huit premiers canaux MIDI, **wChannelMask** est 0x00FF. Si l’appareil est un port de sortie externe, **wVoices** et **wNotes** sont inutilisés, et **wChannelMask** est défini sur 0xFFFF.

Le membre **dwSupport** de la structure **MIDIOUTCAPS** indique si le pilote de périphérique prend en charge les modifications de volume, la mise en cache des correctifs et la diffusion en continu. Les modifications de volume sont prises en charge uniquement par les appareils de synthétiseur internes. Les ports de sortie MIDI externes ne prennent pas en charge les modifications de volume. Pour plus d’informations sur la modification du volume, consultez [modification du volume du synthétiseur MIDI interne](changing-internal-midi-synthesizer-volume.md).

 

 