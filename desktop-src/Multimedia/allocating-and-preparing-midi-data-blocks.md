---
title: Allocation et préparation des blocs de données MIDI
description: Allocation et préparation des blocs de données MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Interface MIDI (Musical Instrument Digital Interface), allouer des blocs de données
- MIDI (Musical Instrument Digital Interface), allouer des blocs de données
- Services MIDI, allouer des blocs de données
- allouer des blocs de données MIDI
- Interface MIDI (Musical Instrument Digital Interface), préparation des blocs de données
- MIDI (Musical Instrument Digital Interface), préparation des blocs de données
- Services MIDI, préparation des blocs de données
- préparation des blocs de données MIDI
- MIDI (Musical Instrument Digital Interface), blocs de données
- MIDI (Musical Instrument Digital Interface), blocs de données
- Services MIDI, blocs de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137556c1344e6f2e8db8557d45a70c5981fa7bab99e7452cc1f756b4a8ee159b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808489"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Allocation et préparation des blocs de données MIDI

Les fonctions [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)et [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) requièrent que les applications allouent des blocs de données à transmettre aux pilotes de périphérique à des fins de lecture ou d’enregistrement. Chacune de ces fonctions utilise une structure [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) pour décrire son bloc de données.

Avant d’utiliser l’une de ces fonctions pour passer un bloc de données à un pilote de périphérique, vous devez allouer de la mémoire pour la mémoire tampon et la structure d’en-tête qui décrit le bloc de données.

Windows fournit les fonctions suivantes pour la préparation et le nettoyage des blocs de données MIDI.



| Valeur                                                    | Signification                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Prépare un bloc de données d’entrée MIDI.                      |
| [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Nettoie la préparation d’un bloc de données d’entrée MIDI.  |
| [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Prépare un bloc de données de sortie MIDI.                     |
| [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Nettoie la préparation d’un bloc de données de sortie MIDI. |



 

Avant de passer un bloc de données MIDI à un pilote de périphérique, vous devez préparer la mémoire tampon en la transmettant à la fonction [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) ou [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) . Lorsque le pilote de périphérique est terminé avec la mémoire tampon et le retourne, vous devez nettoyer cette préparation en passant la mémoire tampon à la fonction [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) ou [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) avant que toute mémoire allouée puisse être libérée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Services MIDI](midi-services.md)
</dt> </dl>

 

 