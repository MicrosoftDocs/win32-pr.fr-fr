---
description: 'La méthode Block bloque ou débloque le workflow de données à partir du code confidentiel. Cette méthode implémente la méthode IPinFlowControl :: Block.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Méthode CDynamicOutputPin. Block (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535028"
---
# <a name="cdynamicoutputpinblock-method"></a><span data-ttu-id="3eaed-104">CDynamicOutputPin. Block, méthode</span><span class="sxs-lookup"><span data-stu-id="3eaed-104">CDynamicOutputPin.Block method</span></span>

<span data-ttu-id="3eaed-105">La `Block` méthode bloque ou débloque le workflow de données à partir du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="3eaed-105">The `Block` method blocks or unblocks the flow of data from the pin.</span></span> <span data-ttu-id="3eaed-106">Cette méthode implémente la méthode [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) .</span><span class="sxs-lookup"><span data-stu-id="3eaed-106">This method implements the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eaed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3eaed-107">Syntax</span></span>


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="3eaed-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eaed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eaed-109">*dwBlockFlags*</span><span class="sxs-lookup"><span data-stu-id="3eaed-109">*dwBlockFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="3eaed-110">Indicateur qui spécifie s’il faut bloquer ou débloquer le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="3eaed-110">Flag that indicates whether to block or unblock the pin.</span></span> <span data-ttu-id="3eaed-111">Il doit s’agir de l’une des valeurs suivantes : </span><span class="sxs-lookup"><span data-stu-id="3eaed-111">Must be one of the following values:</span></span>

<span data-ttu-id="3eaed-112">Zéro : débloquer le workflow de données à partir du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="3eaed-112">Zero: Unblock data flow from the pin.</span></span>

<span data-ttu-id="3eaed-113">\_ \_ \_ Bloc de contrôle de workflow am pin \_ : bloquer le workflow de données à partir du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="3eaed-113">AM\_PIN\_FLOW\_CONTROL\_BLOCK: Block data flow from the pin.</span></span>

</dd> <dt>

<span data-ttu-id="3eaed-114">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="3eaed-114">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="3eaed-115">Handle vers un objet d’événement, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="3eaed-115">Handle to an event object, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eaed-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3eaed-116">Return value</span></span>

<span data-ttu-id="3eaed-117">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3eaed-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3eaed-118">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eaed-118">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="3eaed-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3eaed-119">Return code</span></span>                                                                                                                    | <span data-ttu-id="3eaed-120">Description</span><span class="sxs-lookup"><span data-stu-id="3eaed-120">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="3eaed-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3eaed-121"><dt>**S\_FALSE**</dt></span></span> </dl>                                        | <span data-ttu-id="3eaed-122">Le code PIN est déjà débloqué.</span><span class="sxs-lookup"><span data-stu-id="3eaed-122">Pin is already unblocked.</span></span><br/>                     |
| <dl> <span data-ttu-id="3eaed-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3eaed-123"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="3eaed-124">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="3eaed-124">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="3eaed-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3eaed-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                   | <span data-ttu-id="3eaed-126">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="3eaed-126">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="3eaed-127"><dt>**\_code PIN de VFW E \_ \_ déjà \_ bloqué**</dt></span><span class="sxs-lookup"><span data-stu-id="3eaed-127"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="3eaed-128">Le code PIN est déjà bloqué sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="3eaed-128">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="3eaed-129"><dt>**\_ \_ code PIN de VFW E \_ déjà \_ bloqué \_ sur \_ ce \_ thread**</dt></span><span class="sxs-lookup"><span data-stu-id="3eaed-129"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="3eaed-130">Le code PIN est déjà bloqué sur le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="3eaed-130">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3eaed-131">Notes</span><span class="sxs-lookup"><span data-stu-id="3eaed-131">Remarks</span></span>

<span data-ttu-id="3eaed-132">Pour plus d’informations sur cette méthode, consultez [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span><span class="sxs-lookup"><span data-stu-id="3eaed-132">For more information about this method, see [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span></span> <span data-ttu-id="3eaed-133">En interne, cette méthode appelle l’une des méthodes protégées suivantes :</span><span class="sxs-lookup"><span data-stu-id="3eaed-133">Internally, this method calls one of the following protected methods:</span></span>

-   <span data-ttu-id="3eaed-134">Block (asynchrone) : [ **CDynamicOutputPin :: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="3eaed-134">Block (asynchronous): [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="3eaed-135">Bloquer (synchrone) : [ **CDynamicOutputPin :: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="3eaed-135">Block (synchronous): [**CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="3eaed-136">Unblock : [ **CDynamicOutputPin :: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="3eaed-136">Unblock: [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span></span>

<span data-ttu-id="3eaed-137">Le déblocage est toujours effectué de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="3eaed-137">Unblocking is always performed synchronously.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eaed-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3eaed-138">Requirements</span></span>



| <span data-ttu-id="3eaed-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3eaed-139">Requirement</span></span> | <span data-ttu-id="3eaed-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eaed-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eaed-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="3eaed-141">Header</span></span><br/>  | <dl> <span data-ttu-id="3eaed-142"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3eaed-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3eaed-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3eaed-143">Library</span></span><br/> | <dl> <span data-ttu-id="3eaed-144"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3eaed-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eaed-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eaed-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eaed-146">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="3eaed-146">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




