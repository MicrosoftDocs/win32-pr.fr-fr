---
description: 'La méthode EnumMediaTypes énumère les types de média préférés du pin. Cette méthode implémente la méthode IPin :: EnumMediaTypes.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Méthode CTransInPlaceInputPin. EnumMediaTypes (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa634fa695eb0007b49fc1c36c730c7fbde361b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537418"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="1f670-104">Méthode CTransInPlaceInputPin. EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="1f670-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="1f670-105">La `EnumMediaTypes` méthode énumère les types de média préférés du pin.</span><span class="sxs-lookup"><span data-stu-id="1f670-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="1f670-106">Cette méthode implémente la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="1f670-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f670-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f670-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="1f670-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f670-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f670-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="1f670-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="1f670-110">Reçoit un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="1f670-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f670-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f670-111">Return value</span></span>

<span data-ttu-id="1f670-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f670-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1f670-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f670-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1f670-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1f670-114">Return code</span></span>                                                                                           | <span data-ttu-id="1f670-115">Description</span><span class="sxs-lookup"><span data-stu-id="1f670-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="1f670-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f670-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="1f670-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="1f670-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="1f670-118"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="1f670-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="1f670-119">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="1f670-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="1f670-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="1f670-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="1f670-121">Pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="1f670-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="1f670-122"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="1f670-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1f670-123">La broche de sortie n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="1f670-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f670-124">Notes</span><span class="sxs-lookup"><span data-stu-id="1f670-124">Remarks</span></span>

<span data-ttu-id="1f670-125">Cette méthode retourne l’interface **IEnumMediaTypes** à partir de la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="1f670-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f670-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f670-126">Requirements</span></span>



| <span data-ttu-id="1f670-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f670-127">Requirement</span></span> | <span data-ttu-id="1f670-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f670-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f670-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f670-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1f670-130"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f670-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f670-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f670-131">Library</span></span><br/> | <dl> <span data-ttu-id="1f670-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1f670-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f670-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f670-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f670-134">**CTransInPlaceInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="1f670-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




