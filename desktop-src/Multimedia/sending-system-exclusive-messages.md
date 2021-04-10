---
title: Envoi de messages de System-Exclusive
description: Envoi de messages de System-Exclusive
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- MIDI (Musical Instrument Digital Interface), envoi de messages
- MIDI (Musical Instrument Digital Interface), envoi de messages
- Jeux de fichiers MIDI, envoi de messages
- envoi de messages MIDI
- MIDI (Musical Instrument Digital Interface), messages système-exclusifs
- MIDI (Musical Instrument Digital Interface), messages système-exclusifs
- exécution de fichiers MIDI, messages System-exclusive
- messages MIDI exclusifs système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842118"
---
# <a name="sending-system-exclusive-messages"></a>Envoi de messages de System-Exclusive

Les messages système exclusifs MIDI sont les seuls messages MIDI qui ne tiennent pas dans une seule valeur de mot double. Les messages exclusifs système peuvent avoir n’importe quelle longueur. Windows fournit la fonction [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) pour l’envoi de messages exclusifs système aux périphériques de sortie MIDI. Pour spécifier des blocs de données système exclusifs MIDI, utilisez la structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .

Après avoir envoyé un bloc de données System-exclusive à l’aide de **midiOutLongMsg**, vous devez attendre que le pilote de périphérique se termine avec le bloc de données avant de le libérer. Si vous envoyez plusieurs blocs de données, vous devez surveiller l’achèvement de chaque bloc de données afin de savoir quand envoyer des blocs supplémentaires. Pour plus d’informations sur les différentes techniques d’analyse de la saisie semi-automatique des blocs de données, consultez [gestion des blocs de données MIDI](managing-midi-data-blocks.md).

> [!Note]  
> Tout octet d’État MIDI autre qu’un message système en temps réel met fin à un message système exclusif. Si vous utilisez plusieurs blocs de données pour envoyer un seul message système exclusif, n’envoyez pas de messages MIDI autres que des messages du système en temps réel entre les blocs de données.

 

 

 