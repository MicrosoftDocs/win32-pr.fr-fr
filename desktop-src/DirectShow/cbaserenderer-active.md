---
description: La méthode active est appelée lorsque l’état passe à suspendu ou en cours d’exécution.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: CBaseRenderer. active, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11593ffb25a953f4269d84ee2b9c9d884a23e5fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543177"
---
# <a name="cbaserendereractive-method"></a><span data-ttu-id="dcadb-103">CBaseRenderer. active, méthode</span><span class="sxs-lookup"><span data-stu-id="dcadb-103">CBaseRenderer.Active method</span></span>

<span data-ttu-id="dcadb-104">La `Active` méthode est appelée lorsque l’état passe à suspendu ou en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="dcadb-104">The `Active` method is called when the state is switched to paused or running.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcadb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcadb-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="dcadb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcadb-106">Parameters</span></span>

<span data-ttu-id="dcadb-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dcadb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcadb-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcadb-108">Return value</span></span>

<span data-ttu-id="dcadb-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dcadb-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcadb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dcadb-110">Remarks</span></span>

<span data-ttu-id="dcadb-111">La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CRendererInputPin :: active**](crendererinputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="dcadb-111">The input pin calls this method from its own [**CRendererInputPin::Active**](crendererinputpin-active.md) method.</span></span> <span data-ttu-id="dcadb-112">Cette méthode n’a aucun effet dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="dcadb-112">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcadb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcadb-113">Requirements</span></span>



| <span data-ttu-id="dcadb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcadb-114">Requirement</span></span> | <span data-ttu-id="dcadb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcadb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcadb-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcadb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dcadb-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcadb-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dcadb-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dcadb-118">Library</span></span><br/> | <dl> <span data-ttu-id="dcadb-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dcadb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcadb-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcadb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcadb-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="dcadb-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




