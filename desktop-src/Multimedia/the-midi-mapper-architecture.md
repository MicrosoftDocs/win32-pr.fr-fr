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
ms.openlocfilehash: ba337b05fcff1bd0bb0e948e36e7d290eacb9604
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310825"
---
# <a name="the-midi-mapper-architecture"></a>Architecture du mappeur MIDI

Le Mappeur MIDI utilise une carte d’installation MIDI pour déterminer comment traduire et rediriger les messages qu’il reçoit. Une carte d’installation MIDI se compose des types de mappages suivants.

-   [Carte de canal](the-channel-map.md)
-   [Mappages de correctifs](patch-maps.md)
-   [Cartes clés](key-maps.md)

L’illustration suivante montre les rôles des cartes de canal, de correctif et de clé dans une carte d’installation MIDI.

![rôles de canaux, de correctifs et de clés dans une image de carte d’installation midi](images/mmap-a02.gif)

 

 




