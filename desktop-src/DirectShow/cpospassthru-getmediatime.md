---
description: 'Méthode CPosPassThru. GetMediaTime : la méthode GetMediaTime récupère les horodatages sur l’échantillon actuel.'
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Méthode CPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095257"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="5240d-103">Méthode CPosPassThru. GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="5240d-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="5240d-104">La `GetMediaTime` méthode récupère les horodatages sur l’échantillon actuel.</span><span class="sxs-lookup"><span data-stu-id="5240d-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="5240d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5240d-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="5240d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5240d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5240d-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="5240d-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="5240d-108">Pointeur vers une variable qui reçoit l’heure de début, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="5240d-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="5240d-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="5240d-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="5240d-110">Pointeur vers une variable qui reçoit l’heure de fin, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="5240d-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5240d-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5240d-111">Return value</span></span>

<span data-ttu-id="5240d-112">Retourne E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="5240d-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5240d-113">Notes </span><span class="sxs-lookup"><span data-stu-id="5240d-113">Remarks</span></span>

<span data-ttu-id="5240d-114">Substituez cette méthode si votre filtre met en cache les horodatages sur les échantillons qu’il reçoit.</span><span class="sxs-lookup"><span data-stu-id="5240d-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="5240d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5240d-115">Requirements</span></span>



| <span data-ttu-id="5240d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5240d-116">Requirement</span></span> | <span data-ttu-id="5240d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5240d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5240d-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="5240d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5240d-119"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5240d-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5240d-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5240d-120">Library</span></span><br/> | <dl> <span data-ttu-id="5240d-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5240d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5240d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5240d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5240d-123">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="5240d-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




