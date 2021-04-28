---
description: Méthode constructeur CRenderedInputPin. CRenderedInputPin.
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
ms.openlocfilehash: 4bd8e864531604fb36c2abe0bcd57ac5b3a9c869
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085397"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="bab63-103">Constructeur CRenderedInputPin. CRenderedInputPin</span><span class="sxs-lookup"><span data-stu-id="bab63-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="bab63-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="bab63-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab63-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bab63-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="bab63-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bab63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab63-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="bab63-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="bab63-108">Chaîne contenant le nom de débogage de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bab63-108">String containing the debug name of the object.</span></span> <span data-ttu-id="bab63-109">Pour plus d’informations, consultez [**CBaseObject, classe**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="bab63-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab63-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="bab63-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="bab63-111">Pointeur vers le filtre qui a créé ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="bab63-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="bab63-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="bab63-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="bab63-113">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="bab63-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="bab63-114">Il peut s’agir de la même section critique que le verrou de filtre, [**CBaseFilter :: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="bab63-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="bab63-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="bab63-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="bab63-116">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="bab63-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="bab63-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="bab63-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="bab63-118">Chaîne de caractères larges contenant le nom du code confidentiel (également utilisé comme identificateur de code confidentiel).</span><span class="sxs-lookup"><span data-stu-id="bab63-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bab63-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bab63-119">Requirements</span></span>



| <span data-ttu-id="bab63-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bab63-120">Requirement</span></span> | <span data-ttu-id="bab63-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bab63-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bab63-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bab63-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bab63-123"><dt>Amextra. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bab63-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bab63-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bab63-124">Library</span></span><br/> | <dl> <span data-ttu-id="bab63-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bab63-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab63-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bab63-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab63-127">**CRenderedInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="bab63-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




