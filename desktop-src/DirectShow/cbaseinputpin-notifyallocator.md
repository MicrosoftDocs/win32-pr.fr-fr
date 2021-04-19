---
description: 'La méthode NotifyAllocator spécifie un allocateur pour la connexion. Cette méthode implémente la méthode IMemInputPin :: NotifyAllocator.'
ms.assetid: 16167bd5-2d33-4329-87ec-6a6c578e0060
title: Méthode CBaseInputPin. NotifyAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce5bc3cfe165b1adb6b5b970ca43d31c8ace98f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534804"
---
# <a name="cbaseinputpinnotifyallocator-method"></a><span data-ttu-id="338bf-104">Méthode CBaseInputPin. NotifyAllocator</span><span class="sxs-lookup"><span data-stu-id="338bf-104">CBaseInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="338bf-105">La `NotifyAllocator` méthode spécifie un allocateur pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="338bf-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="338bf-106">Cette méthode implémente la méthode [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .</span><span class="sxs-lookup"><span data-stu-id="338bf-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="338bf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="338bf-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="338bf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="338bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="338bf-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="338bf-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="338bf-110">Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="338bf-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="338bf-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="338bf-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="338bf-112">Indicateur qui spécifie si les exemples de cet allocateur sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="338bf-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="338bf-113">Si la **valeur est true**, les exemples sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="338bf-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="338bf-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="338bf-114">Return value</span></span>

<span data-ttu-id="338bf-115">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="338bf-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="338bf-116">Notes</span><span class="sxs-lookup"><span data-stu-id="338bf-116">Remarks</span></span>

<span data-ttu-id="338bf-117">Au cours de la connexion de code confidentiel, la broche de sortie choisit un allocateur et appelle cette méthode pour notifier la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="338bf-117">During the pin connection, the output pin chooses an allocator and calls this method to notify the input pin.</span></span> <span data-ttu-id="338bf-118">La broche de sortie peut utiliser l’allocateur que la broche d’entrée a proposée dans la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) , ou elle peut fournir son propre allocateur.</span><span class="sxs-lookup"><span data-stu-id="338bf-118">The output pin can use the allocator that the input pin proposed in the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method, or it can provide its own allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="338bf-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="338bf-119">Requirements</span></span>



| <span data-ttu-id="338bf-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="338bf-120">Requirement</span></span> | <span data-ttu-id="338bf-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="338bf-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="338bf-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="338bf-122">Header</span></span><br/>  | <dl> <span data-ttu-id="338bf-123"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="338bf-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="338bf-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="338bf-124">Library</span></span><br/> | <dl> <span data-ttu-id="338bf-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="338bf-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="338bf-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="338bf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338bf-127">**CBaseInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="338bf-127">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




