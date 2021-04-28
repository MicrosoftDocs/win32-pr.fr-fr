---
description: 'Méthode CTransInPlaceInputPin. EnumMediaTypes : la méthode EnumMediaTypes énumère les types de média préférés du pin. Cette méthode implémente la méthode IPin :: EnumMediaTypes.'
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
ms.openlocfilehash: 9f9e05d0e9db50cabc700da7b3803c1606efab78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094757"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="86535-104">Méthode CTransInPlaceInputPin. EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="86535-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="86535-105">La `EnumMediaTypes` méthode énumère les types de média préférés du pin.</span><span class="sxs-lookup"><span data-stu-id="86535-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="86535-106">Cette méthode implémente la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="86535-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86535-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86535-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="86535-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86535-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86535-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="86535-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="86535-110">Reçoit un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="86535-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86535-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="86535-111">Return value</span></span>

<span data-ttu-id="86535-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86535-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="86535-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="86535-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="86535-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="86535-114">Return code</span></span>                                                                                           | <span data-ttu-id="86535-115">Description</span><span class="sxs-lookup"><span data-stu-id="86535-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="86535-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86535-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="86535-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="86535-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="86535-118"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="86535-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="86535-119">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="86535-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="86535-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="86535-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="86535-121">Pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="86535-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="86535-122"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="86535-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="86535-123">La broche de sortie n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="86535-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86535-124">Notes </span><span class="sxs-lookup"><span data-stu-id="86535-124">Remarks</span></span>

<span data-ttu-id="86535-125">Cette méthode retourne l’interface **IEnumMediaTypes** à partir de la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="86535-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="86535-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86535-126">Requirements</span></span>



| <span data-ttu-id="86535-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86535-127">Requirement</span></span> | <span data-ttu-id="86535-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="86535-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86535-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="86535-129">Header</span></span><br/>  | <dl> <span data-ttu-id="86535-130"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86535-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="86535-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86535-131">Library</span></span><br/> | <dl> <span data-ttu-id="86535-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="86535-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86535-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86535-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86535-134">**CTransInPlaceInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="86535-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




