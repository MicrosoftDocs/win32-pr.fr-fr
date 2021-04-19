---
description: 'La méthode SetSyncSource définit une horloge de référence pour l’objet. Cette méthode implémente la méthode IMediaFilter :: SetSyncSource.'
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Méthode CBaseMediaFilter. SetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541005"
---
# <a name="cbasemediafiltersetsyncsource-method"></a><span data-ttu-id="5086a-104">Méthode CBaseMediaFilter. SetSyncSource</span><span class="sxs-lookup"><span data-stu-id="5086a-104">CBaseMediaFilter.SetSyncSource method</span></span>

<span data-ttu-id="5086a-105">La `SetSyncSource` méthode définit une horloge de référence pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="5086a-105">The `SetSyncSource` method sets a reference clock for the object.</span></span> <span data-ttu-id="5086a-106">Cette méthode implémente la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="5086a-106">This method implements the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5086a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5086a-107">Syntax</span></span>


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a><span data-ttu-id="5086a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5086a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5086a-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="5086a-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="5086a-110">Pointeur vers l’interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) de l’horloge, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="5086a-110">Pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5086a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5086a-111">Return value</span></span>

<span data-ttu-id="5086a-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5086a-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="5086a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5086a-113">Requirements</span></span>



| <span data-ttu-id="5086a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5086a-114">Requirement</span></span> | <span data-ttu-id="5086a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5086a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5086a-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="5086a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5086a-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5086a-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5086a-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5086a-118">Library</span></span><br/> | <dl> <span data-ttu-id="5086a-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5086a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5086a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5086a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5086a-121">**CBaseMediaFilter, classe**</span><span class="sxs-lookup"><span data-stu-id="5086a-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




