---
title: Effet de métadonnées d’opacité
description: Vous pouvez utiliser cet effet pour marquer une zone d’une image d’entrée comme opaque, afin que les optimisations de rendu internes au graphique soient possibles.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105448"
---
# <a name="opacity-metadata-effect"></a><span data-ttu-id="fc9e0-103">Effet de métadonnées d’opacité</span><span class="sxs-lookup"><span data-stu-id="fc9e0-103">Opacity metadata effect</span></span>

<span data-ttu-id="fc9e0-104">Vous pouvez utiliser cet effet pour marquer une zone d’une image d’entrée comme opaque, afin que les optimisations de rendu internes au graphique soient possibles.</span><span class="sxs-lookup"><span data-stu-id="fc9e0-104">You can use this effect to mark an area of an input image as opaque, so internal rendering optimizations to the graph are possible.</span></span>

> [!Note]  
> <span data-ttu-id="fc9e0-105">Cet effet ne modifie pas l’image elle-même pour qu’elle soit opaque.</span><span class="sxs-lookup"><span data-stu-id="fc9e0-105">This effect doesn't modify the image itself to be opaque.</span></span> <span data-ttu-id="fc9e0-106">Il modifie les données associées à l’image afin que le convertisseur suppose que la région spécifiée est opaque.</span><span class="sxs-lookup"><span data-stu-id="fc9e0-106">It modifies data associated with the image so the renderer assumes the specified region is opaque.</span></span>

 

<span data-ttu-id="fc9e0-107">Le CLSID de cet effet est CLSID \_ D2D1OpacityMetadata.</span><span class="sxs-lookup"><span data-stu-id="fc9e0-107">The CLSID for this effect is CLSID\_D2D1OpacityMetadata.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="fc9e0-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="fc9e0-108">Effect properties</span></span>



| <span data-ttu-id="fc9e0-109">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="fc9e0-109">Display name and index enumeration</span></span>                                                 | <span data-ttu-id="fc9e0-110">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fc9e0-110">Type and default value</span></span>                                                             | <span data-ttu-id="fc9e0-111">Description</span><span class="sxs-lookup"><span data-stu-id="fc9e0-111">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9e0-112">OutputRect</span><span class="sxs-lookup"><span data-stu-id="fc9e0-112">OutputRect</span></span><br/> <span data-ttu-id="fc9e0-113">D2D1 \_ OPACITYMETADATA \_ prop \_ , \_ rectangle opaque d’entrée \_</span><span class="sxs-lookup"><span data-stu-id="fc9e0-113">D2D1\_OPACITYMETADATA\_PROP\_INPUT\_OPAQUE\_RECT</span></span> <br/> | <span data-ttu-id="fc9e0-114">D2D1 \_ vecteur \_ 4F</span><span class="sxs-lookup"><span data-stu-id="fc9e0-114">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="fc9e0-115">(-FLT \_ MAX,-FLT \_ Max, FLT Max, \_ flt \_ Max.)</span><span class="sxs-lookup"><span data-stu-id="fc9e0-115">(-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX)</span></span> <br/> | <span data-ttu-id="fc9e0-116">Partie de l’image source qui est opaque.</span><span class="sxs-lookup"><span data-stu-id="fc9e0-116">The portion of the source image that is opaque.</span></span> <span data-ttu-id="fc9e0-117">La valeur par défaut est la totalité de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fc9e0-117">The default is the entire input image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fc9e0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc9e0-118">Requirements</span></span>



| <span data-ttu-id="fc9e0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc9e0-119">Requirement</span></span> | <span data-ttu-id="fc9e0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc9e0-120">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9e0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc9e0-121">Minimum supported client</span></span> | <span data-ttu-id="fc9e0-122">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="fc9e0-122">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fc9e0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc9e0-123">Minimum supported server</span></span> | <span data-ttu-id="fc9e0-124">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="fc9e0-124">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fc9e0-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc9e0-125">Header</span></span>                   | <span data-ttu-id="fc9e0-126">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="fc9e0-126">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="fc9e0-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc9e0-127">Library</span></span>                  | <span data-ttu-id="fc9e0-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="fc9e0-128">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="fc9e0-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc9e0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc9e0-130">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="fc9e0-130">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

