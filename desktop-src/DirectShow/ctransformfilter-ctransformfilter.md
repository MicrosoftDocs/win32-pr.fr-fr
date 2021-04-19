---
description: Méthode de constructeur.
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Constructeur CTransformFilter. CTransformFilter (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525295"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="f72c1-103">Constructeur CTransformFilter. CTransformFilter</span><span class="sxs-lookup"><span data-stu-id="f72c1-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="f72c1-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f72c1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f72c1-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="f72c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f72c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72c1-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="f72c1-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="f72c1-108">Chaîne contenant le nom de débogage du filtre.</span><span class="sxs-lookup"><span data-stu-id="f72c1-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="f72c1-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="f72c1-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="f72c1-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="f72c1-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f72c1-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="f72c1-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="f72c1-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="f72c1-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="f72c1-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f72c1-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f72c1-114">*identificateur*</span><span class="sxs-lookup"><span data-stu-id="f72c1-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="f72c1-115">Identificateur de classe du filtre.</span><span class="sxs-lookup"><span data-stu-id="f72c1-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f72c1-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f72c1-116">Remarks</span></span>

<span data-ttu-id="f72c1-117">Le constructeur ne crée pas les codes confidentiels du filtre.</span><span class="sxs-lookup"><span data-stu-id="f72c1-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="f72c1-118">Cela se produit lors du premier appel à la méthode [**GetPin**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="f72c1-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="f72c1-119">Le constructeur initialise les variables de membre [**m \_ pInput**](ctransformfilter-m-pinput.md) et [**m \_ pOutput**](ctransformfilter-m-poutput.md) à la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f72c1-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f72c1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f72c1-120">Requirements</span></span>



| <span data-ttu-id="f72c1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f72c1-121">Requirement</span></span> | <span data-ttu-id="f72c1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f72c1-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72c1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f72c1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f72c1-124"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f72c1-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f72c1-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f72c1-125">Library</span></span><br/> | <dl> <span data-ttu-id="f72c1-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f72c1-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f72c1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f72c1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72c1-128">**CTransformFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="f72c1-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




