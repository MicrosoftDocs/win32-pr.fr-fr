---
description: Méthode de constructeur.
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
ms.openlocfilehash: 63e642182a0f968db5bda06e0af410d02455eb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529965"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="4d7ad-103">Constructeur CVideoTransformFilter. CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="4d7ad-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="4d7ad-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d7ad-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="4d7ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d7ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7ad-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="4d7ad-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="4d7ad-108">Chaîne contenant le nom de débogage du filtre.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="4d7ad-109">Pour plus d’informations, consultez [**CBaseObject :: CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="4d7ad-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d7ad-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="4d7ad-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4d7ad-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="4d7ad-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="4d7ad-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4d7ad-114">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="4d7ad-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="4d7ad-115">Identificateur de classe du filtre.</span><span class="sxs-lookup"><span data-stu-id="4d7ad-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d7ad-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d7ad-116">Requirements</span></span>



| <span data-ttu-id="4d7ad-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d7ad-117">Requirement</span></span> | <span data-ttu-id="4d7ad-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d7ad-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7ad-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d7ad-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4d7ad-120"><dt>Vtrans. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ad-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4d7ad-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d7ad-121">Library</span></span><br/> | <dl> <span data-ttu-id="4d7ad-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ad-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7ad-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d7ad-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7ad-124">**CVideoTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="4d7ad-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




