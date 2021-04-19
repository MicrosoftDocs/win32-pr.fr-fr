---
description: 'La méthode GetAvailable récupère la plage de temps pendant laquelle la recherche est efficace. Cette méthode implémente la méthode IMediaSeeking :: GetAvailable.'
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Méthode CPosPassThru. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542551"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="dd29a-104">Méthode CPosPassThru. GetAvailable</span><span class="sxs-lookup"><span data-stu-id="dd29a-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="dd29a-105">La `GetAvailable` méthode récupère la plage de temps pendant laquelle la recherche est efficace.</span><span class="sxs-lookup"><span data-stu-id="dd29a-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="dd29a-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="dd29a-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd29a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd29a-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="dd29a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd29a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd29a-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="dd29a-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="dd29a-110">Pointeur vers une variable qui reçoit l’heure la plus précoce pour une recherche efficace.</span><span class="sxs-lookup"><span data-stu-id="dd29a-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="dd29a-111">*Plaque*</span><span class="sxs-lookup"><span data-stu-id="dd29a-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="dd29a-112">Pointeur vers une variable qui reçoit l’heure la plus récente pour une recherche efficace.</span><span class="sxs-lookup"><span data-stu-id="dd29a-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd29a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd29a-113">Return value</span></span>

<span data-ttu-id="dd29a-114">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="dd29a-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd29a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd29a-115">Requirements</span></span>



| <span data-ttu-id="dd29a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd29a-116">Requirement</span></span> | <span data-ttu-id="dd29a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd29a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd29a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd29a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dd29a-119"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd29a-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dd29a-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd29a-120">Library</span></span><br/> | <dl> <span data-ttu-id="dd29a-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dd29a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd29a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd29a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd29a-123">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="dd29a-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




