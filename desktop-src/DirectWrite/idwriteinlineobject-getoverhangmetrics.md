---
title: Méthode IDWriteInlineObject GetOverhangMetrics
description: IDWriteTextLayout appelle cette fonction de rappel pour récupérer les étendues visibles (en DIP) de l’objet Inline. Dans le cas d’une image bitmap simple, sans remplissage ni dépassement, tous les surblocages sont simplement des zéros.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Écriture directe de la méthode GetOverhangMetrics
- Méthode GetOverhangMetrics Write directe, interface IDWriteInlineObject
- Écriture directe de l’interface IDWriteInlineObject, méthode GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538132"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a><span data-ttu-id="904a0-107">IDWriteInlineObject :: GetOverhangMetrics, méthode</span><span class="sxs-lookup"><span data-stu-id="904a0-107">IDWriteInlineObject::GetOverhangMetrics method</span></span>

<span data-ttu-id="904a0-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) appelle cette fonction de rappel pour récupérer les étendues visibles (en DIP) de l’objet Inline.</span><span class="sxs-lookup"><span data-stu-id="904a0-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the visible extents (in DIPs) of the inline object.</span></span> <span data-ttu-id="904a0-109">Dans le cas d’une image bitmap simple, sans remplissage ni dépassement, tous les surblocages sont simplement des zéros.</span><span class="sxs-lookup"><span data-stu-id="904a0-109">In the case of a simple bitmap, with no padding and no overhang, all the overhangs will simply be zeroes.</span></span>

<span data-ttu-id="904a0-110">Les surblocages doivent être retournés par rapport à la taille signalée de l’objet (consultez mesures de l' [**\_ \_ objet \_ inline DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) et ne doivent pas être ajustées à la ligne de base.</span><span class="sxs-lookup"><span data-stu-id="904a0-110">The overhangs should be returned relative to the reported size of the object (see [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)), and should not be baseline adjusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="904a0-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="904a0-111">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="904a0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="904a0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="904a0-113">*surblocages* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="904a0-113">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="904a0-114">Type : **[ **\_ \_ métriques de dépassement DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="904a0-114">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="904a0-115">Dépassement des étendues visibles (en DIP) à l’extérieur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="904a0-115">Overshoot of visible extents (in DIPs) outside the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="904a0-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="904a0-116">Return value</span></span>

<span data-ttu-id="904a0-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="904a0-117">Type: **HRESULT**</span></span>

<span data-ttu-id="904a0-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="904a0-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="904a0-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="904a0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="904a0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="904a0-120">Requirements</span></span>



| <span data-ttu-id="904a0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="904a0-121">Requirement</span></span> | <span data-ttu-id="904a0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="904a0-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="904a0-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="904a0-123">Library</span></span><br/> | <dl> <span data-ttu-id="904a0-124"><dt>DWrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="904a0-124"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="904a0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="904a0-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="904a0-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="904a0-126"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904a0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="904a0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904a0-128">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="904a0-128">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[<span data-ttu-id="904a0-129">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="904a0-129">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

