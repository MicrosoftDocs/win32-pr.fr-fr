---
title: Vue d’ensemble de l’exemple Echo
description: Vue d’ensemble de l’exemple Echo
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Plug-ins du lecteur Windows Media, vue d’ensemble de l’exemple Echo
- plug-ins, vue d’ensemble de l’exemple Echo
- plug-ins de traitement de signal numérique, vue d’ensemble de l’exemple Echo
- Plug-ins DSP, vue d’ensemble de l’exemple Echo
- Echo DSP, exemple de plug-in, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513479"
---
# <a name="echo-sample-overview"></a>Vue d’ensemble de l’exemple Echo

Ce guide crée un plug-in de lecteur Windows Media DSP qui crée un effet d’écho dans le son PCM lors de la lecture. Les objectifs du plug-in sont les suivants :

-   Le plug-in traite uniquement les données audio PCM 8 bits ou 16 bits.
-   Il prend en charge un délai entre 10 millisecondes (MS) et 2000 ms (2 secondes). Cela représente une plage pratique pour la plupart des applications.
-   Il prend en charge la combinaison du signal d’origine avec le signal de temporisation.
-   Il fournit une implémentation de page de propriétés qui permet à l’utilisateur de fournir une valeur pour le délai et une valeur pour le pourcentage de signal de retard par rapport au niveau de signal audio global.
-   Pour créer le code, modifiez l’exemple de plug-in de plug-in de l’Assistant de plug-in du lecteur Windows Media.

L’exemple Echo n’est pas inclus dans le kit de développement logiciel (SDK) du lecteur Windows Media. Il s’agit d’un exemple que vous créez. Pour créer l’exemple Echo, vous devez commencer par le projet par défaut à partir de l’Assistant de plug-in du lecteur Windows Media. Vous pouvez nommer le projet comme vous le souhaitez ; Cette documentation suppose que le projet est nommé Echo. Pour plus d’informations sur l’utilisation de l’Assistant, consultez [génération d’un plug-in DSP](building-a-dsp-plug-in.md).

La section suivante fournit une vue d’ensemble de la façon dont l’exemple crée un effet d’écho :

-   [Fonctionnement de l’exemple Echo](how-the-echo-sample-works.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple Echo**](the-echo-sample.md)
</dt> </dl>

 

 




