---
description: La méthode Connect termine une connexion à la broche de sortie.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: CPullPin. Connect, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544037"
---
# <a name="cpullpinconnect-method"></a><span data-ttu-id="69ec5-103">CPullPin. Connect, méthode</span><span class="sxs-lookup"><span data-stu-id="69ec5-103">CPullPin.Connect method</span></span>

<span data-ttu-id="69ec5-104">La `Connect` méthode termine une connexion à la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="69ec5-104">The `Connect` method completes a connection to the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="69ec5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69ec5-105">Syntax</span></span>


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a><span data-ttu-id="69ec5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69ec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69ec5-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="69ec5-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="69ec5-108">Pointeur vers l’interface **IUnknown** de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="69ec5-108">Pointer to the **IUnknown** interface of the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="69ec5-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="69ec5-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="69ec5-110">Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur préféré du code confidentiel d’entrée, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="69ec5-110">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="69ec5-111">*bSync*</span><span class="sxs-lookup"><span data-stu-id="69ec5-111">*bSync*</span></span> 
</dt> <dd>

<span data-ttu-id="69ec5-112">Valeur booléenne qui spécifie s’il faut utiliser des lectures synchrones.</span><span class="sxs-lookup"><span data-stu-id="69ec5-112">Boolean value that specifies whether to use synchronous reads.</span></span> <span data-ttu-id="69ec5-113">Si la **valeur est true**, le code PIN effectue des opérations de lecture synchrones sur la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="69ec5-113">If **TRUE**, the pin performs synchronous read operations on the output pin.</span></span> <span data-ttu-id="69ec5-114">Si la **valeur est false**, le code PIN effectue des requêtes de lecture asynchrones.</span><span class="sxs-lookup"><span data-stu-id="69ec5-114">If **FALSE**, the pin makes asynchronous read requests.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69ec5-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69ec5-115">Return value</span></span>

<span data-ttu-id="69ec5-116">Retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="69ec5-116">Returns an **HRESULT**.</span></span> <span data-ttu-id="69ec5-117">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="69ec5-117">Possible values include the following.</span></span>



| <span data-ttu-id="69ec5-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="69ec5-118">Return code</span></span>                                                                                               | <span data-ttu-id="69ec5-119">Description</span><span class="sxs-lookup"><span data-stu-id="69ec5-119">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69ec5-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69ec5-120"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="69ec5-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="69ec5-121">Success.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="69ec5-122"><dt>**VFW \_ E \_ déjà \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="69ec5-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="69ec5-123">La broche d’entrée est déjà connectée.</span><span class="sxs-lookup"><span data-stu-id="69ec5-123">The input pin is already connected.</span></span><br/>                                  |
| <dl> <span data-ttu-id="69ec5-124"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="69ec5-124"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="69ec5-125">La broche de sortie n’expose pas [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span><span class="sxs-lookup"><span data-stu-id="69ec5-125">The output pin does not expose [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69ec5-126">Notes</span><span class="sxs-lookup"><span data-stu-id="69ec5-126">Remarks</span></span>

<span data-ttu-id="69ec5-127">Appelez cette méthode pendant le processus de connexion du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="69ec5-127">Call this method during the input pin's connection process.</span></span> <span data-ttu-id="69ec5-128">Si la méthode échoue, le code PIN doit faire échouer la connexion.</span><span class="sxs-lookup"><span data-stu-id="69ec5-128">If the method fails, the pin should fail the connection.</span></span>

<span data-ttu-id="69ec5-129">Cette méthode interroge la broche de sortie pour l’interface **IAsyncReader** .</span><span class="sxs-lookup"><span data-stu-id="69ec5-129">This method queries the output pin for the **IAsyncReader** interface.</span></span> <span data-ttu-id="69ec5-130">En cas de réussite, elle appelle [**CPullPin ::D ecideallocator**](cpullpin-decideallocator.md) pour négocier l’allocateur pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="69ec5-130">If successful, it calls [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) to negotiate the allocator for the connection.</span></span> <span data-ttu-id="69ec5-131">Si votre code pin d’entrée a un allocateur préféré, spécifiez-le dans le paramètre *pAlloc* ; la méthode **DecideAllocator** transmet ce pointeur à la méthode [**IAsyncReader :: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="69ec5-131">If your input pin has a preferred allocator, specify it in the *pAlloc* parameter; the **DecideAllocator** method passes this pointer to the output pin's [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method.</span></span> <span data-ttu-id="69ec5-132">Sinon, affectez à *pAlloc* la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="69ec5-132">Otherwise, set *pAlloc* to **NULL**.</span></span>

<span data-ttu-id="69ec5-133">Si la valeur de *bSync* est **true**, l’objet **CPullPin** effectue des requêtes de lecture synchrones, en appelant le [**IAsyncReader :: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="69ec5-133">If the value of *bSync* is **TRUE**, the **CPullPin** object makes synchronous read requests, by calling the output pin's [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span> <span data-ttu-id="69ec5-134">Sinon, elle appelle la méthode [**IAsyncReader :: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) pour effectuer le chevauchement des demandes de lecture.</span><span class="sxs-lookup"><span data-stu-id="69ec5-134">Otherwise, it calls the [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) method to make overlapping read requests.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ec5-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69ec5-135">Requirements</span></span>



| <span data-ttu-id="69ec5-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69ec5-136">Requirement</span></span> | <span data-ttu-id="69ec5-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="69ec5-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ec5-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="69ec5-138">Header</span></span><br/>  | <dl> <span data-ttu-id="69ec5-139"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="69ec5-139"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="69ec5-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69ec5-140">Library</span></span><br/> | <dl> <span data-ttu-id="69ec5-141"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="69ec5-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ec5-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69ec5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ec5-143">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="69ec5-143">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




