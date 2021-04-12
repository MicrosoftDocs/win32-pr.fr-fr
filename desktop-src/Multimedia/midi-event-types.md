---
title: Types d’événements MIDI
description: Types d’événements MIDI
ms.assetid: 0b0984b7-3087-461e-90f2-a899dc1a88c6
keywords:
- MIDI (Musical Instrument Digital Interface), types d’événements
- MIDI (Musical Instrument Digital Interface), types d’événements
- MIDIEVENT, structure
- mémoires tampons de flux, types d’événements MIDI
- Types d’événements MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823ce5ce7af898ca3178e0379fb814c54fbf06b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031219"
---
# <a name="midi-event-types"></a>Types d’événements MIDI

Le membre **dwEvent** de la structure [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) décrit l’événement midi qui doit avoir lieu. Les événements courts s’inscrivent entièrement dans ce membre. Les événements longs requièrent une ou plusieurs valeurs de mot double en plus du membre **dwEvent** pour stocker les descriptions des événements.

L’octet de poids fort du membre **dwEvent** contient des informations indiquant si l’événement est long ou bref et si un rappel est généré avec l’événement. En outre, cet octet est utilisé pour décrire le type d’événement. Les 24 bits restants du membre **dwEvent** sont utilisés pour contenir les paramètres d’événement (pour les messages courts) ou pour contenir la longueur des paramètres d’événement (pour les messages longs). Pour extraire des informations du membre **dwEvent** , utilisez les macros [**MEVT \_ eventType**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype) et [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm) .

Pour obtenir une description des types d’événements prédéfinis, consultez la documentation de référence de la structure **MIDIEVENT** .

 

 