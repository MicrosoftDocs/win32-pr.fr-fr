---
title: Entrée et sortie de données
description: Entrée et sortie de données
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Plug-ins du lecteur Windows Media, entrée et sortie de données
- plug-ins, entrée et sortie de données
- plug-ins de traitement de signal numérique, entrée et sortie de données
- Plug-ins DSP, entrée et sortie de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100721"
---
# <a name="data-input-and-output"></a>Entrée et sortie de données

Le lecteur Windows Media fournit des données audio ou vidéo aux plug-ins DSP par le biais d’une mémoire tampon d’entrée allouée par le lecteur Windows Media. Les plug-ins DSP renvoient des données traitées au lecteur Windows Media par le biais d’une mémoire tampon de sortie qui est également allouée par le lecteur Windows Media. Le lecteur Windows Media gère le processus de passage de données entre lui-même et le plug-in DSP en appelant des méthodes implémentées par le plug-in. Pour un plug-in agissant comme un objet de média DirectX (DMO), le processus fonctionne comme suit :

1.  Le lecteur Windows Media appelle **IMediaObject ::P rocessinput**, en passant un pointeur vers un objet **IMediaBuffer** vers le plug-in DSP.
2.  Le plug-in DSP conserve un décompte de références sur l’objet de mémoire tampon d’entrée. Le plug-in DSP retourne une valeur **HRESULT** de réussite ou d’échec appropriée.
3.  Le lecteur Windows Media appelle **IMediaObject ::P rocessoutput**, en passant un pointeur vers un tableau de structures de **\_ \_ \_ tampons de données de sortie DMO** (qui contiennent des mémoires tampons de sortie) vers le plug-in DSP.
4.  Le plug-in DSP traite les données dans la mémoire tampon d’entrée, puis copie les données dans la mémoire tampon de sortie appropriée. Le plug-in DSP libère le décompte de références sur l’objet de mémoire tampon d’entrée lorsque toutes les données de la mémoire tampon ont été traitées. Le plug-in DSP retourne alors un **HRESULT** de réussite ou d’échec approprié.
5.  Le lecteur Windows Media affiche le contenu dans la mémoire tampon de sortie.

Pour un plug-in agissant en tant que Media Foundation Transform (MFT), le processus fonctionne comme suit :

-   Le lecteur Windows Media appelle **IMFTransform ::P rocessinput**, en passant un pointeur vers un objet d’interface **IMFSample** vers le plug-in DSP.
    1.  Le plug-in DSP conserve un décompte de références sur l’interface **IMFSample** . Le plug-in DSP retourne une valeur **HRESULT** de réussite ou d’échec appropriée.
    2.  Le lecteur Windows Media appelle **IMFTransform ::P rocessoutput**, en passant un pointeur vers un tableau de structures de **\_ \_ \_ mémoire tampon de données de sortie MFT** (qui contiennent des mémoires tampons de sortie) vers le plug-in DSP.
    3.  Le plug-in DSP traite les données dans la mémoire tampon d’entrée, puis copie les données dans la mémoire tampon de sortie appropriée. Le plug-in DSP libère le décompte de références sur l’objet de mémoire tampon d’entrée lorsque toutes les données de la mémoire tampon ont été traitées. Le plug-in DSP retourne alors un **HRESULT** de réussite ou d’échec approprié.
    4.  Le lecteur Windows Media affiche le contenu dans la mémoire tampon de sortie.

Ce processus se répète continuellement lorsque le plug-in est activé et que le lecteur Windows Media a le contenu à afficher.

> [!Note]  
> N’écrivez pas de code qui écrit des données dans la mémoire tampon d’entrée ou qui lit des données à partir de la mémoire tampon de sortie. L’accès incorrect aux tampons de données peut générer des résultats inattendus.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




