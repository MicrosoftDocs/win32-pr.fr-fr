---
title: Ouverture de périphériques d’entrée MIDI
description: Ouverture de périphériques d’entrée MIDI
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Interface MIDI (Musical Instrument Digital Interface), appareils d’entrée
- MIDI (Musical Instrument Digital Interface), appareils d’entrée
- enregistrement de données audio MIDI, appareils d’entrée
- Périphériques d’entrée MIDI
- Interface MIDI (Musical Instrument Digital Interface), ouverture des périphériques d’entrée
- MIDI (Musical Instrument Digital Interface), ouverture des appareils d’entrée
- enregistrement de l’audio MIDI, ouverture des appareils d’entrée
- ouverture de périphériques d’entrée MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364436"
---
# <a name="opening-midi-input-devices"></a>Ouverture de périphériques d’entrée MIDI

Pour ouvrir un appareil d’entrée MIDI pour l’enregistrement, utilisez la fonction [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) . Cette fonction ouvre l’appareil associé à l’identificateur de périphérique spécifié et retourne un descripteur de l’appareil ouvert en écrivant le handle dans un emplacement de mémoire spécifié.

si vous utilisez l' \_ indicateur d’état d’e/s MIDI \_ avec **midiInOpen**, le système utilise le message [**MIM \_ MOREDATA**](mim-moredata.md) pour alerter la fonction de rappel de votre application lorsqu’il ne traite pas les données MIDI suffisamment rapidement pour suivre le pilote de périphérique d’entrée. (le message [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md) effectue la même tâche avec les rappels de fenêtre. Toutefois, pour des raisons de performances, la plupart des applications utilisent des fonctions de rappel au lieu de rappels de fenêtre.) Si votre application traite des données MIDI dans un thread séparé, l’augmentation de la priorité du thread peut avoir un impact significatif sur la capacité de l’application à suivre le processus de données.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement d’un fichier audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 