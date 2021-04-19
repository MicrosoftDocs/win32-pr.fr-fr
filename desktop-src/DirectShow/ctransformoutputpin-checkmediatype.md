---
description: La méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Méthode CTransformOutputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c2bc617a5ff56a8b82184700af85e2634960ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530031"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="cdc1d-103">Méthode CTransformOutputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="cdc1d-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="cdc1d-104">La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="cdc1d-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdc1d-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="cdc1d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdc1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdc1d-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="cdc1d-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc1d-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="cdc1d-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdc1d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdc1d-109">Return value</span></span>

<span data-ttu-id="cdc1d-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cdc1d-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cdc1d-111">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="cdc1d-111">Possible values include the following.</span></span>



| <span data-ttu-id="cdc1d-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cdc1d-112">Return code</span></span>                                                                                  | <span data-ttu-id="cdc1d-113">Description</span><span class="sxs-lookup"><span data-stu-id="cdc1d-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="cdc1d-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cdc1d-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cdc1d-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cdc1d-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cdc1d-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cdc1d-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="cdc1d-117">La broche d’entrée du filtre n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="cdc1d-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cdc1d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="cdc1d-118">Remarks</span></span>

<span data-ttu-id="cdc1d-119">Cette méthode implémente la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="cdc1d-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="cdc1d-120">La méthode échoue si la broche d’entrée du filtre n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="cdc1d-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="cdc1d-121">Sinon, elle appelle la méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) du filtre, qui est également pure virtual.</span><span class="sxs-lookup"><span data-stu-id="cdc1d-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="cdc1d-122">La classe dérivée du filtre doit implémenter **CheckTransform**, qui détermine si le type de média de sortie proposé est compatible avec le type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cdc1d-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc1d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdc1d-123">Requirements</span></span>



| <span data-ttu-id="cdc1d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdc1d-124">Requirement</span></span> | <span data-ttu-id="cdc1d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc1d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc1d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdc1d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cdc1d-127"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc1d-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cdc1d-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cdc1d-128">Library</span></span><br/> | <dl> <span data-ttu-id="cdc1d-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc1d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




