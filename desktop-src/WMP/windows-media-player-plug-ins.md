---
title: Lecteur Windows Media Plug-ins
description: Lecteur Windows Media Plug-ins
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Lecteur Windows Media, plug-ins
- plug-ins Lecteur Windows Media, à propos de
- plug-ins, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521956"
---
# <a name="windows-media-player-plug-ins"></a>Lecteur Windows Media Plug-ins

Microsoft Lecteur Windows Media expose des interfaces qui vous permettent d’étendre les fonctionnalités de plusieurs façons. Les sections suivantes décrivent les architectures de plug-in prises en charge et le processus de création d’un plug-in :



| Section                                                                                                         | Description                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Génération d’un plug-in](building-a-plug-in.md)                                                                    | vous pouvez créer plusieurs types de plug-ins à l’aide de Visual Studio et de l’assistant de plug-in Lecteur Windows Media.                                                                                                                                                                                             |
| [Lecteur Windows Media Visualisations personnalisées](windows-media-player-custom-visualizations.md)                    | les visualisations Lecteur Windows Media sont des objets COM (component Object Model) utilisés pour afficher l’image visuelle qui est synchronisée avec la partie audio de la lecture du média du lecteur. Les visualisations personnalisées peuvent être créées à l’aide de Microsoft Visual C++.                                             |
| [Lecteur Windows Media Plug-ins d’interface utilisateur](windows-media-player-user-interface-plug-ins.md)                | Lecteur Windows Media plug-ins d’interface utilisateur ajoutent de nouvelles fonctionnalités au volet de **lecture** en cours du lecteur en mode complet. Vous pouvez créer des plug-ins qui utilisent la zone de visualisation, une fenêtre distincte, la zone Paramètres, la zone de métadonnées ou des plug-ins d’arrière-plan qui n’exposent aucune interface utilisateur visible. |
| [Lecteur Windows Media Plug-ins DSP](windows-media-player-dsp-plug-ins.md)                                      | Lecteur Windows Media Les plug-ins DSP modifient ou traitent les données audio et vidéo avant qu’elles ne soient rendues par le joueur. les plug-ins DSP sont des objets multimédia DirectX (DMO) qui se connectent au lecteur via des interfaces COM.                                                                                           |
| [Lecteur Windows Media Rendu des plug-ins (déconseillé)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85)) | Lecteur Windows Media le décodage des plug-ins (si nécessaire) et le rendu des données personnalisées contenues dans un flux de format de média Windows. les plug-ins de rendu sont des objets de média DirectX (DMO) qui se connectent au lecteur via des interfaces COM.                                                                  |
| [Lecteur Windows Media Plug-ins de conversion](windows-media-player-conversion-plug-ins.md)                        | les plug-ins de conversion Lecteur Windows Media convertissent les fichiers multimédias numériques créés à l’aide des technologies non fournies par Microsoft, au Format ASF (Advanced Systems Format).                                                                                                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media SDK**](windows-media-player-sdk.md)
</dt> </dl>

 

 