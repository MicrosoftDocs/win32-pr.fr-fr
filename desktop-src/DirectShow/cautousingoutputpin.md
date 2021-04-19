---
description: La classe CAutoUsingOutputPin obtient et libère l’accès à un objet CDynamicOutputPin.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: CAutoUsingOutputPin, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544482"
---
# <a name="cautousingoutputpin-class"></a><span data-ttu-id="7b4a3-103">CAutoUsingOutputPin, classe</span><span class="sxs-lookup"><span data-stu-id="7b4a3-103">CAutoUsingOutputPin class</span></span>

<span data-ttu-id="7b4a3-104">La classe **CAutoUsingOutputPin** obtient et libère l’accès à un objet [**CDynamicOutputPin**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="7b4a3-104">The **CAutoUsingOutputPin** class obtains and releases access to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

<span data-ttu-id="7b4a3-105">**CAutoUsingOutputPin** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b4a3-105">**CAutoUsingOutputPin** has these types of members:</span></span>



| <span data-ttu-id="7b4a3-106">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="7b4a3-106">Public Methods</span></span>                                                           | <span data-ttu-id="7b4a3-107">Description</span><span class="sxs-lookup"><span data-stu-id="7b4a3-107">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="7b4a3-108">**CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7b4a3-108">**CAutoUsingOutputPin**</span></span>](cautousingoutputpin-cautousingoutputpin.md)   | <span data-ttu-id="7b4a3-109">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="7b4a3-109">Constructor method.</span></span> <span data-ttu-id="7b4a3-110">Obtient l’accès au code confidentiel spécifié.</span><span class="sxs-lookup"><span data-stu-id="7b4a3-110">Obtains access to the specified pin.</span></span> |
| [<span data-ttu-id="7b4a3-111">**~ CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7b4a3-111">**~CAutoUsingOutputPin**</span></span>](cautousingoutputpin--cautousingoutputpin.md) | <span data-ttu-id="7b4a3-112">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="7b4a3-112">Destructor method.</span></span> <span data-ttu-id="7b4a3-113">Obtient l’accès au code confidentiel spécifié.</span><span class="sxs-lookup"><span data-stu-id="7b4a3-113">Obtains access to the specified pin.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="7b4a3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7b4a3-114">Remarks</span></span>

<span data-ttu-id="7b4a3-115">Lorsque certaines méthodes sont appelées sur [**CDynamicOutputPin**](cdynamicoutputpin.md), l’appelant doit obtenir l’accès au code confidentiel, puis libérer cet accès.</span><span class="sxs-lookup"><span data-stu-id="7b4a3-115">When certain methods are called on [**CDynamicOutputPin**](cdynamicoutputpin.md), the caller must obtain access to the pin and then release that access.</span></span> <span data-ttu-id="7b4a3-116">Pour obtenir l’accès, l’appelant utilise la méthode [**CDynamicOutputPin :: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="7b4a3-116">To obtain access, the caller uses the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method.</span></span> <span data-ttu-id="7b4a3-117">Pour libérer l’accès, elle appelle la méthode [**CDynamicOutputPin :: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="7b4a3-117">To release access, it calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method.</span></span> <span data-ttu-id="7b4a3-118">La classe **CAutoUsingOutputPin** est une classe d’assistance qui gère ces tâches dans ses méthodes de constructeur et de destructeur.</span><span class="sxs-lookup"><span data-stu-id="7b4a3-118">The **CAutoUsingOutputPin** class is a helper class that handles these tasks in its constructor and destructor methods.</span></span> <span data-ttu-id="7b4a3-119">L’exemple de code suivant montre comment utiliser cette classe :</span><span class="sxs-lookup"><span data-stu-id="7b4a3-119">The following code example shows how to use this class:</span></span>


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a><span data-ttu-id="7b4a3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b4a3-120">Requirements</span></span>



| <span data-ttu-id="7b4a3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b4a3-121">Requirement</span></span> | <span data-ttu-id="7b4a3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b4a3-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4a3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b4a3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7b4a3-124"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a3-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7b4a3-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7b4a3-125">Library</span></span><br/> | <dl> <span data-ttu-id="7b4a3-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7b4a3-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4a3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b4a3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4a3-128">Référence de classe de base</span><span class="sxs-lookup"><span data-stu-id="7b4a3-128">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

 




