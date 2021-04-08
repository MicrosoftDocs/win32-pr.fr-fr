---
title: Ouverture et fermeture de pilotes de périphérique
description: Ouverture et fermeture de pilotes de périphérique
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Interface MIDI (Musical Instrument Digital Interface), ouverture d’appareils
- MIDI (Musical Instrument Digital Interface), ouvrir des appareils
- Services MIDI, ouverture d’appareils
- ouverture d’appareils MIDI
- Interface MIDI (Musical Instrument Digital Interface), fermeture des appareils
- MIDI (Musical Instrument Digital Interface), fermer des appareils
- Services MIDI, fermeture d’appareils
- fermeture des appareils MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725077"
---
# <a name="opening-and-closing-device-drivers"></a>Ouverture et fermeture de pilotes de périphérique

Vous devez ouvrir un appareil MIDI avant de l’utiliser, et vous devez fermer l’appareil dès que vous avez fini de l’utiliser. Windows fournit les fonctions suivantes pour ouvrir et fermer différents types d’appareils MIDI.



| Valeur                                | Signification                                            |
|--------------------------------------|----------------------------------------------------|
| [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | Ferme un appareil d’entrée MIDI spécifié.              |
| [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | Ouvre un appareil d’entrée MIDI spécifié pour l’enregistrement. |
| [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | Ferme un appareil de sortie MIDI spécifié.             |
| [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | Ouvre un appareil de sortie MIDI pour la lecture.           |



 

Chaque fonction qui ouvre un appareil MIDI prend comme paramètres un identificateur d’appareil, l’adresse d’un emplacement de mémoire et certains paramètres propres aux périphériques MIDI. L’emplacement de la mémoire est rempli avec un handle d’appareil, qui est utilisé pour identifier le périphérique audio ouvert dans les appels à d’autres fonctions audio.

De nombreuses fonctions MIDI peuvent accepter un handle d’appareil ou un identificateur d’appareil. Bien que vous puissiez utiliser un handle d’appareil partout où vous utiliseriez un identificateur de périphérique, vous ne pouvez pas toujours utiliser un identificateur de périphérique quand un handle est appelé pour.

> [!Note]  
> Les périphériques MIDI ne sont pas nécessairement partageables. un appareil particulier peut donc ne pas être disponible lorsqu’un utilisateur le demande. Dans ce cas, l’application doit avertir l’utilisateur et permettre à l’utilisateur d’essayer d’ouvrir à nouveau l’appareil.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Services MIDI](midi-services.md)
</dt> </dl>

 

 