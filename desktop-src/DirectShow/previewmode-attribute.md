---
description: L’attribut PreviewMode spécifie le mode Aperçu pour le groupe. Si la valeur est TRUE, les frames peuvent être supprimés pendant la préversion. Dans le cas contraire, aucun cadre n’est supprimé pendant la version préliminaire. La valeur par défaut est TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Attribut PreviewMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392600"
---
# <a name="previewmode-attribute"></a><span data-ttu-id="c08a1-106">Attribut PreviewMode</span><span class="sxs-lookup"><span data-stu-id="c08a1-106">previewmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="c08a1-107">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c08a1-107">\[Deprecated.</span></span> <span data-ttu-id="c08a1-108">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c08a1-108">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c08a1-109">L' `previewmode` attribut spécifie le mode Aperçu pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="c08a1-109">The `previewmode` attribute specifies the preview mode for the group.</span></span> <span data-ttu-id="c08a1-110">Si la valeur est **true**, les frames peuvent être supprimés pendant la préversion.</span><span class="sxs-lookup"><span data-stu-id="c08a1-110">If the value is **TRUE**, frames might be dropped during preview.</span></span> <span data-ttu-id="c08a1-111">Dans le cas contraire, aucun cadre n’est supprimé pendant la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="c08a1-111">Otherwise, no frames are dropped during preview.</span></span> <span data-ttu-id="c08a1-112">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="c08a1-112">The default value is **TRUE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="c08a1-113">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c08a1-113">Possible Values</span></span>

<span data-ttu-id="c08a1-114">Les valeurs suivantes sont définies sur TRUE : y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="c08a1-114">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="c08a1-115">Les valeurs suivantes sont définies avec la valeur FALSe : n, N, f, F, 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="c08a1-115">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c08a1-116">S'applique à</span><span class="sxs-lookup"><span data-stu-id="c08a1-116">Applies To</span></span>

[<span data-ttu-id="c08a1-117">**Communauté**</span><span class="sxs-lookup"><span data-stu-id="c08a1-117">**group**</span></span>](group-element.md)

## <a name="remarks"></a><span data-ttu-id="c08a1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c08a1-118">Remarks</span></span>

<span data-ttu-id="c08a1-119">Dans le paramètre par défaut, les images sont supprimées lors de l’aperçu des effets ou des transitions lents, afin de maintenir la vidéo synchronisée avec l’audio.</span><span class="sxs-lookup"><span data-stu-id="c08a1-119">Under the default setting, frames are dropped while previewing slow effects or transitions, to keep the video synchronized with the audio.</span></span> <span data-ttu-id="c08a1-120">La vidéo peut paraître hachée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="c08a1-120">The video might look choppy as a result.</span></span> <span data-ttu-id="c08a1-121">L’affectation de la **valeur false** à cet attribut force chaque frame à être rendu pendant la version préliminaire, ce qui peut entraîner une désynchronisation de la vidéo avec l’audio.</span><span class="sxs-lookup"><span data-stu-id="c08a1-121">Setting this attribute to **FALSE** forces every frame to render during preview, possibly resulting in the video becoming out of sync with the audio.</span></span> <span data-ttu-id="c08a1-122">Les frames ne sont jamais supprimés lors de l’écriture dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="c08a1-122">Frames are never dropped when writing to a file.</span></span>

## <a name="see-also"></a><span data-ttu-id="c08a1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c08a1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c08a1-124">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="c08a1-124">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="c08a1-125">**IAMTimelineGroup::SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="c08a1-125">**IAMTimelineGroup::SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



