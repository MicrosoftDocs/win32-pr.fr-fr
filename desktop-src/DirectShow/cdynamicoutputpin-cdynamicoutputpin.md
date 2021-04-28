---
description: Méthode constructeur CDynamicOutputPin. CDynamicOutputPin.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Constructeur CDynamicOutputPin. CDynamicOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099307"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="ca474-103">Constructeur CDynamicOutputPin. CDynamicOutputPin</span><span class="sxs-lookup"><span data-stu-id="ca474-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="ca474-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ca474-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca474-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca474-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="ca474-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca474-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca474-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="ca474-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="ca474-108">Pointeur vers une chaîne contenant le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca474-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="ca474-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="ca474-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca474-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="ca474-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="ca474-111">Pointeur vers le filtre qui a créé ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="ca474-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="ca474-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="ca474-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="ca474-113">Pointeur vers un verrou [**CCritSec**](ccritsec.md) , utilisé pour sérialiser les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="ca474-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="ca474-114">Utilisez la même section critique que le verrou de filtre, [ **CBaseFilter :: m \_ pLock**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="ca474-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="ca474-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="ca474-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ca474-116">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ca474-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="ca474-117">Initialisez la valeur sur \_ OK avant de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca474-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="ca474-118">La valeur est modifiée uniquement si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="ca474-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="ca474-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="ca474-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ca474-120">Pointeur vers une chaîne de caractères larges contenant l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="ca474-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="ca474-121">Pour plus d’informations, consultez [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span><span class="sxs-lookup"><span data-stu-id="ca474-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca474-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca474-122">Requirements</span></span>



| <span data-ttu-id="ca474-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca474-123">Requirement</span></span> | <span data-ttu-id="ca474-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca474-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca474-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca474-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ca474-126"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca474-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca474-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ca474-127">Library</span></span><br/> | <dl> <span data-ttu-id="ca474-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ca474-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca474-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca474-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca474-130">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="ca474-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




