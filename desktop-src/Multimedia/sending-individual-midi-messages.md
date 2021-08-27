---
title: Envoi de messages MIDI individuels
description: Envoi de messages MIDI individuels
ms.assetid: 9e5b7194-d6d0-40a6-b8c1-ea9442f34bd8
keywords:
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- Jeux de fichiers MIDI, envoi de messages
- envoi de messages MIDI
- MIDI (Musical Instrument Digital Interface), messages individuels
- MIDI (Musical Instrument Digital Interface), messages individuels
- Jeux de fichiers MIDI, messages individuels
- messages MIDI individuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1f73d0956004f90644ce2e8b0e41b368137a7b61fd04e6d17302619980336d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037449"
---
# <a name="sending-individual-midi-messages"></a>Envoi de messages MIDI individuels

Vous pouvez utiliser des messages MIDI individuels à l’aide des fonctions suivantes.



| Valeur                                      | Signification                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Envoie une mémoire tampon de données MIDI au périphérique de sortie MIDI spécifié. Utilisez cette fonction pour envoyer des messages système-exclusifs à un appareil MIDI.                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Désactive toutes les notes sur tous les canaux pour un périphérique de sortie MIDI spécifié. Les mémoires tampons de flux et les mémoires tampons de flux System-exclusive en attente sont marquées comme terminées et retournées à l’application. |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Envoie un message MIDI à un appareil de sortie MIDI spécifié.                                                                                                                             |



 

Pour envoyer un message MIDI (à l’exception des messages système exclusifs), utilisez [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).

 

 