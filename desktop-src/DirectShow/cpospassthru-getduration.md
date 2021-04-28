---
description: 'Méthode CPosPassThru. GetDuration : la méthode GetDuration récupère la durée du flux. Cette méthode implémente la méthode IMediaSeeking :: GetDuration.'
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
ms.openlocfilehash: 0b0af7bfaca405ed52a4e3c5a63c18b4bc087ba3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085577"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="4becf-104">Méthode CPosPassThru. GetDuration</span><span class="sxs-lookup"><span data-stu-id="4becf-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="4becf-105">La `GetDuration` méthode récupère la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="4becf-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="4becf-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="4becf-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4becf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4becf-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="4becf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4becf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4becf-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="4becf-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="4becf-110">Pointeur vers une variable qui reçoit la durée, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="4becf-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4becf-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4becf-111">Return value</span></span>

<span data-ttu-id="4becf-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="4becf-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4becf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4becf-113">Requirements</span></span>



| <span data-ttu-id="4becf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4becf-114">Requirement</span></span> | <span data-ttu-id="4becf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4becf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4becf-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4becf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4becf-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4becf-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4becf-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4becf-118">Library</span></span><br/> | <dl> <span data-ttu-id="4becf-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4becf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4becf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4becf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4becf-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="4becf-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




