---
description: 'La méthode GetAvailable récupère la plage de temps pendant laquelle la recherche est efficace. Cette méthode implémente la méthode IMediaSeeking :: GetAvailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Méthode CSourceSeeking. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540319"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="3909c-104">Méthode CSourceSeeking. GetAvailable</span><span class="sxs-lookup"><span data-stu-id="3909c-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="3909c-105">La `GetAvailable` méthode récupère la plage de temps pendant laquelle la recherche est efficace.</span><span class="sxs-lookup"><span data-stu-id="3909c-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="3909c-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="3909c-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3909c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3909c-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="3909c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3909c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3909c-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="3909c-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="3909c-110">Pointeur vers une variable qui reçoit l’heure la plus précoce pour une recherche efficace.</span><span class="sxs-lookup"><span data-stu-id="3909c-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="3909c-111">La variable a la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3909c-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3909c-112">*Plaque*</span><span class="sxs-lookup"><span data-stu-id="3909c-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="3909c-113">Pointeur vers une variable qui reçoit l’heure la plus récente pour une recherche efficace.</span><span class="sxs-lookup"><span data-stu-id="3909c-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="3909c-114">La variable est définie sur la valeur de la variable membre [**CSourceSeeking :: m \_ rtDuration**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="3909c-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3909c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3909c-115">Return value</span></span>

<span data-ttu-id="3909c-116">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3909c-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="3909c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3909c-117">Requirements</span></span>



| <span data-ttu-id="3909c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3909c-118">Requirement</span></span> | <span data-ttu-id="3909c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3909c-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3909c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3909c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3909c-121"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3909c-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3909c-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3909c-122">Library</span></span><br/> | <dl> <span data-ttu-id="3909c-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3909c-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3909c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3909c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3909c-125">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="3909c-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




