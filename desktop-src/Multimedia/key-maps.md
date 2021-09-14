---
title: Cartes de clé
description: Cartes de clé
ms.assetid: 5d0367b0-bbf1-4a4b-98b2-dbca6f2f8b0c
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, mappages de clés
- cartes clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffafd99e6d813f12c388b633997980b7a58d62dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195220"
---
# <a name="key-maps"></a>Cartes de clé

Chaque entrée dans la table de traduction de mappage de correctifs peut être associée à un mappage de clés. Les mappages de clés affectent les messages Remarque on, note-OFF et Polyphonic-Key-aftertouch. Un mappage de clés a une table de traduction avec une entrée pour chacune des valeurs de clé MIDI 128. Par exemple, si l’entrée pour la valeur de clé 60 est 72, le Mappeur MIDI modifie les messages de note MIDI, comme indiqué dans l’illustration suivante.

![image du mappeur midi](images/mmap-a06.gif)

Les cartes clés sont utiles avec les synthétiseurs qui ont des instruments à percussion basés sur des clés avec un son de percussion particulier affecté à chaque clé. Les mappages de clés sont généralement affectés au premier correctif dans les mappages de correctifs sur les canaux à percussion (10 et 16).

 

 




