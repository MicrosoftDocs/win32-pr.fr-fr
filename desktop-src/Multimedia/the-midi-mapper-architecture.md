---
title: Architecture du mappeur MIDI
description: Architecture du mappeur MIDI
ms.assetid: d08d1442-bf9f-46bb-bd44-f512ff4b6bd5
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, architecture
- Mappeur MIDI, plan d’installation
- Carte d’installation MIDI
- Mappeur MIDI, mappage de canal
- Mappeur MIDI, mappages de correctifs
- Mappeur MIDI, mappages de clés
- carte de canal
- mappages de correctifs
- cartes clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a20e73c9a361487468870698d3c36d59ef35bb6a28da1b03957dd24f1d7b7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136400"
---
# <a name="the-midi-mapper-architecture"></a>Architecture du mappeur MIDI

Le Mappeur MIDI utilise une carte d’installation MIDI pour déterminer comment traduire et rediriger les messages qu’il reçoit. Une carte d’installation MIDI se compose des types de mappages suivants.

-   [Carte de canal](the-channel-map.md)
-   [Cartes de correctifs](patch-maps.md)
-   [Cartes de clé](key-maps.md)

L’illustration suivante montre les rôles des cartes de canal, de correctif et de clé dans une carte d’installation MIDI.

![rôles de canaux, de correctifs et de clés dans une image de carte d’installation midi](images/mmap-a02.gif)

 

 




