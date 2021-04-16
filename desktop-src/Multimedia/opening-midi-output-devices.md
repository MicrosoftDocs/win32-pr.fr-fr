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
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463067"
---
# <a name="opening-midi-output-devices"></a>Ouverture de périphériques de sortie MIDI

Pour ouvrir un appareil de sortie MIDI pour la lecture, utilisez la fonction [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) . Cette fonction ouvre l’appareil associé à l’identificateur de périphérique spécifié et retourne un descripteur de l’appareil ouvert en écrivant le handle dans un emplacement de mémoire spécifié.

L’un des paramètres de **midiOutOpen** est une valeur de mot double. Cette valeur spécifie une fenêtre ou un handle de thread, un handle d’événement ou l’adresse d’une fonction de rappel utilisée pour surveiller la progression de la lecture des données et des mémoires tampons de flux exclusives du système MIDI. La surveillance permet à l’application de déterminer quand envoyer des blocs de données supplémentaires et quand libérer des blocs de données qui ont été envoyés. Pour plus d’informations sur ces méthodes, consultez [gestion des blocs de données MIDI](managing-midi-data-blocks.md).

 

 