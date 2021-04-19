---
description: 'La méthode SetMediaType définit le type de média pour la connexion. Cette méthode remplace la méthode CBasePin :: SetMediaType.'
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Méthode CRendererInputPin. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca70878f8f6358a3297c22cbb9ac8e49ba0ce310
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543949"
---
# <a name="crendererinputpinsetmediatype-method"></a><span data-ttu-id="be203-104">Méthode CRendererInputPin. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="be203-104">CRendererInputPin.SetMediaType method</span></span>

<span data-ttu-id="be203-105">La `SetMediaType` méthode définit le type de média pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="be203-105">The `SetMediaType` method sets the media type for the connection.</span></span> <span data-ttu-id="be203-106">Cette méthode remplace la méthode [**CBasePin :: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="be203-106">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be203-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be203-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="be203-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be203-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be203-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="be203-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="be203-110">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="be203-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be203-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be203-111">Return value</span></span>

<span data-ttu-id="be203-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be203-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be203-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be203-113">Requirements</span></span>



| <span data-ttu-id="be203-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be203-114">Requirement</span></span> | <span data-ttu-id="be203-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="be203-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be203-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="be203-116">Header</span></span><br/>  | <dl> <span data-ttu-id="be203-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be203-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be203-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be203-118">Library</span></span><br/> | <dl> <span data-ttu-id="be203-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="be203-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be203-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be203-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be203-121">**CRendererInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="be203-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




