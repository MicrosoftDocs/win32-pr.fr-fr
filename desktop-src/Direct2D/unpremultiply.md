---
title: Effet Unpremultiply
description: Utilisez cet effet pour convertir une image de l’alpha prémultiplié en unpremultiplied alpha.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- effet unpremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385060"
---
# <a name="unpremultiply-effect"></a><span data-ttu-id="39413-104">Effet Unpremultiply</span><span class="sxs-lookup"><span data-stu-id="39413-104">Unpremultiply effect</span></span>

<span data-ttu-id="39413-105">Utilisez cet effet pour convertir une image de l’alpha prémultiplié en unpremultiplied alpha.</span><span class="sxs-lookup"><span data-stu-id="39413-105">Use this effect to convert an image from premultiplied alpha to unpremultiplied alpha.</span></span> <span data-ttu-id="39413-106">L’effet remplace chaque pixel d’entrée `P = {R, G, B, A}` par `P' = {R/A, G/A, B/A, A}` dans la sortie.</span><span class="sxs-lookup"><span data-stu-id="39413-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R/A, G/A, B/A, A}` in the output.</span></span>

<span data-ttu-id="39413-107">Cet effet n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="39413-107">This effect has no properties.</span></span>

<span data-ttu-id="39413-108">Le CLSID de cet effet est CLSID \_ D2D1Unpremultiply.</span><span class="sxs-lookup"><span data-stu-id="39413-108">The CLSID for this effect is CLSID\_D2D1Unpremultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="39413-109">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="39413-109">Output bitmap</span></span>

<span data-ttu-id="39413-110">La taille de la bitmap de sortie est la même que la taille de la bitmap d’entrée.</span><span class="sxs-lookup"><span data-stu-id="39413-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="39413-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39413-111">Requirements</span></span>



| <span data-ttu-id="39413-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39413-112">Requirement</span></span> | <span data-ttu-id="39413-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="39413-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39413-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39413-114">Minimum supported client</span></span> | <span data-ttu-id="39413-115">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="39413-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="39413-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39413-116">Minimum supported server</span></span> | <span data-ttu-id="39413-117">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="39413-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="39413-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="39413-118">Header</span></span>                   | <span data-ttu-id="39413-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="39413-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="39413-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39413-120">Library</span></span>                  | <span data-ttu-id="39413-121">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="39413-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="39413-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39413-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39413-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="39413-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
