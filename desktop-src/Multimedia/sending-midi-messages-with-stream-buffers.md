---
title: Envoi de messages MIDI avec des mémoires tampons de flux
description: Envoi de messages MIDI avec des mémoires tampons de flux
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- MIDI (Musical Instrument Digital Interface), mémoires tampons de flux
- lire des fichiers MIDI, mémoires tampons de flux
- mémoires tampons de flux, envoyer des messages MIDI
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- Jeux de fichiers MIDI, envoi de messages
- envoi de messages MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364499"
---
# <a name="sending-midi-messages-with-stream-buffers"></a>Envoi de messages MIDI avec des mémoires tampons de flux

Lorsque votre application fonctionne avec des tampons de flux, elle utilise la fonction [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) pour envoyer tous les messages MIDI (courts et longs) à l’appareil. Pour spécifier des blocs de données de flux, utilisez les structures [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) et [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . La structure **MIDIHDR** contient l’adresse d’un bloc de données verrouillé, la longueur du bloc de données et certains indicateurs assortis. Les données sont stockées sous la forme de structures **MIDIEVENT** . Le système impose une limite de taille de 64 Ko sur les mémoires tampons de flux.

Une fois que vous avez utilisé **midiStreamOut** pour envoyer une mémoire tampon de données de flux de données, vous devez attendre que le pilote de périphérique se termine avec le bloc de données avant de le libérer. Si vous envoyez plusieurs blocs de données, vous devez surveiller l’achèvement de chaque bloc de données afin de savoir quand envoyer des blocs supplémentaires. Pour plus d’informations sur les différentes techniques d’analyse de la saisie semi-automatique des blocs de données, consultez [gestion des blocs de données MIDI](managing-midi-data-blocks.md).

 

 