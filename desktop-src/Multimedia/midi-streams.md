---
title: Flux MIDI
description: Flux MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- MIDI (Musical Instrument Digital Interface), flux
- MIDI (Musical Instrument Digital Interface), flux
- mémoires tampons de flux, flux MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101596"
---
# <a name="midi-streams"></a>Flux MIDI

Les événements MIDI se produisent dans le contexte d’un flux de données MIDI. Bien qu’une application puisse utiliser plusieurs flux pour définir des données musicales, le Mappeur MIDI ne reconnaît pas plusieurs flux. La plupart des applications qui utilisent des flux utilisent un flux MIDI unique.

Les fonctions suivantes fonctionnent avec les flux.



| Valeur                                            | Signification                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | Ferme un flux MIDI.                                                   |
| [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | Ouvre un flux MIDI et récupère un handle.                             |
| [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | Lit ou met en file d’attente un flux (mémoire tampon) de données MIDI sur un appareil de sortie MIDI. |
| [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | Suspend la lecture d’un flux MIDI spécifié.                             |
| [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | Récupère la position actuelle dans un flux MIDI.                        |
| [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | Définit et récupère les propriétés du flux.                                   |
| [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | Redémarre la lecture d’un flux MIDI suspendu.                              |
| [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | Désactive toutes les notes sur tous les canaux MIDI pour le flux MIDI spécifié. |



 

 

 