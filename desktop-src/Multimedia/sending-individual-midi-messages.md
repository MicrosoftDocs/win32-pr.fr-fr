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
ms.openlocfilehash: 5473d1ab7361c26a922683ed7d5021995b0f13ea
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106545743"
---
# <a name="sending-individual-midi-messages"></a>Envoi de messages MIDI individuels

Vous pouvez utiliser des messages MIDI individuels à l’aide des fonctions suivantes.



| Valeur                                      | Signification                                                                                                                                                                             |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)   | Envoie une mémoire tampon de données MIDI au périphérique de sortie MIDI spécifié. Utilisez cette fonction pour envoyer des messages système-exclusifs à un appareil MIDI.                                              |
| [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)       | Désactive toutes les notes sur tous les canaux pour un périphérique de sortie MIDI spécifié. Les mémoires tampons de flux et les mémoires tampons de flux System-exclusive en attente sont marquées comme terminées et retournées à l’application. |
| [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) | Envoie un message MIDI à un appareil de sortie MIDI spécifié.                                                                                                                             |



 

Pour envoyer un message MIDI (à l’exception des messages système exclusifs), utilisez [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg).

 

 