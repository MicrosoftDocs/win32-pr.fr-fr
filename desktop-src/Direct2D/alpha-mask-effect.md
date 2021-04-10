---
title: Effet masque Alpha
description: Cet effet applique un masque Alpha à une image. Il a deux entrées, nommées destination et Mask. Les valeurs de couleur de l’image de destination sont multipliées par le canal alpha de l’image de masque.
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87669608ab75ab7a655c072e174dbcd19df4bb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106561"
---
# <a name="alpha-mask-effect"></a><span data-ttu-id="be68c-105">Effet masque Alpha</span><span class="sxs-lookup"><span data-stu-id="be68c-105">Alpha mask effect</span></span>

<span data-ttu-id="be68c-106">Cet effet applique un masque Alpha à une image.</span><span class="sxs-lookup"><span data-stu-id="be68c-106">This effect applies an alpha mask to an image.</span></span> <span data-ttu-id="be68c-107">Il a deux entrées, nommées destination et Mask.</span><span class="sxs-lookup"><span data-stu-id="be68c-107">It has two inputs, named Destination and Mask.</span></span> <span data-ttu-id="be68c-108">Les valeurs de couleur de l’image de destination sont multipliées par le canal alpha de l’image de masque.</span><span class="sxs-lookup"><span data-stu-id="be68c-108">Color values in the Destination image are multiplied by the alpha channel of the Mask image.</span></span>

<span data-ttu-id="be68c-109">Le CLSID de cet effet est CLSID \_ D2D1AlphaMask.</span><span class="sxs-lookup"><span data-stu-id="be68c-109">The CLSID for this effect is CLSID\_D2D1AlphaMask.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="be68c-110">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="be68c-110">Effect properties</span></span>

<span data-ttu-id="be68c-111">Cet effet n’a aucune propriété propre à l’effet.</span><span class="sxs-lookup"><span data-stu-id="be68c-111">This effect has no effect-specific properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="be68c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be68c-112">Requirements</span></span>



| <span data-ttu-id="be68c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be68c-113">Requirement</span></span> | <span data-ttu-id="be68c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="be68c-114">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="be68c-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be68c-115">Minimum supported client</span></span> | <span data-ttu-id="be68c-116">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="be68c-116">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="be68c-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be68c-117">Minimum supported server</span></span> | <span data-ttu-id="be68c-118">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="be68c-118">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="be68c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="be68c-119">Header</span></span>                   | <span data-ttu-id="be68c-120">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="be68c-120">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="be68c-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be68c-121">Library</span></span>                  | <span data-ttu-id="be68c-122">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="be68c-122">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="be68c-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be68c-123">Related topics</span></span>

* [<span data-ttu-id="be68c-124">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="be68c-124">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

