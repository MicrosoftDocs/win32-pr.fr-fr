---
title: Placer et déplacer des rectangles vidéo dans l’espace de composition
description: Positionnement et déplacement de rectangles vidéo dans l’espace de composition
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766d1ae739e46a2c56bfab81b4243c9dcf6f10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519187"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="fc47a-103">Placer et déplacer des rectangles vidéo dans l’espace de composition</span><span class="sxs-lookup"><span data-stu-id="fc47a-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="fc47a-104">Lorsque VMR mélange plusieurs flux d’entrée, il place chaque flux dans un rectangle normalisé, appelé « espace de composition ».</span><span class="sxs-lookup"><span data-stu-id="fc47a-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="fc47a-105">Dans l’espace de composition, les coordonnées (0,0, 0,0) à (1,0, 1,0) forment le rectangle vidéo visible.</span><span class="sxs-lookup"><span data-stu-id="fc47a-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="fc47a-106">Toutes les coordonnées qui se trouvent en dehors de ce rectangle sont découpées.</span><span class="sxs-lookup"><span data-stu-id="fc47a-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="fc47a-107">Une application peut effectuer des effets spéciaux en déplaçant, en étirant et en réduisant la vidéo d’un flux d’entrée, en modifiant le rectangle de destination dans l’espace de composition pour ce flux.</span><span class="sxs-lookup"><span data-stu-id="fc47a-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="fc47a-108">Si le rectangle spécifié est d’une taille différente de celle du rectangle vidéo natif, la vidéo Native sera réduite ou étirée pour s’ajuster.</span><span class="sxs-lookup"><span data-stu-id="fc47a-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="fc47a-109">Le rectangle de destination est spécifié en appelant la méthode [**IVMRMixerControl :: SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .</span><span class="sxs-lookup"><span data-stu-id="fc47a-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="fc47a-110">Supposons, par exemple, que le flux 0 (qui correspond à la broche 0) contient le flux vidéo principal et que Stream 1 (qui correspond à pin 1) contienne une vidéo secondaire.</span><span class="sxs-lookup"><span data-stu-id="fc47a-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="fc47a-111">Stream 1 peut être positionné complètement hors-écran en spécifiant un rectangle normalisé de {-1.0 f, 0.0 f, 0.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="fc47a-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="fc47a-112">Stream 1 peut ensuite être déplacé dans la zone visible en modifiant les côtés gauche et droit du rectangle lors des appels successifs à **SetOutputRect**:</span><span class="sxs-lookup"><span data-stu-id="fc47a-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



|        |                             |
|--------|-----------------------------|
| <span data-ttu-id="fc47a-113">Temps</span><span class="sxs-lookup"><span data-stu-id="fc47a-113">Time</span></span>   | <span data-ttu-id="fc47a-114">Rectangle</span><span class="sxs-lookup"><span data-stu-id="fc47a-114">Rectangle</span></span>                   |
| <span data-ttu-id="fc47a-115">t + 0</span><span class="sxs-lookup"><span data-stu-id="fc47a-115">t + 0</span></span>  | <span data-ttu-id="fc47a-116">{-1.0 f, 0.0 f, 0.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="fc47a-116">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="fc47a-117">t + 1</span><span class="sxs-lookup"><span data-stu-id="fc47a-117">t + 1</span></span>  | <span data-ttu-id="fc47a-118">{-0,9 f, 0.0 f, 0.1 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="fc47a-118">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="fc47a-119">t + 2</span><span class="sxs-lookup"><span data-stu-id="fc47a-119">t + 2</span></span>  | <span data-ttu-id="fc47a-120">{-0,8 f, 0.0 f, 0,2 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="fc47a-120">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="fc47a-121">...</span><span class="sxs-lookup"><span data-stu-id="fc47a-121">...</span></span>    | <span data-ttu-id="fc47a-122">...</span><span class="sxs-lookup"><span data-stu-id="fc47a-122">...</span></span>                         |
| <span data-ttu-id="fc47a-123">t + 10</span><span class="sxs-lookup"><span data-stu-id="fc47a-123">t + 10</span></span> | <span data-ttu-id="fc47a-124">{0.0 f, 0.0 f, 1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="fc47a-124">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![déplacement d’un flux vidéo dans l’espace de composition](images/composition-space.png)

<span data-ttu-id="fc47a-126">À l’heure t + 10, la vidéo de Stream 1 est entièrement visible.</span><span class="sxs-lookup"><span data-stu-id="fc47a-126">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="fc47a-127">Dans cet exemple, la taille native de Stream 1 a été maintenue pendant le déplacement.</span><span class="sxs-lookup"><span data-stu-id="fc47a-127">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="fc47a-128">Vous pouvez également étirer ou réduire le rectangle pour produire des effets intéressants.</span><span class="sxs-lookup"><span data-stu-id="fc47a-128">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="fc47a-129">Vous pouvez également retourner la vidéo verticalement, en spécifiant une valeur supérieure à la partie inférieure du bas, ou mettre la vidéo en miroir horizontalement en spécifiant une valeur supérieure pour la gauche par rapport à la droite.</span><span class="sxs-lookup"><span data-stu-id="fc47a-129">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc47a-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc47a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc47a-131">Utilisation du mode de mixage VMR</span><span class="sxs-lookup"><span data-stu-id="fc47a-131">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



