---
description: La méthode GetPin récupère un code confidentiel.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Méthode CBaseRenderer. GetPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b67b926e0af604e0a25ea7c09b417baf3647fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523505"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="15507-103">Méthode CBaseRenderer. GetPin</span><span class="sxs-lookup"><span data-stu-id="15507-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="15507-104">La `GetPin` méthode récupère un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="15507-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="15507-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15507-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="15507-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15507-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15507-107">*n*</span><span class="sxs-lookup"><span data-stu-id="15507-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="15507-108">Numéro du code confidentiel spécifié.</span><span class="sxs-lookup"><span data-stu-id="15507-108">Number of the specified pin.</span></span> <span data-ttu-id="15507-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="15507-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15507-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15507-110">Return value</span></span>

<span data-ttu-id="15507-111">Retourne le pointeur [**CBaseRenderer :: m \_ pInputPin**](cbaserenderer-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="15507-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="15507-112">Notes</span><span class="sxs-lookup"><span data-stu-id="15507-112">Remarks</span></span>

<span data-ttu-id="15507-113">Cette méthode implémente la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) , qui est virtuelle pure dans la classe **CBaseFilter** .</span><span class="sxs-lookup"><span data-stu-id="15507-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="15507-114">Le filtre prend en charge exactement un pin (la broche d’entrée).</span><span class="sxs-lookup"><span data-stu-id="15507-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="15507-115">La première fois que cette méthode est appelée, elle crée le code confidentiel en tant que nouvel objet [**CRendererInputPin**](crendererinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="15507-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="15507-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15507-116">Requirements</span></span>



| <span data-ttu-id="15507-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15507-117">Requirement</span></span> | <span data-ttu-id="15507-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="15507-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15507-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="15507-119">Header</span></span><br/>  | <dl> <span data-ttu-id="15507-120"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15507-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15507-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="15507-121">Library</span></span><br/> | <dl> <span data-ttu-id="15507-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="15507-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15507-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15507-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15507-124">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="15507-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




