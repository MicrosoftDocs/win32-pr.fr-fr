---
description: 'La méthode GetSyncSource récupère l’horloge de référence utilisée par l’objet. Cette méthode implémente la méthode IMediaFilter :: GetSyncSource.'
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Méthode CBaseMediaFilter. GetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541020"
---
# <a name="cbasemediafiltergetsyncsource-method"></a><span data-ttu-id="05905-104">Méthode CBaseMediaFilter. GetSyncSource</span><span class="sxs-lookup"><span data-stu-id="05905-104">CBaseMediaFilter.GetSyncSource method</span></span>

<span data-ttu-id="05905-105">La `GetSyncSource` méthode récupère l’horloge de référence utilisée par l’objet.</span><span class="sxs-lookup"><span data-stu-id="05905-105">The `GetSyncSource` method retrieves the reference clock that the object is using.</span></span> <span data-ttu-id="05905-106">Cette méthode implémente la méthode [**IMediaFilter :: GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="05905-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05905-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05905-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="05905-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05905-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05905-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="05905-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="05905-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="05905-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05905-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05905-111">Return value</span></span>

<span data-ttu-id="05905-112">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="05905-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="05905-113">Notes</span><span class="sxs-lookup"><span data-stu-id="05905-113">Remarks</span></span>

<span data-ttu-id="05905-114">Si l’objet n’utilise pas une horloge de référence, *\* pClock* a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="05905-114">If the object is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="05905-115">Lorsque la méthode est retournée, si *\* pClock* est non **null**, l’interface **IReferenceClock** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="05905-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="05905-116">Veillez à le libérer lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="05905-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="05905-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05905-117">Requirements</span></span>



| <span data-ttu-id="05905-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05905-118">Requirement</span></span> | <span data-ttu-id="05905-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="05905-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05905-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="05905-120">Header</span></span><br/>  | <dl> <span data-ttu-id="05905-121"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05905-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="05905-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05905-122">Library</span></span><br/> | <dl> <span data-ttu-id="05905-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="05905-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05905-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05905-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05905-125">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="05905-125">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




