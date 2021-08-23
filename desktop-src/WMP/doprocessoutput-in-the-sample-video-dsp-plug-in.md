---
title: DoProcessOutput dans l’exemple de plug-in DSP de vidéo
description: DoProcessOutput dans l’exemple de plug-in DSP de vidéo
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- plug-ins Lecteur Windows Media, DSP de vidéo
- plug-ins, DSP vidéo
- plug-ins de traitement de signal numérique, DoProcessOutput
- Plug-ins DSP, DoProcessOutput
- plug-ins vidéo DSP, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b031ecddc4f7a1e4a83d4f8a7d8db3b975957789d7f887bf8b12438407624205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680599"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>DoProcessOutput dans l’exemple de plug-in DSP de vidéo

Étant donné qu’un plug-in de DSP vidéo prend généralement en charge plusieurs formats vidéo, il est commode de séparer le code d’implémentation de traitement dans une fonction distincte pour chaque format. Cela signifie que l’implémentation de **DoProcessOutput** pour les plug-ins de vidéo DSP est relativement simple.

L’implémentation dans l’exemple de plug-in teste d’abord si l’utilisateur a activé le plug-in. Si le plug-in est désactivé, le code copie les données fournies dans la mémoire tampon d’entrée dans la mémoire tampon de sortie sans le modifier, comme le montre le code suivant :


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



Si le plug-in est activé, le code effectue simplement une série de vérifications sur le membre de sous- **type** de type de média d’entrée pour déterminer le format vidéo actuel. Lorsqu’une correspondance est trouvée, le code appelle la fonction de traitement appropriée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in de DSP vidéo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




