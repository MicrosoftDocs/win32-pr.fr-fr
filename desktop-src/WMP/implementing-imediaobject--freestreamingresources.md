---
title: Implémentation de IMediaObject FreeStreamingResources
description: Implémentation de IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- plug-ins Lecteur Windows Media, ressources de streaming d’exemples Echo
- plug-ins, exemples de ressources de streaming
- plug-ins de traitement de signal numérique, exemples de ressources de streaming d’écho
- Plug-ins DSP, exemples de ressources de streaming
- Echo DSP, exemple de plug-in, ressources de streaming
- Echo DSP, exemple de plug-in, libérer de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30da5f92ec8420ccc90f74256003aae02664a57a8ffad3470901f672cf37aa73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617319"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a>Implémentation de IMediaObject :: FreeStreamingResources

Il est important que votre code libère toute mémoire allouée avant la destruction de l’objet de plug-in. Lecteur Windows Media appelle **FreeStreamingResources** pour vous permettre de le faire. Pour des raisons de sécurité, l’exemple créé par l’Assistant de plug-in comprend un appel à **FreeStreamingResources** dans la méthode **FinalRelease** pour garantir que la mémoire est libérée. Vous devez ajouter le code suivant à **FreeStreamingResources** pour l’exemple ECHO :


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
    m_pbDelayPointer = NULL;
    m_cbDelayBuffer = 0;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des ressources de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




