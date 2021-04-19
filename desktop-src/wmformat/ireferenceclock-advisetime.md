---
title: Méthode IReferenceClock AdviseTime
description: La méthode AdviseTime demande une notification asynchrone indiquant qu’une heure s’est écoulée.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Méthode AdviseTime format Windows Media
- Méthode AdviseTime format Windows Media, interface IReferenceClock
- Interface IReferenceClock Windows Media format, méthode AdviseTime
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510853"
---
# <a name="ireferenceclockadvisetime-method"></a><span data-ttu-id="68e7b-106">IReferenceClock :: AdviseTime, méthode</span><span class="sxs-lookup"><span data-stu-id="68e7b-106">IReferenceClock::AdviseTime method</span></span>

<span data-ttu-id="68e7b-107">La méthode **AdviseTime** demande une notification asynchrone indiquant qu’une heure s’est écoulée.</span><span class="sxs-lookup"><span data-stu-id="68e7b-107">The **AdviseTime** method requests an asynchronous notification that a time has elapsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e7b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68e7b-108">Syntax</span></span>


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="68e7b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68e7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68e7b-110">*rtBaseTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68e7b-110">*rtBaseTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68e7b-111">Temps de référence de base, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="68e7b-111">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="68e7b-112">*rtStreamTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68e7b-112">*rtStreamTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68e7b-113">Temps de décalage du flux, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="68e7b-113">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="68e7b-114">*hEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68e7b-114">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68e7b-115">Handle vers un événement, créé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="68e7b-115">Handle to an event, created by the caller.</span></span> <span data-ttu-id="68e7b-116">Cet événement est signalé lorsque la durée spécifiée est écoulée.</span><span class="sxs-lookup"><span data-stu-id="68e7b-116">This event will be signaled when the time specified elapses.</span></span>

</dd> <dt>

<span data-ttu-id="68e7b-117">*pdwAdviseCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="68e7b-117">*pdwAdviseCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68e7b-118">Pointeur vers une variable qui reçoit un identificateur pour la demande.</span><span class="sxs-lookup"><span data-stu-id="68e7b-118">Pointer to a variable that receives an identifier for the request.</span></span> <span data-ttu-id="68e7b-119">Il est utilisé pour identifier cet appel à **AdviseTime** à l’avenir, par exemple, pour annuler la demande.</span><span class="sxs-lookup"><span data-stu-id="68e7b-119">This is used to identify this call to **AdviseTime** in the future for example, to cancel the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68e7b-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68e7b-120">Return value</span></span>

<span data-ttu-id="68e7b-121">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="68e7b-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="68e7b-122">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="68e7b-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="68e7b-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="68e7b-123">Return code</span></span>                                                                               | <span data-ttu-id="68e7b-124">Description</span><span class="sxs-lookup"><span data-stu-id="68e7b-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="68e7b-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="68e7b-125"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="68e7b-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="68e7b-126">The method succeeded.</span></span><br/>                        |
| <dl> <span data-ttu-id="68e7b-127"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="68e7b-127"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="68e7b-128">Le paramètre *pdwAdviseCookie* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="68e7b-128">The *pdwAdviseCookie* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="68e7b-129"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="68e7b-129"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="68e7b-130">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="68e7b-130">Unspecified failure.</span></span><br/>                         |



 

## <a name="see-also"></a><span data-ttu-id="68e7b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68e7b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e7b-132">**Interface IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="68e7b-132">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





