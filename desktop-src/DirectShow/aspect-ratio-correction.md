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
# <a name="aspect-ratio-correction"></a><span data-ttu-id="8b5c4-103">Correction du rapport hauteur/largeur</span><span class="sxs-lookup"><span data-stu-id="8b5c4-103">Aspect Ratio Correction</span></span>

<span data-ttu-id="8b5c4-104">Cette rubrique s’applique à Windows XP Service Pack 2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="8b5c4-105">En mode mixage, VMR dimensionne la vidéo sur les proportions correctes.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-105">In mixing mode, the VMR sizes the video to the correct aspect ratio.</span></span> <span data-ttu-id="8b5c4-106">(Exception : consultez la [combinaison non carrée](non-square-mixing.md).) Cela peut nécessiter l’étirement de la vidéo si les proportions recommandées ne sont pas les mêmes que les proportions physiques de l’image.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-106">(Exception: See [Non-Square Mixing](non-square-mixing.md).) This may require stretching the video if the preferred aspect ratio is not the same as the image's physical aspect ratio.</span></span> <span data-ttu-id="8b5c4-107">Par exemple, le format vidéo numérique (DV) est 720 x 480 pixels (3:2), mais doit être affiché à un proportions de 4:3.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-107">For example, digital video (DV) format is 720 x 480 pixels (3:2) but should be displayed at a 4:3 aspect ratio.</span></span>

<span data-ttu-id="8b5c4-108">VMR prend en charge deux comportements différents pour la correction des proportions :</span><span class="sxs-lookup"><span data-stu-id="8b5c4-108">The VMR supports two different behaviors for aspect ratio correction:</span></span>

-   <span data-ttu-id="8b5c4-109">Ajustez la taille horizontale ou verticale pour que l’image soit toujours étirée, jamais réduite.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-109">Adjust either the horizontal or vertical size, so that the image is always stretched, never shrunk.</span></span> <span data-ttu-id="8b5c4-110">C’est maintenant le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-110">This is now the default behavior.</span></span>
-   <span data-ttu-id="8b5c4-111">Ajustez la taille horizontale, en étirant ou en réduisant la vidéo.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-111">Adjust the horizontal size, either stretching or shrinking the video.</span></span>

<span data-ttu-id="8b5c4-112">Étant donné que le deuxième comportement (réglage horizontal uniquement) peut entraîner une réduction de la vidéo, l’image de sortie peut avoir moins de résolution.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-112">Because the second behavior (horizontal adjustment only) may entail shrinking the video, the output image may have less resolution.</span></span> <span data-ttu-id="8b5c4-113">C’est la raison pour laquelle le premier comportement est préféré.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-113">For this reason, the first behavior is preferred.</span></span> <span data-ttu-id="8b5c4-114">Par exemple, dans le cas d’une vidéo 720 x 480 à 4:3 proportions, le comportement par défaut produit une image 720 x 550, tandis que l’ajustement horizontal produit une plus petite image 640 x 480.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-114">For example, in the case of 720 x 480 video at 4:3 aspect ratio, the default behavior produces a 720 x 550 image, while horizontal adjustment produces a smaller 640 x 480 image.</span></span>

<span data-ttu-id="8b5c4-115">**VMR-7**: pour définir la préférence de correction du rapport hauteur/largeur, appelez [**IVMRMixerControl :: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span><span class="sxs-lookup"><span data-stu-id="8b5c4-115">**VMR-7**: To set the aspect ratio correction preference, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span></span> <span data-ttu-id="8b5c4-116">Définissez l' \_ indicateur MixerPref ARAdjustXorY pour le comportement par défaut ou désactivez cet indicateur uniquement pour l’ajustement horizontal.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-116">Set the MixerPref\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

<span data-ttu-id="8b5c4-117">**VMR-9**: pour définir la préférence de correction du rapport hauteur/largeur, appelez [**IVMRMixerControl9 :: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span><span class="sxs-lookup"><span data-stu-id="8b5c4-117">**VMR-9**: To set the aspect ratio correction preference, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span></span> <span data-ttu-id="8b5c4-118">Définissez l' \_ indicateur MixerPref9 ARAdjustXorY pour le comportement par défaut ou désactivez cet indicateur uniquement pour l’ajustement horizontal.</span><span class="sxs-lookup"><span data-stu-id="8b5c4-118">Set the MixerPref9\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b5c4-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b5c4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b5c4-120">Utilisation du mode de mixage VMR</span><span class="sxs-lookup"><span data-stu-id="8b5c4-120">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



