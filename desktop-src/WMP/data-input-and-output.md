---
title: Entrée et sortie de données
description: Entrée et sortie de données
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- plug-ins Lecteur Windows Media, entrée et sortie de données
- plug-ins, entrée et sortie de données
- plug-ins de traitement de signal numérique, entrée et sortie de données
- Plug-ins DSP, entrée et sortie de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31e7c6fba24451d65e59c3fb9f56ec6b1413be3d595530414c25c52964b9b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863669"
---
# <a name="data-input-and-output"></a>Entrée et sortie de données

Lecteur Windows Media fournit des données audio ou vidéo aux plug-ins DSP par le biais d’une mémoire tampon d’entrée allouée par Lecteur Windows Media. les plug-ins DSP renvoient des données traitées à Lecteur Windows Media par le biais d’une mémoire tampon de sortie qui est également allouée par Lecteur Windows Media. Lecteur Windows Media gère le processus de passage de données entre lui-même et le plug-in DSP en appelant des méthodes implémentées par le plug-in. pour un plug-in agissant comme un objet de média DirectX (DMO), le processus fonctionne comme suit :

1.  Lecteur Windows Media appelle **IMediaObject ::P rocessinput**, en passant un pointeur vers un objet **IMediaBuffer** vers le plug-in DSP.
2.  Le plug-in DSP conserve un décompte de références sur l’objet de mémoire tampon d’entrée. Le plug-in DSP retourne une valeur **HRESULT** de réussite ou d’échec appropriée.
3.  Lecteur Windows Media appelle **IMediaObject ::P rocessoutput**, en passant un pointeur vers un tableau de DMO structures de **\_ \_ \_ mémoire tampon de données de sortie** (qui contiennent des mémoires tampons de sortie) au plug-in DSP.
4.  Le plug-in DSP traite les données dans la mémoire tampon d’entrée, puis copie les données dans la mémoire tampon de sortie appropriée. Le plug-in DSP libère le décompte de références sur l’objet de mémoire tampon d’entrée lorsque toutes les données de la mémoire tampon ont été traitées. Le plug-in DSP retourne alors un **HRESULT** de réussite ou d’échec approprié.
5.  Lecteur Windows Media restitue le contenu dans la mémoire tampon de sortie.

Pour un plug-in agissant en tant que Media Foundation Transform (MFT), le processus fonctionne comme suit :

-   Lecteur Windows Media appelle **IMFTransform ::P rocessinput**, en passant un pointeur vers un objet d’interface **IMFSample** vers le plug-in DSP.
    1.  Le plug-in DSP conserve un décompte de références sur l’interface **IMFSample** . Le plug-in DSP retourne une valeur **HRESULT** de réussite ou d’échec appropriée.
    2.  Lecteur Windows Media appelle **IMFTransform ::P rocessoutput**, en passant un pointeur vers un tableau de structures de **\_ \_ \_ mémoire tampon de données de sortie MFT** (qui contiennent des mémoires tampons de sortie) vers le plug-in DSP.
    3.  Le plug-in DSP traite les données dans la mémoire tampon d’entrée, puis copie les données dans la mémoire tampon de sortie appropriée. Le plug-in DSP libère le décompte de références sur l’objet de mémoire tampon d’entrée lorsque toutes les données de la mémoire tampon ont été traitées. Le plug-in DSP retourne alors un **HRESULT** de réussite ou d’échec approprié.
    4.  Lecteur Windows Media restitue le contenu dans la mémoire tampon de sortie.

ce processus se répète continuellement pendant que le plug-in est activé et Lecteur Windows Media a du contenu à afficher.

> [!Note]  
> N’écrivez pas de code qui écrit des données dans la mémoire tampon d’entrée ou qui lit des données à partir de la mémoire tampon de sortie. L’accès incorrect aux tampons de données peut générer des résultats inattendus.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




