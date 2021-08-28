---
title: Ouverture de périphériques de sortie MIDI
description: Ouverture de périphériques de sortie MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- Appareil de sortie MIDI (Musical Instrument Digital Interface)
- MIDI (Musical Instrument Digital Interface), périphériques de sortie
- Jeux de fichiers MIDI, périphériques de sortie
- Périphériques de sortie MIDI
- Interface MIDI (Musical Instrument Digital Interface), ouverture des périphériques de sortie
- MIDI (Musical Instrument Digital Interface), ouverture des appareils de sortie
- exécution de fichiers MIDI, ouverture d’appareils de sortie
- ouverture de périphériques de sortie MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0976e265fe253d02bc9662e6ea9b376d5acc4b5fd9f62e56642b56df53ce135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136708"
---
# <a name="opening-midi-output-devices"></a>Ouverture de périphériques de sortie MIDI

Pour ouvrir un appareil de sortie MIDI pour la lecture, utilisez la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) . Cette fonction ouvre l’appareil associé à l’identificateur de périphérique spécifié et retourne un descripteur de l’appareil ouvert en écrivant le handle dans un emplacement de mémoire spécifié.

L’un des paramètres de **midiOutOpen** est une valeur de mot double. Cette valeur spécifie une fenêtre ou un handle de thread, un handle d’événement ou l’adresse d’une fonction de rappel utilisée pour surveiller la progression de la lecture des données et des mémoires tampons de flux exclusives du système MIDI. La surveillance permet à l’application de déterminer quand envoyer des blocs de données supplémentaires et quand libérer des blocs de données qui ont été envoyés. Pour plus d’informations sur ces méthodes, consultez [gestion des blocs de données MIDI](managing-midi-data-blocks.md).

 

 