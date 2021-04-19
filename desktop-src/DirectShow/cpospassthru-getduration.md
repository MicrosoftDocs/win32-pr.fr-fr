---
description: 'La méthode GetDuration récupère la durée du flux. Cette méthode implémente la méthode IMediaSeeking :: GetDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Méthode CPosPassThru. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9b533537c36ac7ec4c76289307368539482aa47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525930"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="bf830-104">Méthode CPosPassThru. GetDuration</span><span class="sxs-lookup"><span data-stu-id="bf830-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="bf830-105">La `GetDuration` méthode récupère la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="bf830-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="bf830-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="bf830-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf830-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf830-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="bf830-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf830-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf830-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="bf830-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="bf830-110">Pointeur vers une variable qui reçoit la durée, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="bf830-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf830-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf830-111">Return value</span></span>

<span data-ttu-id="bf830-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="bf830-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf830-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf830-113">Requirements</span></span>



| <span data-ttu-id="bf830-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf830-114">Requirement</span></span> | <span data-ttu-id="bf830-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf830-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf830-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf830-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bf830-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf830-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf830-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bf830-118">Library</span></span><br/> | <dl> <span data-ttu-id="bf830-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf830-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf830-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf830-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf830-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="bf830-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




