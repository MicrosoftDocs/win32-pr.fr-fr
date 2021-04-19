---
title: Plug-ins du lecteur Windows Media
description: Plug-ins du lecteur Windows Media
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Lecteur Windows Media, plug-ins
- Plug-ins du lecteur Windows Media, à propos de
- plug-ins, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511308"
---
# <a name="windows-media-player-plug-ins"></a>Plug-ins du lecteur Windows Media

Le lecteur Microsoft Windows Media expose des interfaces qui vous permettent d’étendre les fonctionnalités de plusieurs façons. Les sections suivantes décrivent les architectures de plug-in prises en charge et le processus de création d’un plug-in :



| Section                                                                                                         | Description                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Génération d’un plug-in](building-a-plug-in.md)                                                                    | Vous pouvez créer plusieurs types de plug-ins à l’aide de Visual Studio et de l’Assistant de plug-in du lecteur Windows Media.                                                                                                                                                                                             |
| [Visualisations personnalisées du lecteur Windows Media](windows-media-player-custom-visualizations.md)                    | Les visualisations du lecteur Windows Media sont des objets COM (Component Object Model) utilisés pour afficher l’image visuelle qui est synchronisée avec la partie audio de la lecture du média du lecteur. Les visualisations personnalisées peuvent être créées à l’aide de Microsoft Visual C++.                                             |
| [Plug-ins de l’interface utilisateur du lecteur Windows Media](windows-media-player-user-interface-plug-ins.md)                | Les plug-ins de l’interface utilisateur du lecteur Windows Media ajoutent de nouvelles fonctionnalités au volet de **lecture** en cours du lecteur en mode complet. Vous pouvez créer des plug-ins qui utilisent la zone de visualisation, une fenêtre distincte, la zone Paramètres, la zone de métadonnées ou des plug-ins d’arrière-plan qui n’exposent aucune interface utilisateur visible. |
| [Plug-ins du lecteur Windows Media DSP](windows-media-player-dsp-plug-ins.md)                                      | Les plug-ins du lecteur Windows Media DSP modifient ou traitent les données audio et vidéo avant qu’il ne soit rendu par le lecteur. Les plug-ins DSP sont des objets Media Media Objects (DMO) qui se connectent au lecteur via des interfaces COM.                                                                                           |
| [Plug-ins de rendu du lecteur Windows Media (déconseillé)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85)) | Décoder les plug-ins de rendu de Windows Media Player (si nécessaire) et rendre les données personnalisées contenues dans un flux de format Windows Media. Les plug-ins de rendu sont des objets Media Media Objects (DMO) qui se connectent au lecteur via des interfaces COM.                                                                  |
| [Plug-ins de conversion du lecteur Windows Media](windows-media-player-conversion-plug-ins.md)                        | Les plug-ins de conversion du lecteur Windows Media convertissent les fichiers multimédias numériques créés à l’aide des technologies non fournies par Microsoft en ASF (Advanced Systems Format).                                                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**SDK du lecteur Windows Media**](windows-media-player-sdk.md)
</dt> </dl>

 

 