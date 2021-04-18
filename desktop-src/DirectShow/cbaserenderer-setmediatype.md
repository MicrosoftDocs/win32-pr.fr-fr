---
description: La méthode SetMediaType est appelée lorsque le type de média du pin est défini.
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: Méthode CBaseRenderer. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ccb364545df514e098811ff6135e0c8cf72a329
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540075"
---
# <a name="cbaserenderersetmediatype-method"></a><span data-ttu-id="e9cc3-103">Méthode CBaseRenderer. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="e9cc3-103">CBaseRenderer.SetMediaType method</span></span>

<span data-ttu-id="e9cc3-104">La `SetMediaType` méthode est appelée lorsque le type de média du pin est défini.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-104">The `SetMediaType` method is called when the pin's media type is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9cc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9cc3-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="e9cc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9cc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9cc3-107">*crédit*</span><span class="sxs-lookup"><span data-stu-id="e9cc3-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e9cc3-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9cc3-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9cc3-109">Return value</span></span>

<span data-ttu-id="e9cc3-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9cc3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e9cc3-111">Remarks</span></span>

<span data-ttu-id="e9cc3-112">La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CRendererInputPin :: SetMediaType**](crendererinputpin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="e9cc3-112">The input pin calls this method from its own [**CRendererInputPin::SetMediaType**](crendererinputpin-setmediatype.md) method.</span></span> <span data-ttu-id="e9cc3-113">Cette méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="e9cc3-113">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9cc3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9cc3-114">Requirements</span></span>



| <span data-ttu-id="e9cc3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9cc3-115">Requirement</span></span> | <span data-ttu-id="e9cc3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9cc3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9cc3-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9cc3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e9cc3-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9cc3-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9cc3-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9cc3-119">Library</span></span><br/> | <dl> <span data-ttu-id="e9cc3-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e9cc3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9cc3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9cc3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9cc3-122">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="e9cc3-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




