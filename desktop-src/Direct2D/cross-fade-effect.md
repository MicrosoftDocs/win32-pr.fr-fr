---
title: Effet fondu croisé
description: Cet effet combine deux images en ajoutant des pixels pondérés à partir des images d’entrée. Il a deux entrées, nommées destination et source.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508542"
---
# <a name="cross-fade-effect"></a><span data-ttu-id="e37e4-104">Effet fondu croisé</span><span class="sxs-lookup"><span data-stu-id="e37e4-104">Cross-fade effect</span></span>

<span data-ttu-id="e37e4-105">Cet effet combine deux images en ajoutant des pixels pondérés à partir des images d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e37e4-105">This effect combines two images by adding weighted pixels from input images.</span></span> <span data-ttu-id="e37e4-106">Il a deux entrées, nommées destination et source.</span><span class="sxs-lookup"><span data-stu-id="e37e4-106">It has two inputs, named Destination and Source.</span></span>

<span data-ttu-id="e37e4-107">La formule de fondu croisé est **sortie = poids \* destination + (1-poids) \* source**.</span><span class="sxs-lookup"><span data-stu-id="e37e4-107">The cross fade formula is **output = weight \* Destination + (1 - weight) \* Source**.</span></span>

<span data-ttu-id="e37e4-108">Le CLSID de cet effet est CLSID \_ D2D1CrossFade.</span><span class="sxs-lookup"><span data-stu-id="e37e4-108">The CLSID for this effect is CLSID\_D2D1CrossFade.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="e37e4-109">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="e37e4-109">Effect properties</span></span>

| <span data-ttu-id="e37e4-110">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="e37e4-110">Display name and index enumeration</span></span>             | <span data-ttu-id="e37e4-111">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e37e4-111">Type and default value</span></span> | <span data-ttu-id="e37e4-112">Description</span><span class="sxs-lookup"><span data-stu-id="e37e4-112">Description</span></span>                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e37e4-113">Poids de la \_ prop de fondu WeightD2D1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="e37e4-113">WeightD2D1\_CROSSFADE\_PROP\_WEIGHT</span></span><br/> | <span data-ttu-id="e37e4-114">FLOAT 0.5 f</span><span class="sxs-lookup"><span data-stu-id="e37e4-114">FLOAT0.5f</span></span><br/>   | <span data-ttu-id="e37e4-115">Mesure du poids des valeurs de couleur de l’image source par rapport à l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="e37e4-115">How much to weigh the source image color values versus the destination image.</span></span> <span data-ttu-id="e37e4-116">La valeur minimale est 0.0 f (utilisez exclusivement l’image de destination pour déterminer la sortie) et la valeur maximale est 1,0 f (utilisez exclusivement l’image source pour déterminer la sortie).</span><span class="sxs-lookup"><span data-stu-id="e37e4-116">The minimum value is 0.0f (exclusively use the destination image to determine the output) and the maximum value is 1.0f (exclusively use the source image to determine the output).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e37e4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e37e4-117">Requirements</span></span>



| <span data-ttu-id="e37e4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e37e4-118">Requirement</span></span> | <span data-ttu-id="e37e4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e37e4-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="e37e4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e37e4-120">Minimum supported client</span></span> | <span data-ttu-id="e37e4-121">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e37e4-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e37e4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e37e4-122">Minimum supported server</span></span> | <span data-ttu-id="e37e4-123">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e37e4-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e37e4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e37e4-124">Header</span></span>                   | <span data-ttu-id="e37e4-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="e37e4-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="e37e4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e37e4-126">Library</span></span>                  | <span data-ttu-id="e37e4-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e37e4-127">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="e37e4-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e37e4-128">Related topics</span></span>

* [<span data-ttu-id="e37e4-129">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="e37e4-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
