---
title: Le Mappeur MIDI
description: Le Mappeur MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows multimédia, mappeur MIDI
- multimédia, Mappeur MIDI
- audio multimédia, Mappeur MIDI
- audio, Mappeur MIDI
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, à propos de
- Mappeur MIDI, source
- Mappeur MIDI, destination
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364524"
---
# <a name="the-midi-mapper"></a>Le Mappeur MIDI

Les services de correctif standard du mappeur MIDI fournissent une lecture de fichier MIDI indépendante de l’appareil pour les applications. Le Mappeur MIDI peut être utilisé avec MCI MIDI Sequencer ou avec des services de sortie MIDI de bas niveau.

Sauf indication contraire, toutes les références aux numéros de canaux MIDI utilisent les nombres de canaux logiques 1 à 16. Ces numéros de canaux logiques correspondent aux numéros de canaux physiques de 0 à 15 qui font en fait partie du message MIDI. Toutes les références aux valeurs de clé et de modification de programme MIDI utilisent les valeurs physiques 0 à 127. Tous les nombres sont décimaux sauf s’ils sont précédés du préfixe « 0x », auquel cas ils sont hexadécimaux.

Dans la discussion sur le Mappeur MIDI, le terme *source* fait référence à la partie entrée du mappeur midi. Le terme *destination* fait référence au côté sortie du mappeur midi. Par exemple, un canal source est le canal MIDI d’un message envoyé au mappeur MIDI, et un canal de destination est le canal MIDI d’un message envoyé du mappeur MIDI à un périphérique de sortie.

-   [Le Mappeur MIDI et Windows](the-midi-mapper-and-windows.md)
-   [Architecture du mappeur MIDI](the-midi-mapper-architecture.md)
-   [Carte de canal](the-channel-map.md)
-   [Cartes de correctifs](patch-maps.md)
-   [Le volume scalaire](the-volume-scalar.md)
-   [Cartes de clé](key-maps.md)
-   [résumé des Messages Cartes et MIDI](summary-of-maps-and-midi-messages.md)

 

 




