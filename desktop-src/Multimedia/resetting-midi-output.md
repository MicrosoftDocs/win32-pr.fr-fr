---
title: Réinitialisation de la sortie MIDI
description: Réinitialisation de la sortie MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Interface MIDI (Musical Instrument Digital Interface), réinitialisation des périphériques de sortie
- MIDI (Musical Instrument Digital Interface), réinitialisation des périphériques de sortie
- Jeux de fichiers MIDI, réinitialisation des périphériques de sortie
- réinitialisation des périphériques de sortie
- Appareil de sortie MIDI (Musical Instrument Digital Interface)
- MIDI (Musical Instrument Digital Interface), périphériques de sortie
- Jeux de fichiers MIDI, périphériques de sortie
- Périphériques de sortie MIDI
- EOX (fin de l’exclusivité)
- fin de l’exclusivité (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c0073d9fc016e21e401e4cb2e7c28b4fd1aa5e3180801975df4e334243b953
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689259"
---
# <a name="resetting-midi-output"></a>Réinitialisation de la sortie MIDI

La fonction [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) désactive toutes les notes sur tous les canaux MIDI pour un périphérique MIDI spécifié. Ensuite, la fonction marque toutes les mémoires tampons système exclusives en attente comme terminées et les retourne à l’application. Cette fonction peut être utile dans une application qui utilise une sortie MIDI pour fournir à l’utilisateur la possibilité de réinitialiser la sortie MIDI.

> [!Note]  
> L’arrêt d’un message système sans envoi d’un octet EOX (fin d’exclusivité) peut entraîner des problèmes pour l’appareil de réception. La fonction **midiOutReset** n’envoie pas d’octet EOX lorsqu’elle met fin à un message système, car les applications sont chargées de le faire.

 

 

 