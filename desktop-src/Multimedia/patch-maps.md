---
title: Cartes de correctifs
description: Cartes de correctifs
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, mappages de correctifs
- mappages de correctifs
- Programme MIDI-modification des messages
- Messages du contrôleur de volume MIDI
- programme-modifier les messages
- messages du contrôleur de volume
- Mappeur MIDI, messages de modification de programme
- Mappeur MIDI, messages de contrôleur de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110869"
---
# <a name="patch-maps"></a>Cartes de correctifs

Chaque entrée de mappage de canal peut être associée à une carte de correctif. Les mappages de correctifs affectent les messages de modification de programme MIDI et de contrôleur de volume. Programme : les messages de modification indiquent à un synthétiseur de modifier le son de l’instrument (patch) pour un canal spécifié. Les messages du contrôleur de volume définissent le volume d’un canal.

Une carte de correctifs possède une table de traduction avec une entrée pour chacune des valeurs de modification de programme 128. Chaque mappage de correctif spécifie les éléments suivants :

-   Une valeur de changement de programme de destination.
-   Scalaire de volume. (Pour plus d’informations, consultez [volume Scalar](the-volume-scalar.md).)
-   Mappage de clé facultatif. (pour plus d’informations, consultez [Key Cartes](key-maps.md).)

Lorsque le Mappeur MIDI reçoit des messages de modification de programme, la valeur de modification du programme de destination est remplacée par la valeur de modification du programme dans le message. Par exemple, si la valeur de modification du programme de destination pour le programme-modification 16 est 18, le Mappeur MIDI modifie le message MIDI de modification de programme comme indiqué dans l’illustration suivante.

![image du mappeur midi](images/mmap-a03.gif)

 

 




