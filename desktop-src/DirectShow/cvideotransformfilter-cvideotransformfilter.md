---
description: Méthode constructeur CVideoTransformFilter. CVideoTransformFilter.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Constructeur CVideoTransformFilter. CVideoTransformFilter (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59609e09b252e56aded1669264bb98cdbe823e89
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084587"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="f8188-103">Constructeur CVideoTransformFilter. CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="f8188-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="f8188-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f8188-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8188-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8188-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="f8188-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8188-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8188-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f8188-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f8188-108">Chaîne contenant le nom de débogage du filtre.</span><span class="sxs-lookup"><span data-stu-id="f8188-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="f8188-109">Pour plus d’informations, consultez [**CBaseObject :: CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="f8188-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8188-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="f8188-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f8188-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="f8188-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="f8188-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="f8188-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="f8188-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f8188-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f8188-114">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="f8188-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="f8188-115">Identificateur de classe du filtre.</span><span class="sxs-lookup"><span data-stu-id="f8188-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8188-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8188-116">Requirements</span></span>



| <span data-ttu-id="f8188-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8188-117">Requirement</span></span> | <span data-ttu-id="f8188-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8188-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8188-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8188-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f8188-120"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8188-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f8188-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8188-121">Library</span></span><br/> | <dl> <span data-ttu-id="f8188-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f8188-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8188-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8188-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8188-124">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f8188-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




