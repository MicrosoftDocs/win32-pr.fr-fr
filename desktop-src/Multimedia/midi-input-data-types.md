---
title: Types de données d’entrée MIDI
description: Types de données d’entrée MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Interface MIDI (Musical Instrument Digital Interface), types de données d’entrée
- MIDI (Musical Instrument Digital Interface), types de données d’entrée
- enregistrement d’un fichier audio MIDI, types de données d’entrée
- Types de données d’entrée MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3cb45c321cdac95c09274f25293f4635d5a715638367c8f9e06cf5c45777af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525219"
---
# <a name="midi-input-data-types"></a>Types de données d’entrée MIDI

Windows définit les types de données suivants pour les fonctions d’entrée MIDI.



| Valeur                            | Signification                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HMIDIIN**                      | Handle d’un appareil d’entrée MIDI.                                                                                                                                                              |
| [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | En-tête pour une mémoire tampon de flux ou un bloc de données système-exclusives MIDI. Pour les applications d’entrée, cette structure enregistre uniquement les données système exclusives (la diffusion en continu n’est pas prise en charge pour l’entrée MIDI). |
| [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | Structure utilisée pour se renseigner sur les fonctionnalités d’un appareil d’entrée MIDI.                                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement d’un fichier audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 