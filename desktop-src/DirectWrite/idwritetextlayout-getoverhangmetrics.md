---
title: Méthode IDWriteTextLayout GetOverhangMetrics
description: Retourne les surblocages (en DIP) de la disposition et de tous les objets qu’elle contient, y compris les glyphes de texte et les objets insérés.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Écriture directe de la méthode GetOverhangMetrics
- Méthode GetOverhangMetrics Write directe, interface IDWriteTextLayout
- Écriture directe de l’interface IDWriteTextLayout, méthode GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532634"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a><span data-ttu-id="513d1-106">IDWriteTextLayout :: GetOverhangMetrics, méthode</span><span class="sxs-lookup"><span data-stu-id="513d1-106">IDWriteTextLayout::GetOverhangMetrics method</span></span>

<span data-ttu-id="513d1-107">Retourne les surblocages (en DIP) de la disposition et de tous les objets qu’elle contient, y compris les glyphes de texte et les objets insérés.</span><span class="sxs-lookup"><span data-stu-id="513d1-107">Returns the overhangs (in DIPs) of the layout and all objects contained in it, including text glyphs and inline objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="513d1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="513d1-108">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="513d1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="513d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="513d1-110">*surblocages* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="513d1-110">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="513d1-111">Type : **[ **\_ \_ métriques de dépassement DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="513d1-111">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="513d1-112">Dépassements d’étendues visibles (en DIP) en dehors de la disposition.</span><span class="sxs-lookup"><span data-stu-id="513d1-112">Overshoots of visible extents (in DIPs) outside the layout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="513d1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="513d1-113">Return value</span></span>

<span data-ttu-id="513d1-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="513d1-114">Type: **HRESULT**</span></span>

<span data-ttu-id="513d1-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="513d1-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="513d1-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="513d1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="513d1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="513d1-117">Remarks</span></span>

<span data-ttu-id="513d1-118">Les traits de soulignement et les strikethroughs ne contribuent pas à la détermination de la boîte noire, car ils sont réellement dessinés par le convertisseur, ce qui est autorisé à les dessiner dans n’importe quel ensemble de styles.</span><span class="sxs-lookup"><span data-stu-id="513d1-118">Underlines and strikethroughs do not contribute to the black box determination, since these are actually drawn by the renderer, which is allowed to draw them in any variety of styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="513d1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="513d1-119">Requirements</span></span>



| <span data-ttu-id="513d1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="513d1-120">Requirement</span></span> | <span data-ttu-id="513d1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="513d1-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="513d1-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="513d1-122">Library</span></span><br/> | <dl> <span data-ttu-id="513d1-123"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="513d1-123"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="513d1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="513d1-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="513d1-125"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="513d1-125"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="513d1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="513d1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513d1-127">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="513d1-127">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="513d1-128">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="513d1-128">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

