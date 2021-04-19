---
description: La méthode Ready signale qu’une transition d’État est terminée.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Méthode CBaseRenderer. Ready (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543958"
---
# <a name="cbaserendererready-method"></a><span data-ttu-id="35241-103">CBaseRenderer. Ready, méthode</span><span class="sxs-lookup"><span data-stu-id="35241-103">CBaseRenderer.Ready method</span></span>

<span data-ttu-id="35241-104">La `Ready` méthode signale qu’une transition d’État est terminée.</span><span class="sxs-lookup"><span data-stu-id="35241-104">The `Ready` method signals that a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="35241-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35241-105">Syntax</span></span>


```C++
void Ready();
```



## <a name="parameters"></a><span data-ttu-id="35241-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35241-106">Parameters</span></span>

<span data-ttu-id="35241-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="35241-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35241-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35241-108">Return value</span></span>

<span data-ttu-id="35241-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="35241-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35241-110">Notes</span><span class="sxs-lookup"><span data-stu-id="35241-110">Remarks</span></span>

<span data-ttu-id="35241-111">Cette méthode force la méthode [**CBaseRenderer :: GetState**](cbaserenderer-getstate.md) à retourner la valeur \_ OK, ce qui indique que le filtre a terminé la transition vers son état actuel.</span><span class="sxs-lookup"><span data-stu-id="35241-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return S\_OK, which indicates that the filter has completed the transition to its current state.</span></span> <span data-ttu-id="35241-112">Le filtre appelle cette méthode chaque fois qu’une transition d’État est terminée.</span><span class="sxs-lookup"><span data-stu-id="35241-112">The filter calls this method whenever it completes a state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="35241-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35241-113">Requirements</span></span>



| <span data-ttu-id="35241-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35241-114">Requirement</span></span> | <span data-ttu-id="35241-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="35241-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35241-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="35241-116">Header</span></span><br/>  | <dl> <span data-ttu-id="35241-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35241-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="35241-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35241-118">Library</span></span><br/> | <dl> <span data-ttu-id="35241-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="35241-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35241-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35241-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35241-121">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="35241-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="35241-122">**CBaseRenderer::CheckReady**</span><span class="sxs-lookup"><span data-stu-id="35241-122">**CBaseRenderer::CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="35241-123">**CBaseRenderer :: nochapy**</span><span class="sxs-lookup"><span data-stu-id="35241-123">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> </dl>

 

 




