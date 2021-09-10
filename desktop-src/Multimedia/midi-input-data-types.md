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
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364431"
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

 

 