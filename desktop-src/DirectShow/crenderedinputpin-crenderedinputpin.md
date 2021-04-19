---
description: Méthode de constructeur.
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: Constructeur CRenderedInputPin. CRenderedInputPin (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee1ec8944d56d2aa6f46e59ac5034969ca77ea19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543811"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="5be45-103">Constructeur CRenderedInputPin. CRenderedInputPin</span><span class="sxs-lookup"><span data-stu-id="5be45-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="5be45-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="5be45-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be45-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5be45-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="5be45-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5be45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5be45-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="5be45-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="5be45-108">Chaîne contenant le nom de débogage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5be45-108">String containing the debug name of the object.</span></span> <span data-ttu-id="5be45-109">Pour plus d’informations, consultez [**CBaseObject, classe**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="5be45-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="5be45-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="5be45-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="5be45-111">Pointeur vers le filtre qui a créé ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="5be45-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="5be45-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="5be45-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="5be45-113">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="5be45-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="5be45-114">Il peut s’agir de la même section critique que le verrou de filtre, [**CBaseFilter :: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="5be45-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="5be45-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="5be45-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5be45-116">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="5be45-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="5be45-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="5be45-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5be45-118">Chaîne de caractères larges contenant le nom du code confidentiel (également utilisé comme identificateur de code confidentiel).</span><span class="sxs-lookup"><span data-stu-id="5be45-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5be45-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5be45-119">Requirements</span></span>



| <span data-ttu-id="5be45-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5be45-120">Requirement</span></span> | <span data-ttu-id="5be45-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5be45-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5be45-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5be45-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5be45-123"><dt>Amextra. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5be45-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5be45-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5be45-124">Library</span></span><br/> | <dl> <span data-ttu-id="5be45-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5be45-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5be45-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5be45-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be45-127">**CRenderedInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="5be45-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




