---
description: 'Méthode CBaseRenderer. GetPin : la méthode GetPin récupère un code confidentiel.'
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
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119887"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="e9fde-103">Méthode CBaseRenderer. GetPin</span><span class="sxs-lookup"><span data-stu-id="e9fde-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="e9fde-104">La `GetPin` méthode récupère un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="e9fde-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9fde-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9fde-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="e9fde-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9fde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9fde-107">*n*</span><span class="sxs-lookup"><span data-stu-id="e9fde-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="e9fde-108">Numéro du code confidentiel spécifié.</span><span class="sxs-lookup"><span data-stu-id="e9fde-108">Number of the specified pin.</span></span> <span data-ttu-id="e9fde-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e9fde-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9fde-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e9fde-110">Return value</span></span>

<span data-ttu-id="e9fde-111">Retourne le pointeur [**CBaseRenderer :: m \_ pInputPin**](cbaserenderer-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="e9fde-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9fde-112">Notes </span><span class="sxs-lookup"><span data-stu-id="e9fde-112">Remarks</span></span>

<span data-ttu-id="e9fde-113">Cette méthode implémente la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) , qui est virtuelle pure dans la classe **CBaseFilter** .</span><span class="sxs-lookup"><span data-stu-id="e9fde-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="e9fde-114">Le filtre prend en charge exactement un pin (la broche d’entrée).</span><span class="sxs-lookup"><span data-stu-id="e9fde-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="e9fde-115">La première fois que cette méthode est appelée, elle crée le code confidentiel en tant que nouvel objet [**CRendererInputPin**](crendererinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="e9fde-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9fde-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9fde-116">Requirements</span></span>



| <span data-ttu-id="e9fde-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9fde-117">Requirement</span></span> | <span data-ttu-id="e9fde-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9fde-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9fde-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9fde-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e9fde-120"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9fde-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9fde-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9fde-121">Library</span></span><br/> | <dl> <span data-ttu-id="e9fde-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e9fde-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9fde-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9fde-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9fde-124">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="e9fde-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




