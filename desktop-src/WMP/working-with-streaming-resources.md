---
title: Utilisation des ressources de streaming
description: Utilisation des ressources de streaming
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Plug-ins du lecteur Windows Media, exemples de ressources de streaming d’écho
- plug-ins, exemples de ressources de streaming
- plug-ins de traitement de signal numérique, exemples de ressources de streaming d’écho
- Plug-ins DSP, exemples de ressources de streaming
- Echo DSP, exemple de plug-in, ressources de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a1df8cc221f3d75c8333b3ffd41a144d28bed7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106533545"
---
# <a name="working-with-streaming-resources"></a>Utilisation des ressources de streaming

L’exemple de projet de plug-in audio DSP généré par l’Assistant de plug-in du lecteur Windows Media ne requiert pas que les ressources de streaming soient allouées par le plug-in. Toutefois, l’exemple Echo requiert une mémoire tampon distincte pour stocker les données audio pendant une période de temps pour créer l’effet de délai. La mémoire tampon est gérée par deux méthodes : **IMediaObject :: AllocateStreamingResources**, qui crée la mémoire tampon, et **IMediaObject :: FreeStreamingResources**, qui libère la mémoire tampon. Les méthodes **IMediaObject** sont implémentées dans Echo. cpp.

Les sections suivantes fournissent des informations supplémentaires sur la gestion des tampons :

-   [Variables pour gérer la mémoire tampon de délai](variables-to-manage-the-delay-buffer.md)
-   [Implémentation de IMediaObject :: AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [Implémentation de IMediaObject :: FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple Echo**](the-echo-sample.md)
</dt> </dl>

 

 




