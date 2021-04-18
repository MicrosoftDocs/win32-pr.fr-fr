---
description: La méthode DecideAllocator sélectionne un allocateur de mémoire.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Méthode CBaseOutputPin. DecideAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540337"
---
# <a name="cbaseoutputpindecideallocator-method"></a><span data-ttu-id="bb1ca-103">Méthode CBaseOutputPin. DecideAllocator</span><span class="sxs-lookup"><span data-stu-id="bb1ca-103">CBaseOutputPin.DecideAllocator method</span></span>

<span data-ttu-id="bb1ca-104">La `DecideAllocator` méthode sélectionne un allocateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-104">The `DecideAllocator` method selects a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb1ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb1ca-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="bb1ca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb1ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb1ca-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="bb1ca-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="bb1ca-108">Pointeur vers l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-108">Pointer to the input pin's [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="bb1ca-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="bb1ca-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="bb1ca-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb1ca-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb1ca-111">Return value</span></span>

<span data-ttu-id="bb1ca-112">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb1ca-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bb1ca-113">Remarks</span></span>

<span data-ttu-id="bb1ca-114">Cette méthode est appelée à la fin du processus de connexion du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-114">This method is called at the end of the pin connection process.</span></span> <span data-ttu-id="bb1ca-115">Il permet d'effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bb1ca-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="bb1ca-116">Appelle la méthode [**IMemInputPin :: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) pour récupérer les exigences en matière de mémoire tampon du code confidentiel d’entrée, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-116">Calls the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method to retrieve the input pin's buffer requirements, if any.</span></span>
2.  <span data-ttu-id="bb1ca-117">Appelle la méthode [**IMemInputPin :: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) pour demander un allocateur à partir de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-117">Calls the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method to request an allocator from the input pin.</span></span> <span data-ttu-id="bb1ca-118">Si la broche d’entrée ne fournit pas d’allocateur, la broche de sortie en crée une en appelant la méthode de la classe [**CBaseOutputPin :: InitAllocator**](cbaseoutputpin-initallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="bb1ca-118">If the input pin does not provide an allocator, the output pin creates one by calling the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) class method.</span></span>
3.  <span data-ttu-id="bb1ca-119">Appelle la méthode de la classe [**CBaseOutputPin ::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , qui définit les propriétés Allocator.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-119">Calls the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) class method, which sets the allocator properties.</span></span> <span data-ttu-id="bb1ca-120">Il s’agit d’une méthode virtuelle pure ; la classe dérivée doit l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-120">This is a pure virtual method; the derived class must implement it.</span></span>
4.  <span data-ttu-id="bb1ca-121">Appelle la méthode [**IMemInputPin :: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , qui avertit la broche d’entrée de l’allocateur utilisé.</span><span class="sxs-lookup"><span data-stu-id="bb1ca-121">Calls the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method, which notifies the input pin of the allocator being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb1ca-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb1ca-122">Requirements</span></span>



| <span data-ttu-id="bb1ca-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb1ca-123">Requirement</span></span> | <span data-ttu-id="bb1ca-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb1ca-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1ca-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb1ca-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bb1ca-126"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb1ca-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bb1ca-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb1ca-127">Library</span></span><br/> | <dl> <span data-ttu-id="bb1ca-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb1ca-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb1ca-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb1ca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb1ca-130">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="bb1ca-130">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




