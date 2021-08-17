---
title: Implémentation d’un plug-in de DSP vidéo
description: Implémentation d’un plug-in de DSP vidéo
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- plug-ins Lecteur Windows Media, DSP de vidéo
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
ms.openlocfilehash: d4afdbabd36167c11ef7c1c57aeccb475605f9365c550c572422af3440d760ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135702"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implémentation d’un plug-in de DSP vidéo

Les adaptateurs d’affichage vidéo de l’ordinateur prennent en charge un ensemble de formats vidéo. Les codecs vidéo numériques prennent également en charge un ensemble de formats vidéo. quand vous tentez de lire un fichier vidéo particulier, Lecteur Windows Media devez choisir un format à utiliser pour le rendu. Le joueur tente de trouver la meilleure correspondance entre les formats pris en charge par le codec vidéo et les formats pris en charge par la carte vidéo, c’est-à-dire celui qui donne la meilleure qualité.

pour créer un plug-in Lecteur Windows Media DSP qui traite la vidéo, vous devez d’abord choisir les formats vidéo que vous souhaitez que votre plug-in traite. L’exemple de plug-in Video DSP fonctionne avec les formats vidéo suivants :

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

Vous avez le choix entre les formats à traiter. Vous pouvez supprimer des formats de l’exemple de plug-in afin qu’ils ne soient plus pris en charge et vous pouvez ajouter du code pour traiter des formats supplémentaires.

les sections suivantes fournissent des informations supplémentaires que vous devez connaître avant de créer votre propre plug-in de DSP vidéo pour Lecteur Windows Media :

-   [Négociation du format vidéo dans l’exemple de plug-in de la vidéo DSP](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcessOutput dans l’exemple de plug-in DSP de vidéo](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Traitement de la vidéo](processing-the-video.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de votre code DSP**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




