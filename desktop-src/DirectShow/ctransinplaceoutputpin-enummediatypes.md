---
description: 'Méthode CTransInPlaceOutputPin. EnumMediaTypes : la méthode EnumMediaTypes énumère les types de média préférés du pin. Cette méthode implémente la méthode IPin :: EnumMediaTypes.'
ms.assetid: 942c6594-3053-484a-a0f7-286dcd3f7550
title: Méthode CTransInPlaceOutputPin. EnumMediaTypes (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26dd58f23dc18a086c6c59f6f8a6a098e3449fea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084633"
---
# <a name="ctransinplaceoutputpinenummediatypes-method"></a><span data-ttu-id="bf36a-104">Méthode CTransInPlaceOutputPin. EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="bf36a-104">CTransInPlaceOutputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="bf36a-105">La `EnumMediaTypes` méthode énumère les types de média préférés du pin.</span><span class="sxs-lookup"><span data-stu-id="bf36a-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="bf36a-106">Cette méthode implémente la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="bf36a-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf36a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf36a-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="bf36a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf36a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf36a-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="bf36a-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="bf36a-110">Reçoit un pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="bf36a-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf36a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bf36a-111">Return value</span></span>

<span data-ttu-id="bf36a-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf36a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bf36a-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf36a-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="bf36a-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bf36a-114">Return code</span></span>                                                                                           | <span data-ttu-id="bf36a-115">Description</span><span class="sxs-lookup"><span data-stu-id="bf36a-115">Description</span></span>                                         |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="bf36a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bf36a-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="bf36a-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="bf36a-117">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="bf36a-118"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="bf36a-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="bf36a-119">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="bf36a-119">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="bf36a-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="bf36a-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="bf36a-121">Pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="bf36a-121">**NULL** pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="bf36a-122"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="bf36a-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bf36a-123">La broche d’entrée du filtre n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="bf36a-123">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf36a-124">Notes </span><span class="sxs-lookup"><span data-stu-id="bf36a-124">Remarks</span></span>

<span data-ttu-id="bf36a-125">Cette méthode retourne l’interface **IEnumMediaTypes** à partir de la broche de sortie en amont.</span><span class="sxs-lookup"><span data-stu-id="bf36a-125">This method returns the **IEnumMediaTypes** interface from the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf36a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf36a-126">Requirements</span></span>



| <span data-ttu-id="bf36a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf36a-127">Requirement</span></span> | <span data-ttu-id="bf36a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf36a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf36a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf36a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bf36a-130"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf36a-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf36a-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bf36a-131">Library</span></span><br/> | <dl> <span data-ttu-id="bf36a-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf36a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf36a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf36a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf36a-134">**CTransInPlaceOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="bf36a-134">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




