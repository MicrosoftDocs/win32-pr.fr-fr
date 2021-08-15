---
title: Erreurs de Sequencer
description: Erreurs de Sequencer
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- MCIERR les valeurs de retour, erreurs de Sequencer
- Référence multimédia, erreurs de Sequencer
- référence pour les éléments multimédias, les erreurs Sequencer
- MCI (Media Control Interface), erreurs Sequencer
- MCI (Media Control Interface), erreurs Sequencer
- informations de référence sur MCI, erreurs Sequencer
- Référence MCI, erreurs de Sequencer
- MCI (Media Control Interface), Erreurs
- MCI (interface de contrôle multimédia), Erreurs
- informations de référence sur MCI, Erreurs
- Informations de référence sur MCI, Erreurs
- Erreurs de Sequencer
- Erreurs de séquenceur MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea7e5b38d5541041e8ec065c8cad31f9d31ed1bfa9f22562aba1bf1ff04039b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371127"
---
# <a name="sequencer-errors"></a>Erreurs de Sequencer

Les valeurs de retour supplémentaires suivantes sont définies pour les séquenceurs MCI :



| Valeur                          | Signification                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ Seq \_ div \_ incompatible | Les formats d’heure du pointeur de la chanson et du SMPTE sont singuliers. Vous ne pouvez pas les utiliser ensemble.                                                              |
| MCIERR \_ Seq \_ NOMIDIPRESENT     | Aucun périphérique MIDI n’est installé sur ce système. Utilisez l’option pilotes du panneau de configuration pour installer un pilote MIDI.                                       |
| MCIERR \_ Seq \_ port \_ Inuse       | Le port MIDI spécifié est déjà utilisé. Attendez qu’il soit libre ; Ensuite, réessayez.                                                                       |
| MCIERR \_ Seq \_ port \_ MAPNODEVICE | Le programme d’installation du mappeur MIDI en cours fait référence à un périphérique MIDI qui n’est pas installé sur le système. Utilisez le Mappeur MIDI à partir du panneau de configuration pour modifier l’installation. |
| MCIERR \_ Seq \_ port \_ MISCERROR   | Une erreur s’est produite avec le port spécifié.                                                                                                                   |
| \_port MCIERR \_ Seq \_ inexistant | L’appareil MIDI spécifié n’est pas installé sur le système. Utilisez l’option pilotes du panneau de configuration pour installer un appareil MIDI.                        |
| MCIERR \_ Seq \_ PORTUNSPECIFIED   | Le système n’a pas de port MIDI en cours spécifié.                                                                                                  |
| MCIERR \_ Seq \_ Timer             | Toutes les minuteries multimédias sont utilisées par d’autres applications. Quittez l’une de ces applications ; Ensuite, réessayez.                                             |



 

 

 




