---
description: 'Méthode CBaseOutputPin. CheckConnect : la méthode CheckConnect détermine si une connexion de code confidentiel est appropriée.'
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Méthode CBaseOutputPin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ea5ad32de18046f3d23145d82e971391c3e304c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096187"
---
# <a name="cbaseoutputpincheckconnect-method"></a><span data-ttu-id="12282-103">Méthode CBaseOutputPin. CheckConnect</span><span class="sxs-lookup"><span data-stu-id="12282-103">CBaseOutputPin.CheckConnect method</span></span>

<span data-ttu-id="12282-104">La `CheckConnect` méthode détermine si une connexion de code confidentiel est appropriée.</span><span class="sxs-lookup"><span data-stu-id="12282-104">The `CheckConnect` method determines whether a pin connection is suitable.</span></span>

## <a name="syntax"></a><span data-ttu-id="12282-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12282-105">Syntax</span></span>


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="12282-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12282-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12282-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="12282-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="12282-108">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel d’entrée.</span><span class="sxs-lookup"><span data-stu-id="12282-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12282-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="12282-109">Return value</span></span>

<span data-ttu-id="12282-110">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="12282-110">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="12282-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="12282-111">Return code</span></span>                                                                                               | <span data-ttu-id="12282-112">Description</span><span class="sxs-lookup"><span data-stu-id="12282-112">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="12282-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="12282-113"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="12282-114">Réussite.</span><span class="sxs-lookup"><span data-stu-id="12282-114">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="12282-115"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="12282-115"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="12282-116">La broche d’entrée ne prend pas en charge [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span><span class="sxs-lookup"><span data-stu-id="12282-116">Input pin does not support [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).</span></span><br/> |
| <dl> <span data-ttu-id="12282-117"><dt>**VFW \_ E \_ sens non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12282-117"><dt>**VFW\_E\_INVALID\_DIRECTION**</dt></span></span> </dl> | <span data-ttu-id="12282-118">Les directions de code confidentiel ne sont pas compatibles.</span><span class="sxs-lookup"><span data-stu-id="12282-118">Pin directions are not compatible.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="12282-119">Notes </span><span class="sxs-lookup"><span data-stu-id="12282-119">Remarks</span></span>

<span data-ttu-id="12282-120">Cette méthode appelle la méthode de classe de base [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) , puis interroge la broche d’entrée pour son interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="12282-120">This method calls the base-class [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method, and then queries the input pin for its [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="12282-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12282-121">Requirements</span></span>



| <span data-ttu-id="12282-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12282-122">Requirement</span></span> | <span data-ttu-id="12282-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="12282-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12282-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="12282-124">Header</span></span><br/>  | <dl> <span data-ttu-id="12282-125"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12282-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="12282-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12282-126">Library</span></span><br/> | <dl> <span data-ttu-id="12282-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="12282-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12282-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12282-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12282-129">**CBaseOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="12282-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




