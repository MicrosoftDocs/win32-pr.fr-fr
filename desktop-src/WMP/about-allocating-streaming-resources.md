---
title: À propos de l’allocation des ressources de streaming
description: À propos de l’allocation des ressources de streaming
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- plug-ins Lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, ressources de streaming audio
- Plug-ins DSP, ressources de streaming audio
- plug-ins DSP audio, ressources de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f815fe9875f2e93e140b577da6e00dd7c684c1fedbad13234ecfbf87ca84ddb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903729"
---
# <a name="about-allocating-streaming-resources"></a>À propos de l’allocation des ressources de streaming

l’exemple de plug-in DSP généré par l’assistant de plug-in Lecteur Windows Media ne requiert pas de mémoires tampons de streaming supplémentaires. Toutefois, vous souhaiterez peut-être allouer des ressources mémoire pour votre plug-in DSP. Par exemple, un plug-in qui produit un effet Echo nécessite une mémoire tampon secondaire pour créer le délai nécessaire.

L’interface **IMediaObject** contient deux méthodes pour gérer cette situation. Lecteur Windows Media appelle **IMediaObject :: AllocateStreamingResources** pour vous permettre de créer des mémoires tampons dont vous avez besoin. Lecteur Windows Media appelle ensuite **IMediaObject :: FreeStreamingResources** pour vous permettre de libérer la mémoire que vous avez allouée précédemment. L’exemple d’implémentation de plug-in DSP appelle également **FreeStreamingResources** à partir de *CProjectName*::**FinalRelease** pour s’assurer que toutes les ressources sont libérées avant la destruction de l’objet de plug-in.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




