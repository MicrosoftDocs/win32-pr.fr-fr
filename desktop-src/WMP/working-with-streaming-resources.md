---
title: Utilisation des ressources de streaming
description: Utilisation des ressources de streaming
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- plug-ins Lecteur Windows Media, ressources de streaming d’exemples Echo
- plug-ins, exemples de ressources de streaming
- plug-ins de traitement de signal numérique, exemples de ressources de streaming d’écho
- Plug-ins DSP, exemples de ressources de streaming
- Echo DSP, exemple de plug-in, ressources de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268dc57bfad71f8ee46a3b934e671e478ca6a78a6b05fc30b7123e7b3f7f6ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118567168"
---
# <a name="working-with-streaming-resources"></a>Utilisation des ressources de streaming

l’exemple de projet de plug-in audio DSP généré par l’assistant de plug-in Lecteur Windows Media ne requiert pas que les ressources de streaming soient allouées par le plug-in. Toutefois, l’exemple Echo requiert une mémoire tampon distincte pour stocker les données audio pendant une période de temps pour créer l’effet de délai. La mémoire tampon est gérée par deux méthodes : **IMediaObject :: AllocateStreamingResources**, qui crée la mémoire tampon, et **IMediaObject :: FreeStreamingResources**, qui libère la mémoire tampon. Les méthodes **IMediaObject** sont implémentées dans Echo. cpp.

Les sections suivantes fournissent des informations supplémentaires sur la gestion des tampons :

-   [Variables pour gérer la mémoire tampon de délai](variables-to-manage-the-delay-buffer.md)
-   [Implémentation de IMediaObject :: AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [Implémentation de IMediaObject :: FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple Echo**](the-echo-sample.md)
</dt> </dl>

 

 




