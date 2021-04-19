---
description: Correction du rapport hauteur/largeur
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Correction du rapport hauteur/largeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515323"
---
# <a name="aspect-ratio-correction"></a>Correction du rapport hauteur/largeur

Cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure.

En mode mixage, VMR dimensionne la vidéo sur les proportions correctes. (Exception : consultez la [combinaison non carrée](non-square-mixing.md).) Cela peut nécessiter l’étirement de la vidéo si les proportions recommandées ne sont pas les mêmes que les proportions physiques de l’image. Par exemple, le format vidéo numérique (DV) est 720 x 480 pixels (3:2), mais doit être affiché à un proportions de 4:3.

VMR prend en charge deux comportements différents pour la correction des proportions :

-   Ajustez la taille horizontale ou verticale pour que l’image soit toujours étirée, jamais réduite. C’est maintenant le comportement par défaut.
-   Ajustez la taille horizontale, en étirant ou en réduisant la vidéo.

Étant donné que le deuxième comportement (réglage horizontal uniquement) peut entraîner une réduction de la vidéo, l’image de sortie peut avoir moins de résolution. C’est la raison pour laquelle le premier comportement est préféré. Par exemple, dans le cas d’une vidéo 720 x 480 à 4:3 proportions, le comportement par défaut produit une image 720 x 550, tandis que l’ajustement horizontal produit une plus petite image 640 x 480.

**VMR-7**: pour définir la préférence de correction du rapport hauteur/largeur, appelez [**IVMRMixerControl :: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect). Définissez l' \_ indicateur MixerPref ARAdjustXorY pour le comportement par défaut ou désactivez cet indicateur uniquement pour l’ajustement horizontal.

**VMR-9**: pour définir la préférence de correction du rapport hauteur/largeur, appelez [**IVMRMixerControl9 :: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs). Définissez l' \_ indicateur MixerPref9 ARAdjustXorY pour le comportement par défaut ou désactivez cet indicateur uniquement pour l’ajustement horizontal.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du mode de mixage VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



