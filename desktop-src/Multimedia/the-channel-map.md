---
title: Carte de canal
description: Carte de canal
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, mappage de canal
- carte de canal
- Mappeur MIDI, messages de canal
- Messages de canal MIDI
- messages de canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87027c74ebddea9b51545d15bfa90e52dee95a8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364536"
---
# <a name="the-channel-map"></a>Carte de canal

Le mappage de canal affecte tous les messages de canal MIDI. Les messages de canaux MIDI incluent les messages de Remarque on, de note de Polyphonic-Key-aftertouch, de contrôle-modification, de modification de programme, de canal aftertouch et de modification de la courbure. Le Mappeur MIDI utilise un mappage de canal unique avec une entrée pour chacun des 16 canaux MIDI. Chaque entrée de mappage de canal spécifie les éléments suivants :

-   Canal de destination pour le message MIDI
-   Périphérique de sortie de destination pour le message MIDI
-   Carte de correctif facultative spécifiant d’autres modifications possibles pour le message MIDI

Le canal de destination est défini sur l’un des 16 canaux MIDI. Les messages MIDI sont modifiés pour refléter chaque nouvelle attribution de canal. Par exemple, si l’entrée de canal de destination pour MIDI Channel 4 est définie sur 6, tous les messages MIDI envoyés vers Channel 4 sont mappés à Channel 6, comme indiqué dans l’illustration suivante.

![image midi mappée](images/mmap-a05.gif)

Dans cet exemple, l’octet d’État MIDI 0x93 est mappé à 0x95. Le poids faible d’un octet d’État MIDI spécifie le numéro de canal. Les canaux source sont activés ou inactifs. Les messages envoyés aux canaux sources inactifs sont ignorés. un canal inactif est donc en effet muet ou désactivé.

L’appareil de sortie de destination est défini sur l’un des périphériques de sortie MIDI disponibles. Un périphérique de sortie MIDI peut être un synthétiseur interne ou un port de sortie MIDI physique.

Les messages système MIDI sont des messages MIDI (avec octets d’État) de 0xF0 à 0xFF. Il n’existe aucun canal associé aux messages système MIDI, ils ne peuvent donc pas être mappés. Les messages système MIDI sont envoyés à tous les périphériques de sortie MIDI répertoriés dans une carte de canal.

 

 




