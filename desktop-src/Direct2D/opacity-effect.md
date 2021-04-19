---
title: Effet d’opacité
description: Cet effet ajuste l’opacité d’une image en multipliant le canal alpha de l’entrée par la valeur d’opacité spécifiée. Il a une seule entrée.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511576"
---
# <a name="opacity-effect"></a><span data-ttu-id="ca71d-104">Effet d’opacité</span><span class="sxs-lookup"><span data-stu-id="ca71d-104">Opacity effect</span></span>

<span data-ttu-id="ca71d-105">Cet effet ajuste l’opacité d’une image en multipliant le canal alpha de l’entrée par la valeur d’opacité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ca71d-105">This effect adjusts the opacity of an image by multiplying the alpha channel of the input by the specified opacity value.</span></span> <span data-ttu-id="ca71d-106">Il a une seule entrée.</span><span class="sxs-lookup"><span data-stu-id="ca71d-106">It has a single input.</span></span>

<span data-ttu-id="ca71d-107">Le CLSID de cet effet est CLSID \_ D2D1Opacity.</span><span class="sxs-lookup"><span data-stu-id="ca71d-107">The CLSID for this effect is CLSID\_D2D1Opacity.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="ca71d-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="ca71d-108">Effect properties</span></span>



| <span data-ttu-id="ca71d-109">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="ca71d-109">Display name and index enumeration</span></span>              | <span data-ttu-id="ca71d-110">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ca71d-110">Type and default value</span></span> | <span data-ttu-id="ca71d-111">Description</span><span class="sxs-lookup"><span data-stu-id="ca71d-111">Description</span></span>                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca71d-112">Opacité D2D1 opacité du \_ \_ Prop. \_</span><span class="sxs-lookup"><span data-stu-id="ca71d-112">Opacity D2D1\_OPACITY\_PROP\_OPACITY</span></span><br/> | <span data-ttu-id="ca71d-113">FLOAT 1.0 f</span><span class="sxs-lookup"><span data-stu-id="ca71d-113">FLOAT1.0f</span></span><br/>   | <span data-ttu-id="ca71d-114">Multiplicateur du canal alpha de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ca71d-114">The multiplier to the input image's alpha channel.</span></span> <span data-ttu-id="ca71d-115">La valeur minimale est 0.0 f et la valeur maximale est 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="ca71d-115">The minimum value is 0.0f and the maximum value is 1.0f.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ca71d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca71d-116">Requirements</span></span>



| <span data-ttu-id="ca71d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca71d-117">Requirement</span></span> | <span data-ttu-id="ca71d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca71d-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="ca71d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca71d-119">Minimum supported client</span></span> | <span data-ttu-id="ca71d-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ca71d-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ca71d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca71d-121">Minimum supported server</span></span> | <span data-ttu-id="ca71d-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ca71d-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ca71d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca71d-123">Header</span></span>                   | <span data-ttu-id="ca71d-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="ca71d-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="ca71d-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ca71d-125">Library</span></span>                  | <span data-ttu-id="ca71d-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ca71d-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="ca71d-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca71d-127">Related topics</span></span>

* [<span data-ttu-id="ca71d-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="ca71d-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
