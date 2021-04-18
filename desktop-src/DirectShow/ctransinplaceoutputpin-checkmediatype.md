---
description: La méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.
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
ms.openlocfilehash: b0a422851bc7e09075076decc39d57b85d1052ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532980"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="1eaff-103">Méthode CTransInPlaceOutputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="1eaff-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="1eaff-104">La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="1eaff-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eaff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eaff-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="1eaff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1eaff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eaff-107">*crédit*</span><span class="sxs-lookup"><span data-stu-id="1eaff-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1eaff-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="1eaff-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eaff-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1eaff-109">Return value</span></span>

<span data-ttu-id="1eaff-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1eaff-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1eaff-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1eaff-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1eaff-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1eaff-112">Return code</span></span>                                                                                                | <span data-ttu-id="1eaff-113">Description</span><span class="sxs-lookup"><span data-stu-id="1eaff-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="1eaff-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1eaff-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="1eaff-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="1eaff-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="1eaff-116"><dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt></span><span class="sxs-lookup"><span data-stu-id="1eaff-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="1eaff-117">Type de média non accepté.</span><span class="sxs-lookup"><span data-stu-id="1eaff-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1eaff-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1eaff-118">Remarks</span></span>

<span data-ttu-id="1eaff-119">Cette méthode remplace la méthode [**CTransformOutputPin :: CheckMediaType**](ctransformoutputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="1eaff-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="1eaff-120">Si le filtre est déjà en continu et utilise deux allocateurs, cette méthode rejette toutes les modifications de format.</span><span class="sxs-lookup"><span data-stu-id="1eaff-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="1eaff-121">Sinon, cette méthode appelle la méthode [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) du filtre pour vérifier le type de média.</span><span class="sxs-lookup"><span data-stu-id="1eaff-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="1eaff-122">Si la broche d’entrée est connectée, elle appelle également la méthode [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) sur la broche de sortie en amont.</span><span class="sxs-lookup"><span data-stu-id="1eaff-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eaff-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eaff-123">Requirements</span></span>



| <span data-ttu-id="1eaff-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eaff-124">Requirement</span></span> | <span data-ttu-id="1eaff-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eaff-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eaff-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1eaff-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1eaff-127"><dt>Transip. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1eaff-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1eaff-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1eaff-128">Library</span></span><br/> | <dl> <span data-ttu-id="1eaff-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1eaff-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eaff-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eaff-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eaff-131">**CTransInPlaceOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="1eaff-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




