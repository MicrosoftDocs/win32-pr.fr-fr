---
description: La méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique.
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Méthode CTransformInputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6841370795a3131cdbcc95a3bab160be2011c600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541145"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="c6b3e-103">Méthode CTransformInputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="c6b3e-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="c6b3e-104">La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="c6b3e-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6b3e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6b3e-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="c6b3e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6b3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6b3e-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="c6b3e-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b3e-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui contient le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="c6b3e-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6b3e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6b3e-109">Return value</span></span>

<span data-ttu-id="c6b3e-110">Retourne S \_ OK ou une autre valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c6b3e-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6b3e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c6b3e-111">Remarks</span></span>

<span data-ttu-id="c6b3e-112">Cette méthode implémente la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="c6b3e-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="c6b3e-113">Elle appelle la méthode [**CTransformFilter :: CheckInputType**](ctransformfilter-checkinputtype.md) du filtre, qui est également pure virtual.</span><span class="sxs-lookup"><span data-stu-id="c6b3e-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="c6b3e-114">La classe dérivée du filtre doit implémenter **CheckInputType** pour déterminer si un type d’entrée donné est acceptable.</span><span class="sxs-lookup"><span data-stu-id="c6b3e-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="c6b3e-115">Si la broche de sortie du filtre est connectée, cette méthode appelle également la méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) du filtre pour déterminer si le type d’entrée est compatible avec le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="c6b3e-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="c6b3e-116">La méthode **CheckTransform** est également virtuelle pure.</span><span class="sxs-lookup"><span data-stu-id="c6b3e-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b3e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6b3e-117">Requirements</span></span>



| <span data-ttu-id="c6b3e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6b3e-118">Requirement</span></span> | <span data-ttu-id="c6b3e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6b3e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b3e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6b3e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c6b3e-121"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6b3e-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c6b3e-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c6b3e-122">Library</span></span><br/> | <dl> <span data-ttu-id="c6b3e-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c6b3e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




