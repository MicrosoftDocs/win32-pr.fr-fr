---
title: Réception de messages Time-Stamped MIDI
description: Réception de messages Time-Stamped MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- MIDI (Musical Instrument Digital Interface), messages horodatés
- MIDI (Musical Instrument Digital Interface), messages horodatés
- enregistrement d’un fichier audio MIDI, messages horodatés
- messages MIDI horodatés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121518"
---
# <a name="receiving-time-stamped-midi-messages"></a>Réception de messages Time-Stamped MIDI

En raison du délai entre le moment où le pilote de périphérique reçoit un message MIDI et le moment où l’application reçoit le message, l’horodatage des pilotes de périphériques d’entrée MIDI est le message MIDI avec l’heure à laquelle le message a été reçu. Les horodatages MIDI, qui sont définis au moment de la réception du premier octet du message, sont spécifiés en millisecondes. La fonction [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) réinitialise les horodatages pour un appareil à zéro.

Comme indiqué précédemment, pour recevoir des horodatages avec entrée MIDI, vous devez utiliser une fonction de rappel. le paramètre *dwParam2* de la fonction de rappel spécifie l’horodatage pour les données associées aux messages [**MIM \_**](mim-data.md) et [**MIM \_ LONGDATA**](mim-longdata.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement d’un fichier audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 