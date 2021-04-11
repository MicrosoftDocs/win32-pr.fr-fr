---
title: Implémentation d’un plug-in de DSP vidéo
description: Implémentation d’un plug-in de DSP vidéo
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Plug-ins du lecteur Windows Media, DSP vidéo
- plug-ins, DSP vidéo
- plug-ins de traitement de signal numérique, implémentation du code
- Plug-ins DSP, implémentation du code
- plug-ins de traitement de signal numérique, modification de l’exemple de code
- Plug-ins DSP, modification de l’exemple de code
- plug-ins de traitement de signal numérique, implémentation vidéo
- Plug-ins DSP, implémentation vidéo
- plug-ins vidéo DSP, implémentation du code
- plug-ins vidéo DSP, modification de l’exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310258"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implémentation d’un plug-in de DSP vidéo

Les adaptateurs d’affichage vidéo de l’ordinateur prennent en charge un ensemble de formats vidéo. Les codecs vidéo numériques prennent également en charge un ensemble de formats vidéo. Lorsque vous tentez de lire un fichier vidéo particulier, le lecteur Windows Media doit choisir un format à utiliser pour le rendu. Le joueur tente de trouver la meilleure correspondance entre les formats pris en charge par le codec vidéo et les formats pris en charge par la carte vidéo, c’est-à-dire celui qui donne la meilleure qualité.

Pour créer un plug-in Windows Media Player DSP qui traite la vidéo, vous devez d’abord décider quels formats vidéo vous souhaitez faire traiter par votre plug-in. L’exemple de plug-in Video DSP fonctionne avec les formats vidéo suivants :

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

Vous avez le choix entre les formats à traiter. Vous pouvez supprimer des formats de l’exemple de plug-in afin qu’ils ne soient plus pris en charge et vous pouvez ajouter du code pour traiter des formats supplémentaires.

Les sections suivantes fournissent des informations supplémentaires que vous devez connaître avant de créer votre propre plug-in de DSP vidéo pour le lecteur Windows Media :

-   [Négociation du format vidéo dans l’exemple de plug-in de la vidéo DSP](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcessOutput dans l’exemple de plug-in DSP de vidéo](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Traitement de la vidéo](processing-the-video.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de votre code DSP**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




