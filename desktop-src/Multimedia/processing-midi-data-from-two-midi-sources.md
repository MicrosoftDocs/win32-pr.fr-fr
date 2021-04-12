---
title: Traitement des données MIDI à partir de deux sources MIDI
description: Traitement des données MIDI à partir de deux sources MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Multimédia Windows, traitement de données MIDI à partir de deux sources
- multimédia, traitement de données MIDI à partir de deux sources
- audio multimédia, traitement de données MIDI à partir de deux sources
- audio, traitement des données MIDI à partir de deux sources
- Interface MIDI (Musical Instrument Digital Interface), traitement des données à partir de deux sources
- MIDI (Musical Instrument Digital Interface), traitement des données à partir de deux sources
- traitement des données MIDI à partir de deux sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031174"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>Traitement des données MIDI à partir de deux sources MIDI

Le sous-système MIDI peut acheminer des messages MIDI de deux sources de données vers un seul périphérique de sortie MIDI pour une lecture simultanée. Par exemple, une source peut être une musique en arrière-plan ou une ligne de basses qui a été pré-enregistrée et stockée dans un fichier. La deuxième source peut être des données en temps réel à partir d’un instrument MIDI, tel qu’un clavier ou une guitare.

Les deux sources de données envoient des données MIDI à un seul appareil MIDI identifié avec un seul descripteur. Envoyer un flux de données à l’aide de la fonction [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) et d’une ou plusieurs mémoires tampons de flux. Ce flux de données contient généralement des données préenregistrées qui sont compressées dans la mémoire tampon.

Envoyez le deuxième flux de données (généralement à partir d’un instrument MIDI) de façon asynchrone à l’aide de la fonction [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) . L’état d’exécution d’une mémoire tampon de flux n’est pas affecté par les appels asynchrones effectués par le deuxième flux de données.

Chaque message bref envoyé avec **midiOutShortMsg** doit être un message MIDI complet, avec un octet d’État et le nombre approprié d’octets de données. Si l’octet d’État est omis, **midiOutShortMsg** retourne une erreur. (Toutefois, il n’y a pas d’État en cours d’exécution avec la sortie du flux.)

 

 