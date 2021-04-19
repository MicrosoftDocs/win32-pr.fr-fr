---
description: 'La méthode CheckMediaType détermine si le code PIN accepte un type de média spécifique. Cette méthode remplace la méthode CBasePin :: CheckMediaType.'
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Méthode CRendererInputPin. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525270"
---
# <a name="crendererinputpincheckmediatype-method"></a><span data-ttu-id="4664d-104">Méthode CRendererInputPin. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="4664d-104">CRendererInputPin.CheckMediaType method</span></span>

<span data-ttu-id="4664d-105">La `CheckMediaType` méthode détermine si le code PIN accepte un type de média spécifique.</span><span class="sxs-lookup"><span data-stu-id="4664d-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="4664d-106">Cette méthode remplace la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="4664d-106">This method overrides the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4664d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4664d-107">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="4664d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4664d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4664d-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="4664d-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="4664d-110">Pointeur vers un objet de type de média qui contient le type de média proposé.</span><span class="sxs-lookup"><span data-stu-id="4664d-110">Pointer to a media type object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4664d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4664d-111">Return value</span></span>

<span data-ttu-id="4664d-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4664d-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4664d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4664d-113">Requirements</span></span>



| <span data-ttu-id="4664d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4664d-114">Requirement</span></span> | <span data-ttu-id="4664d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4664d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4664d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4664d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4664d-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4664d-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4664d-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4664d-118">Library</span></span><br/> | <dl> <span data-ttu-id="4664d-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4664d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4664d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4664d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4664d-121">**CRendererInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="4664d-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




