---
title: Effet de nuances de gris
description: convertit une image en gris monochrome.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741972"
---
# <a name="grayscale-effect"></a><span data-ttu-id="33aad-103">Effet de nuances de gris</span><span class="sxs-lookup"><span data-stu-id="33aad-103">Grayscale effect</span></span>

<span data-ttu-id="33aad-104">convertit une image en gris monochrome.</span><span class="sxs-lookup"><span data-stu-id="33aad-104">Converts an image to monochromatic gray.</span></span>

<span data-ttu-id="33aad-105">Le gris utilise l’effet de matrice de couleurs pour convertir en nuances de gris, à l’aide de la matrice suivante :</span><span class="sxs-lookup"><span data-stu-id="33aad-105">Grayscale uses the color matrix effect to convert to grayscale, using the following matrix:</span></span>

![matrice de conversion](images/grayscale-effect-matrix.png)

<span data-ttu-id="33aad-107">Le CLSID de cet effet est CLSID \_ D2D1Grayscale.</span><span class="sxs-lookup"><span data-stu-id="33aad-107">The CLSID for this effect is CLSID\_D2D1Grayscale.</span></span>

-   [<span data-ttu-id="33aad-108">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="33aad-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="33aad-109">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="33aad-109">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="33aad-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33aad-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="33aad-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33aad-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="33aad-112">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="33aad-112">Example image</span></span>

![exemple de sortie d’effet](images/grayscale-effect.png)

## <a name="effect-properties"></a><span data-ttu-id="33aad-114">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="33aad-114">Effect properties</span></span>

<span data-ttu-id="33aad-115">Cet effet n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="33aad-115">This effect has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="33aad-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33aad-116">Requirements</span></span>



| <span data-ttu-id="33aad-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33aad-117">Requirement</span></span> | <span data-ttu-id="33aad-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="33aad-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="33aad-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33aad-119">Minimum supported client</span></span> | <span data-ttu-id="33aad-120">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="33aad-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="33aad-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33aad-121">Minimum supported server</span></span> | <span data-ttu-id="33aad-122">Applications de \[ Bureau Windows 10 \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="33aad-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="33aad-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="33aad-123">Header</span></span>                   | <span data-ttu-id="33aad-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="33aad-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="33aad-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33aad-125">Library</span></span>                  | <span data-ttu-id="33aad-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="33aad-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="33aad-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="33aad-127">Related topics</span></span>

* [<span data-ttu-id="33aad-128">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="33aad-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
