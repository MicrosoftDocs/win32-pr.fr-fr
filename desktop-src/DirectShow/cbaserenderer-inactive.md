---
description: La méthode inactive est appelée lorsque l’état passe à arrêté.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: CBaseRenderer. inactive, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530454"
---
# <a name="cbaserendererinactive-method"></a><span data-ttu-id="0e15c-103">CBaseRenderer. inactive, méthode</span><span class="sxs-lookup"><span data-stu-id="0e15c-103">CBaseRenderer.Inactive method</span></span>

<span data-ttu-id="0e15c-104">La `Inactive` méthode est appelée lorsque l’état passe à arrêté.</span><span class="sxs-lookup"><span data-stu-id="0e15c-104">The `Inactive` method is called when the state is switched to stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e15c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e15c-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="0e15c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e15c-106">Parameters</span></span>

<span data-ttu-id="0e15c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0e15c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e15c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e15c-108">Return value</span></span>

<span data-ttu-id="0e15c-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e15c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e15c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0e15c-110">Remarks</span></span>

<span data-ttu-id="0e15c-111">La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CRendererInputPin :: inactive**](crendererinputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="0e15c-111">The input pin calls this method from its own [**CRendererInputPin::Inactive**](crendererinputpin-inactive.md) method.</span></span> <span data-ttu-id="0e15c-112">Le filtre appelle la méthode [**CBaseRenderer :: ClearPendingSample**](cbaserenderer-clearpendingsample.md) pour libérer l’exemple le plus récent.</span><span class="sxs-lookup"><span data-stu-id="0e15c-112">The filter calls the [**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md) method to release the most recent sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e15c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e15c-113">Requirements</span></span>



| <span data-ttu-id="0e15c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e15c-114">Requirement</span></span> | <span data-ttu-id="0e15c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e15c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e15c-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e15c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0e15c-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e15c-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0e15c-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0e15c-118">Library</span></span><br/> | <dl> <span data-ttu-id="0e15c-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0e15c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e15c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e15c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e15c-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="0e15c-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




