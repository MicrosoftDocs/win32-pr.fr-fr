---
description: 'Méthode CTransInPlaceOutputPin. CheckMediaType : la méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.'
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Méthode CTransInPlaceOutputPin. CheckMediaType (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66cd29758e0b2d63db88db8b998cc79ec12efdd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094717"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="1f2a5-103">Méthode CTransInPlaceOutputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="1f2a5-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="1f2a5-104">La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f2a5-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="1f2a5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f2a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f2a5-107">*crédit*</span><span class="sxs-lookup"><span data-stu-id="1f2a5-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1f2a5-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f2a5-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f2a5-109">Return value</span></span>

<span data-ttu-id="1f2a5-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f2a5-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1f2a5-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f2a5-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1f2a5-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1f2a5-112">Return code</span></span>                                                                                                | <span data-ttu-id="1f2a5-113">Description</span><span class="sxs-lookup"><span data-stu-id="1f2a5-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="1f2a5-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f2a5-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="1f2a5-115">Réussite.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="1f2a5-116"><dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt></span><span class="sxs-lookup"><span data-stu-id="1f2a5-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="1f2a5-117">Type de média non accepté.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f2a5-118">Notes </span><span class="sxs-lookup"><span data-stu-id="1f2a5-118">Remarks</span></span>

<span data-ttu-id="1f2a5-119">Cette méthode remplace la méthode [**CTransformOutputPin :: CheckMediaType**](ctransformoutputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="1f2a5-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="1f2a5-120">Si le filtre est déjà en continu et utilise deux allocateurs, cette méthode rejette toutes les modifications de format.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="1f2a5-121">Sinon, cette méthode appelle la méthode [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) du filtre pour vérifier le type de média.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="1f2a5-122">Si la broche d’entrée est connectée, elle appelle également la méthode [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche de sortie en amont.</span><span class="sxs-lookup"><span data-stu-id="1f2a5-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2a5-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f2a5-123">Requirements</span></span>



| <span data-ttu-id="1f2a5-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f2a5-124">Requirement</span></span> | <span data-ttu-id="1f2a5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f2a5-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2a5-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f2a5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1f2a5-127"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2a5-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f2a5-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f2a5-128">Library</span></span><br/> | <dl> <span data-ttu-id="1f2a5-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2a5-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f2a5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f2a5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f2a5-131">**CTransInPlaceOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="1f2a5-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




