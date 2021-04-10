---
title: Effet prémultiplier
description: Utilisez cet effet pour convertir une image de unpremultiplied alpha en valeur alpha prémultipliée.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- effet prémultiplier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942444"
---
# <a name="premultiply-effect"></a><span data-ttu-id="531d1-104">Effet prémultiplier</span><span class="sxs-lookup"><span data-stu-id="531d1-104">Premultiply effect</span></span>

<span data-ttu-id="531d1-105">Utilisez cet effet pour convertir une image de unpremultiplied alpha en valeur alpha prémultipliée.</span><span class="sxs-lookup"><span data-stu-id="531d1-105">Use this effect to convert an image from unpremultiplied alpha to premultiplied alpha.</span></span> <span data-ttu-id="531d1-106">L’effet remplace chaque pixel d’entrée `P = {R, G, B, A}` par `P' = {R*A, G*A, B*A, A}` dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="531d1-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R*A, G*A, B*A, A}` in the output.</span></span>

<span data-ttu-id="531d1-107">Cet effet n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="531d1-107">This effect has no properties.</span></span>

<span data-ttu-id="531d1-108">Le CLSID de cet effet est CLSID \_ D2D1Premultiply.</span><span class="sxs-lookup"><span data-stu-id="531d1-108">The CLSID for this effect is CLSID\_D2D1Premultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="531d1-109">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="531d1-109">Output bitmap</span></span>

<span data-ttu-id="531d1-110">La taille de la bitmap de sortie est la même que la taille de la bitmap d’entrée.</span><span class="sxs-lookup"><span data-stu-id="531d1-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="531d1-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="531d1-111">Requirements</span></span>



| <span data-ttu-id="531d1-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="531d1-112">Requirement</span></span> | <span data-ttu-id="531d1-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="531d1-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="531d1-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="531d1-114">Minimum supported client</span></span> | <span data-ttu-id="531d1-115">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="531d1-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="531d1-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="531d1-116">Minimum supported server</span></span> | <span data-ttu-id="531d1-117">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="531d1-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="531d1-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="531d1-118">Header</span></span>                   | <span data-ttu-id="531d1-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="531d1-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="531d1-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="531d1-120">Library</span></span>                  | <span data-ttu-id="531d1-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="531d1-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="531d1-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="531d1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="531d1-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="531d1-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
