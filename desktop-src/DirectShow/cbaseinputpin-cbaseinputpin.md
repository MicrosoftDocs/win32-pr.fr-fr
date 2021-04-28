---
description: Méthode constructeur CBaseInputPin. CBaseInputPin.
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: Constructeur CBaseInputPin. CBaseInputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95a6dca29a9bdcaf978a54587035b34959d81719
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120047"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a><span data-ttu-id="84c8e-103">Constructeur CBaseInputPin. CBaseInputPin</span><span class="sxs-lookup"><span data-stu-id="84c8e-103">CBaseInputPin.CBaseInputPin constructor</span></span>

<span data-ttu-id="84c8e-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="84c8e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84c8e-105">Syntax</span></span>


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a><span data-ttu-id="84c8e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84c8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c8e-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="84c8e-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="84c8e-108">Chaîne contenant le nom de débogage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="84c8e-108">String containing the debug name of the object.</span></span> <span data-ttu-id="84c8e-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="84c8e-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="84c8e-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="84c8e-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="84c8e-111">Pointeur vers le filtre qui a créé ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="84c8e-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="84c8e-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="84c8e-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="84c8e-113">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="84c8e-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="84c8e-114">Il peut s’agir de la même section critique que le verrou de filtre, [**CBaseFilter :: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="84c8e-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="84c8e-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="84c8e-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="84c8e-116">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="84c8e-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="84c8e-117">*pPinName*</span><span class="sxs-lookup"><span data-stu-id="84c8e-117">*pPinName*</span></span> 
</dt> <dd>

<span data-ttu-id="84c8e-118">Chaîne de caractères larges contenant le nom du code confidentiel (également utilisé comme identificateur de code confidentiel).</span><span class="sxs-lookup"><span data-stu-id="84c8e-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84c8e-119">Notes </span><span class="sxs-lookup"><span data-stu-id="84c8e-119">Remarks</span></span>

<span data-ttu-id="84c8e-120">Tous les paramètres sont passés directement au constructeur [**CBasePin**](cbasepin-cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="84c8e-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin-cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c8e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84c8e-121">Requirements</span></span>



| <span data-ttu-id="84c8e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84c8e-122">Requirement</span></span> | <span data-ttu-id="84c8e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="84c8e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c8e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="84c8e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="84c8e-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84c8e-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="84c8e-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="84c8e-126">Library</span></span><br/> | <dl> <span data-ttu-id="84c8e-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="84c8e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84c8e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84c8e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c8e-129">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="84c8e-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




