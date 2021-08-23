---
title: À propos de l’exemple de plug-in de vidéo DSP
description: À propos de l’exemple de plug-in de vidéo DSP
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- plug-ins Lecteur Windows Media, exemples
- plug-ins, exemples
- plug-ins de traitement de signal numérique, exemples
- Plug-ins DSP, exemples
- plug-ins Lecteur Windows Media, DSP de vidéo
- plug-ins, DSP vidéo
- plug-ins de traitement de signal numérique, exemples vidéo
- Plug-ins DSP, exemples vidéo
- exemples, plug-ins DSP
- plug-ins vidéo DSP, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb771bb87ffb53cf46022fc17ee2588e7cdac0b6b2c821f98fe6cf86799434c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470249"
---
# <a name="about-the-sample-video-dsp-plug-in"></a>À propos de l’exemple de plug-in de vidéo DSP

L’exemple de plug-in Video DSP fournit une implémentation de traitement simple qui met à l’échelle la saturation de couleur de la vidéo par un facteur fourni par l’utilisateur dans la page de propriétés. Le plug-in accepte des valeurs comprises entre 0 et 1. La valeur par défaut est 1. La valeur 1 n’a aucun effet sur l’image vidéo ; d’autres facteurs de mise à l’échelle désaturent la couleur de l’image. Par exemple, la valeur 5 donne une saturation de couleur de 50%. La valeur zéro produit une vidéo en nuances de gris.

L’exemple de plug-in Video DSP fonctionne avec les formats vidéo suivants :

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Génération d’un plug-in DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




