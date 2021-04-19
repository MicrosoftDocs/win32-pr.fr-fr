---
description: Méthode de constructeur.
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: Constructeur CBaseOutputPin. CBaseOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0461c5056ee48caa19f21d1fcb8fcf1636157d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540039"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a><span data-ttu-id="ecfa5-103">Constructeur CBaseOutputPin. CBaseOutputPin</span><span class="sxs-lookup"><span data-stu-id="ecfa5-103">CBaseOutputPin.CBaseOutputPin constructor</span></span>

<span data-ttu-id="ecfa5-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ecfa5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecfa5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecfa5-105">Syntax</span></span>


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="ecfa5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecfa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecfa5-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="ecfa5-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="ecfa5-108">Chaîne contenant le nom de débogage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ecfa5-108">String containing the debug name of the object.</span></span> <span data-ttu-id="ecfa5-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="ecfa5-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecfa5-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="ecfa5-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="ecfa5-111">Pointeur vers le filtre qui a créé ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="ecfa5-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="ecfa5-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="ecfa5-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="ecfa5-113">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="ecfa5-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="ecfa5-114">Il peut s’agir de la même section critique que le verrou de filtre, [**CBaseFilter :: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="ecfa5-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="ecfa5-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="ecfa5-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ecfa5-116">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ecfa5-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="ecfa5-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="ecfa5-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ecfa5-118">Chaîne de caractères larges contenant le nom du code confidentiel (également utilisé comme identificateur de code confidentiel).</span><span class="sxs-lookup"><span data-stu-id="ecfa5-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecfa5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ecfa5-119">Remarks</span></span>

<span data-ttu-id="ecfa5-120">Tous les paramètres sont passés directement au constructeur [**CBasePin**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="ecfa5-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecfa5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecfa5-121">Requirements</span></span>



| <span data-ttu-id="ecfa5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecfa5-122">Requirement</span></span> | <span data-ttu-id="ecfa5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecfa5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfa5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecfa5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ecfa5-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecfa5-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ecfa5-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ecfa5-126">Library</span></span><br/> | <dl> <span data-ttu-id="ecfa5-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ecfa5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecfa5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecfa5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecfa5-129">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="ecfa5-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




