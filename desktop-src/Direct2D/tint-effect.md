---
title: Effet de teinte
description: Cet effet colore l’image source en multipliant l’image source par la couleur spécifiée. Il a une seule entrée.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942057"
---
# <a name="tint-effect"></a><span data-ttu-id="d0e8b-104">Effet de teinte</span><span class="sxs-lookup"><span data-stu-id="d0e8b-104">Tint effect</span></span>

<span data-ttu-id="d0e8b-105">Cet effet colore l’image source en multipliant l’image source par la couleur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-105">This effect tints the source image by multiplying the source image by the specified color.</span></span> <span data-ttu-id="d0e8b-106">Il a une seule entrée.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-106">It has a single input.</span></span>

<span data-ttu-id="d0e8b-107">Le CLSID de cet effet est CLSID \_ D2D1Tint.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-107">The CLSID for this effect is CLSID\_D2D1Tint.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="d0e8b-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="d0e8b-108">Effect properties</span></span>



| <span data-ttu-id="d0e8b-109">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="d0e8b-109">Display name and index enumeration</span></span>                    | <span data-ttu-id="d0e8b-110">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="d0e8b-110">Type and default value</span></span>                              | <span data-ttu-id="d0e8b-111">Description</span><span class="sxs-lookup"><span data-stu-id="d0e8b-111">Description</span></span>                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d0e8b-112">Couleur de la ColorD2D1 de \_ teinte \_ \_</span><span class="sxs-lookup"><span data-stu-id="d0e8b-112">ColorD2D1\_TINT\_PROP\_COLOR</span></span><br/>               | <span data-ttu-id="d0e8b-113">D2D1 \_ Vector \_ 4F (1.0 f, 1.0 f, 1.0 f, 1.0 f)</span><span class="sxs-lookup"><span data-stu-id="d0e8b-113">D2D1\_VECTOR\_4F(1.0f, 1.0f, 1.0f, 1.0f)</span></span><br/> | <span data-ttu-id="d0e8b-114">Les couleurs de l’image source sont multipliées par cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d0e8b-114">Colors from the source image are multiplied by this value.</span></span>       |
| <span data-ttu-id="d0e8b-115">Sortie de la bride de \_ teinte ClampOutputD2D1 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="d0e8b-115">ClampOutputD2D1\_TINT\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="d0e8b-116">BOOLFALSE</span><span class="sxs-lookup"><span data-stu-id="d0e8b-116">BOOLFALSE</span></span><br/>                                | <span data-ttu-id="d0e8b-117">Indique s’il faut ou non fixer les valeurs de sortie à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="d0e8b-117">Whether or not to clamp the output values to the range \[0, 1\].</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d0e8b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0e8b-118">Requirements</span></span>



| <span data-ttu-id="d0e8b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0e8b-119">Requirement</span></span> | <span data-ttu-id="d0e8b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0e8b-120">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="d0e8b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0e8b-121">Minimum supported client</span></span> | <span data-ttu-id="d0e8b-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d0e8b-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d0e8b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0e8b-123">Minimum supported server</span></span> | <span data-ttu-id="d0e8b-124">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d0e8b-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d0e8b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0e8b-125">Header</span></span>                   | <span data-ttu-id="d0e8b-126">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="d0e8b-126">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="d0e8b-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0e8b-127">Library</span></span>                  | <span data-ttu-id="d0e8b-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d0e8b-128">d2d1.lib, dxguid.lib</span></span>                              |



 ## <a name="related-topics"></a><span data-ttu-id="d0e8b-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0e8b-129">Related topics</span></span>

* [<span data-ttu-id="d0e8b-130">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="d0e8b-130">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
