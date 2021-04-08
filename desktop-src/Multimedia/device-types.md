---
title: Types d’appareils
description: Types d’appareils
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674845"
---
# <a name="device-types"></a>Types d’appareils

MCI reconnaît un ensemble de base de *types d’appareils*. Un type d’appareil est un ensemble de pilotes MCI qui partagent un jeu de commandes commun et sont utilisés pour contrôler des périphériques multimédias ou des fichiers de données similaires. De nombreuses commandes MCI, telles que [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), nécessitent que vous spécifiiez un type d’appareil.

Le tableau suivant répertorie les types de périphériques définis. L’implémentation actuelle de MCI comprend des jeux de commandes pour un sous-ensemble de ces appareils.



| Type d’appareil      | Constante                      | Description                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | \_ \_ CD audio MCI \_ devtype       | Lecteur audio CD                                  |
| **anciens**          | \_dat devtype \_ MCI             | Lecteur de bandes audio numérique                        |
| **digitalvideo** | \_ \_ vidéo numérique MCI \_ devtype  | Vidéo numérique dans une fenêtre (non basée sur GDI)        |
| **autres**        | MCI \_ devtype \_ autre           | Appareil MCI non défini                             |
| **superposition**      | superposition MCI \_ devtype \_         | Superposition d’appareil (vidéo analogique dans une fenêtre)        |
| **scanner**      | \_ \_ scanneur devtype MCI         | Scanneur d’images                                    |
| **sequencer**    | \_ \_ séquenceur MCI devtype       | Séquenceur MIDI                                   |
| **vidéo**          | \_magnétoscope devtype \_ MCI             | Vidéo-magnétoscope ou lecteur                |
| **videodisc**    | \_VIDEODISC devtype \_ MCI       | Lecteur Videodisc                                 |
| **WaveAudio**    | MCI \_ devtype \_ Waveform \_ audio | Périphérique audio qui lit des fichiers Waveform numérisés |



 

Dans ce document, les noms des types d’appareils sont en gras. Les noms de type d’appareil sont utilisés avec l’interface de chaîne de commande. Les constantes de type appareil sont utilisées avec l’interface de message de commande.

 

 




