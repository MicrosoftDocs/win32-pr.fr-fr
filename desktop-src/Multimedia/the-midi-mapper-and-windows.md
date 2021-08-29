---
title: Le Mappeur MIDI et Windows
description: Le Mappeur MIDI et Windows
ms.assetid: a077f935-e085-4148-9975-7926ac018f0c
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024a3ce675677df8fa1bfcf32f4fdf4e6bdcae921cc14c7ccb42d6fe832480e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805112"
---
# <a name="the-midi-mapper-and-windows"></a>Le Mappeur MIDI et Windows

Le Mappeur MIDI fait partie du logiciel système. L’illustration suivante montre comment le Mappeur MIDI se réfère à d’autres éléments des services audio.

![relation entre le Mappeur midi et les autres éléments de l’image des services audio](images/mmap-a01.gif)

Du point de vue d’une application, le Mappeur MIDI ressemble à un autre périphérique de sortie MIDI. Le Mappeur MIDI reçoit les messages qui lui sont envoyés par les fonctions de sortie MIDI de bas niveau [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) et [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg). Le Mappeur MIDI modifie ces messages et les redirige vers un périphérique de sortie MIDI en fonction de la carte d’installation MIDI en cours. La carte d’installation MIDI active est sélectionnée par l’utilisateur au moyen de l’option du panneau de configuration MIDI. Seul l’utilisateur peut sélectionner le plan d’installation actuel ; les applications ne peuvent pas modifier la carte d’installation actuelle.

 

 