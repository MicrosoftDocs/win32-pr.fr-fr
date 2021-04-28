---
description: 'Méthode CTransInPlaceInputPin. CheckMediaType : la méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.'
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Méthode CTransInPlaceInputPin. CheckMediaType (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5de3cec87d740db42824b0d7abf1ee4bfc6aeecb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094797"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="2da8d-103">Méthode CTransInPlaceInputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="2da8d-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="2da8d-104">La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="2da8d-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da8d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2da8d-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2da8d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2da8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da8d-107">*crédit*</span><span class="sxs-lookup"><span data-stu-id="2da8d-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2da8d-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="2da8d-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da8d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2da8d-109">Return value</span></span>

<span data-ttu-id="2da8d-110">Retourne S \_ OK si le type de média proposé est acceptable.</span><span class="sxs-lookup"><span data-stu-id="2da8d-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="2da8d-111">Sinon, retourne S \_ false ou un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2da8d-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da8d-112">Notes </span><span class="sxs-lookup"><span data-stu-id="2da8d-112">Remarks</span></span>

<span data-ttu-id="2da8d-113">Cette méthode remplace la méthode [**CTransformInputPin :: CheckMediaType**](ctransforminputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="2da8d-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="2da8d-114">Elle appelle la méthode [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) du filtre pour vérifier le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2da8d-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="2da8d-115">Si la broche de sortie est connectée, cette méthode appelle également la méthode [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="2da8d-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da8d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2da8d-116">Requirements</span></span>



| <span data-ttu-id="2da8d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2da8d-117">Requirement</span></span> | <span data-ttu-id="2da8d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2da8d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da8d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="2da8d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2da8d-120"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2da8d-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2da8d-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2da8d-121">Library</span></span><br/> | <dl> <span data-ttu-id="2da8d-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2da8d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da8d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2da8d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da8d-124">**CTransInPlaceInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="2da8d-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




