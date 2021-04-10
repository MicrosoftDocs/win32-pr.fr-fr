---
title: À propos de l’allocation des ressources de streaming
description: À propos de l’allocation des ressources de streaming
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Plug-ins du lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, ressources de streaming audio
- Plug-ins DSP, ressources de streaming audio
- plug-ins DSP audio, ressources de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba82f150908e7b96f4e6e56c2161e1b2fdfe145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100761"
---
# <a name="about-allocating-streaming-resources"></a>À propos de l’allocation des ressources de streaming

L’exemple de plug-in DSP généré par l’Assistant de plug-in du lecteur Windows Media ne requiert pas de mémoires tampons de streaming supplémentaires. Toutefois, vous souhaiterez peut-être allouer des ressources mémoire pour votre plug-in DSP. Par exemple, un plug-in qui produit un effet Echo nécessite une mémoire tampon secondaire pour créer le délai nécessaire.

L’interface **IMediaObject** contient deux méthodes pour gérer cette situation. Le lecteur Windows Media appelle **IMediaObject :: AllocateStreamingResources** pour vous permettre de créer les mémoires tampons dont vous avez besoin. Le lecteur Windows Media appelle ensuite **IMediaObject :: FreeStreamingResources** pour vous permettre de libérer la mémoire que vous avez allouée précédemment. L’exemple d’implémentation de plug-in DSP appelle également **FreeStreamingResources** à partir de *CProjectName*::**FinalRelease** pour s’assurer que toutes les ressources sont libérées avant la destruction de l’objet de plug-in.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




