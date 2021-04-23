---
title: Placer et déplacer des rectangles vidéo dans l’espace de composition
description: Positionnement et déplacement de rectangles vidéo dans l’espace de composition
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96955fc2107036299ab6f530eeda76374a0a0315
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909627"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="4f6d9-103">Placer et déplacer des rectangles vidéo dans l’espace de composition</span><span class="sxs-lookup"><span data-stu-id="4f6d9-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="4f6d9-104">Lorsque VMR mélange plusieurs flux d’entrée, il place chaque flux dans un rectangle normalisé, appelé « espace de composition ».</span><span class="sxs-lookup"><span data-stu-id="4f6d9-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="4f6d9-105">Dans l’espace de composition, les coordonnées (0,0, 0,0) à (1,0, 1,0) forment le rectangle vidéo visible.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="4f6d9-106">Toutes les coordonnées qui se trouvent en dehors de ce rectangle sont découpées.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="4f6d9-107">Une application peut effectuer des effets spéciaux en déplaçant, en étirant et en réduisant la vidéo d’un flux d’entrée, en modifiant le rectangle de destination dans l’espace de composition pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="4f6d9-108">Si le rectangle spécifié est d’une taille différente de celle du rectangle vidéo natif, la vidéo Native sera réduite ou étirée pour s’ajuster.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="4f6d9-109">Le rectangle de destination est spécifié en appelant la méthode [**IVMRMixerControl :: SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .</span><span class="sxs-lookup"><span data-stu-id="4f6d9-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="4f6d9-110">Supposons, par exemple, que le flux 0 (qui correspond à la broche 0) contient le flux vidéo principal et que Stream 1 (qui correspond à pin 1) contienne une vidéo secondaire.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="4f6d9-111">Stream 1 peut être positionné complètement hors-écran en spécifiant un rectangle normalisé de {-1.0 f, 0.0 f, 0.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="4f6d9-112">Stream 1 peut ensuite être déplacé dans la zone visible en modifiant les côtés gauche et droit du rectangle lors des appels successifs à **SetOutputRect**:</span><span class="sxs-lookup"><span data-stu-id="4f6d9-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



| <span data-ttu-id="4f6d9-113">Étiquette</span><span class="sxs-lookup"><span data-stu-id="4f6d9-113">Label</span></span> | <span data-ttu-id="4f6d9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f6d9-114">Value</span></span> |
|--------|-----------------------------|
| <span data-ttu-id="4f6d9-115">Temps</span><span class="sxs-lookup"><span data-stu-id="4f6d9-115">Time</span></span>   | <span data-ttu-id="4f6d9-116">Rectangle</span><span class="sxs-lookup"><span data-stu-id="4f6d9-116">Rectangle</span></span>                   |
| <span data-ttu-id="4f6d9-117">t + 0</span><span class="sxs-lookup"><span data-stu-id="4f6d9-117">t + 0</span></span>  | <span data-ttu-id="4f6d9-118">{-1.0 f, 0.0 f, 0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="4f6d9-118">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="4f6d9-119">t + 1</span><span class="sxs-lookup"><span data-stu-id="4f6d9-119">t + 1</span></span>  | <span data-ttu-id="4f6d9-120">{-0,9 f, 0.0 f, 0.1 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="4f6d9-120">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="4f6d9-121">t + 2</span><span class="sxs-lookup"><span data-stu-id="4f6d9-121">t + 2</span></span>  | <span data-ttu-id="4f6d9-122">{-0,8 f, 0.0 f, 0,2 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="4f6d9-122">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="4f6d9-123">...</span><span class="sxs-lookup"><span data-stu-id="4f6d9-123">...</span></span>    | <span data-ttu-id="4f6d9-124">...</span><span class="sxs-lookup"><span data-stu-id="4f6d9-124">...</span></span>                         |
| <span data-ttu-id="4f6d9-125">t + 10</span><span class="sxs-lookup"><span data-stu-id="4f6d9-125">t + 10</span></span> | <span data-ttu-id="4f6d9-126">{0.0 f, 0.0 f, 1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="4f6d9-126">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![déplacement d’un flux vidéo dans l’espace de composition](images/composition-space.png)

<span data-ttu-id="4f6d9-128">À l’heure t + 10, la vidéo de Stream 1 est entièrement visible.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-128">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="4f6d9-129">Dans cet exemple, la taille native de Stream 1 a été maintenue pendant le déplacement.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-129">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="4f6d9-130">Vous pouvez également étirer ou réduire le rectangle pour produire des effets intéressants.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-130">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="4f6d9-131">Vous pouvez également retourner la vidéo verticalement, en spécifiant une valeur supérieure à la partie inférieure du bas, ou mettre la vidéo en miroir horizontalement en spécifiant une valeur supérieure pour la gauche par rapport à la droite.</span><span class="sxs-lookup"><span data-stu-id="4f6d9-131">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f6d9-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f6d9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f6d9-133">Utilisation du mode de mixage VMR</span><span class="sxs-lookup"><span data-stu-id="4f6d9-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



