---
description: La méthode SetSyncSource notifie la classe de base de l’horloge de référence actuelle.
ms.assetid: 056385ac-682c-456e-9a5f-86490bd6e05f
title: Méthode CBaseStreamControl. SetSyncSource (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60832d1bf7ceca59089875f10579d52cf2cfec4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539491"
---
# <a name="cbasestreamcontrolsetsyncsource-method"></a><span data-ttu-id="82e2a-103">Méthode CBaseStreamControl. SetSyncSource</span><span class="sxs-lookup"><span data-stu-id="82e2a-103">CBaseStreamControl.SetSyncSource method</span></span>

<span data-ttu-id="82e2a-104">La `SetSyncSource` méthode notifie la classe de base de l’horloge de référence actuelle.</span><span class="sxs-lookup"><span data-stu-id="82e2a-104">The `SetSyncSource` method notifies the base class of the current reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e2a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82e2a-105">Syntax</span></span>


```C++
void SetSyncSource(
   IReferenceClock *pRefClock
);
```



## <a name="parameters"></a><span data-ttu-id="82e2a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82e2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82e2a-107">*pRefClock*</span><span class="sxs-lookup"><span data-stu-id="82e2a-107">*pRefClock*</span></span> 
</dt> <dd>

<span data-ttu-id="82e2a-108">Pointeur vers l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) de l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="82e2a-108">Pointer to the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface of the reference clock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82e2a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82e2a-109">Return value</span></span>

<span data-ttu-id="82e2a-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="82e2a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82e2a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="82e2a-111">Remarks</span></span>

<span data-ttu-id="82e2a-112">Appelez cette méthode à l’intérieur de la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) du filtre.</span><span class="sxs-lookup"><span data-stu-id="82e2a-112">Call this method from inside the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span> <span data-ttu-id="82e2a-113">La classe **CBaseStreamControl** utilise l’interface **IReferenceClock** pour s’assurer qu’elle n’ignore pas les exemples trop rapidement.</span><span class="sxs-lookup"><span data-stu-id="82e2a-113">The **CBaseStreamControl** class uses the **IReferenceClock** interface to ensure that it does not discard samples too quickly.</span></span>

## <a name="examples"></a><span data-ttu-id="82e2a-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="82e2a-114">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::SetSyncSource(IReferenceClock *pClock)
{
    // Note: It's OK if pClock is NULL.

    m_pMyPin->SetSyncSource(pClock);
    return CBaseFilter::SetSyncSource(pClock);
}
```



## <a name="requirements"></a><span data-ttu-id="82e2a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82e2a-115">Requirements</span></span>



| <span data-ttu-id="82e2a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82e2a-116">Requirement</span></span> | <span data-ttu-id="82e2a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="82e2a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e2a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="82e2a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="82e2a-119"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82e2a-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82e2a-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="82e2a-120">Library</span></span><br/> | <dl> <span data-ttu-id="82e2a-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="82e2a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82e2a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82e2a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e2a-123">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="82e2a-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




