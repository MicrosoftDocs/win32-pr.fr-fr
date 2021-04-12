---
title: Interrogation d’appareils MIDI
description: Interrogation d’appareils MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Interface MIDI (Musical Instrument Digital Interface), interrogation des appareils
- MIDI (Musical Instrument Digital Interface), interroger des appareils
- Services MIDI, interrogation des appareils
- interrogation d’appareils MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381822"
---
# <a name="querying-midi-devices"></a>Interrogation d’appareils MIDI

Avant de lancer ou d’enregistrer des données MIDI, vous devez déterminer les fonctionnalités du matériel MIDI présent dans le système. La fonctionnalité MIDI peut varier d’un ordinateur multimédia à l’autre. les applications ne doivent pas faire d’hypothèses sur le matériel présent dans un système donné.

Windows fournit les fonctions suivantes pour déterminer le nombre de périphériques MIDI disponibles pour l’entrée ou la sortie dans un système donné.



| Valeur                                          | Signification                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | Récupère le nombre d’appareils d’entrée MIDI présents dans le système.  |
| [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | Récupère le nombre d’appareils de sortie MIDI présents dans le système. |



 

Comme les autres périphériques audio, les périphériques MIDI sont identifiés par un identificateur de périphérique, qui est déterminé implicitement à partir du nombre d’appareils présents dans un système donné. Les identificateurs d’appareil sont compris entre zéro et le nombre d’appareils présents, moins un. Par exemple, s’il existe deux périphériques de sortie MIDI dans un système, les identificateurs d’appareil valides sont 0 et 1.

Une fois que vous avez déterminé le nombre de périphériques d’entrée ou de sortie MIDI présents dans un système, vous pouvez vous renseigner sur les fonctionnalités de chaque appareil. Windows fournit les fonctions suivantes pour déterminer les fonctionnalités des périphériques audio.



| Valeur                                          | Signification                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | Récupère les fonctionnalités d’un appareil d’entrée MIDI donné et place ces informations dans la structure [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) .    |
| [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | Récupère les fonctionnalités d’un appareil de sortie MIDI donné et place ces informations dans la structure [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) . |



 

Chacune de ces fonctions a un paramètre qui spécifie l’adresse d’une structure que la fonction remplit à l’aide d’informations sur les fonctionnalités d’un appareil spécifié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Services MIDI](midi-services.md)
</dt> </dl>

 

 