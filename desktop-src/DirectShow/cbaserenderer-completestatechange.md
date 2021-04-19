---
description: La méthode CompleteStateChange détermine si une transition vers l’état suspendu est terminée.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Méthode CBaseRenderer. CompleteStateChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538780"
---
# <a name="cbaserenderercompletestatechange-method"></a><span data-ttu-id="8990a-103">Méthode CBaseRenderer. CompleteStateChange</span><span class="sxs-lookup"><span data-stu-id="8990a-103">CBaseRenderer.CompleteStateChange method</span></span>

<span data-ttu-id="8990a-104">La `CompleteStateChange` méthode détermine si une transition vers l’état suspendu est terminée.</span><span class="sxs-lookup"><span data-stu-id="8990a-104">The `CompleteStateChange` method determines whether a transition to the paused state is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="8990a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8990a-105">Syntax</span></span>


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a><span data-ttu-id="8990a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8990a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8990a-107">*OldState*</span><span class="sxs-lookup"><span data-stu-id="8990a-107">*OldState*</span></span> 
</dt> <dd>

<span data-ttu-id="8990a-108">État avant la transition.</span><span class="sxs-lookup"><span data-stu-id="8990a-108">State prior to the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8990a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8990a-109">Return value</span></span>

<span data-ttu-id="8990a-110">Retourne S \_ OK si la transition est terminée.</span><span class="sxs-lookup"><span data-stu-id="8990a-110">Returns S\_OK if the transition is complete.</span></span> <span data-ttu-id="8990a-111">Sinon, retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="8990a-111">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="8990a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8990a-112">Remarks</span></span>

<span data-ttu-id="8990a-113">La méthode [**CBaseRenderer ::P ause**](cbaserenderer-pause.md) appelle cette méthode pour mettre à jour l’état de la transition d’État.</span><span class="sxs-lookup"><span data-stu-id="8990a-113">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md) method calls this method to update the state-transition status.</span></span> <span data-ttu-id="8990a-114">En général, la transition vers suspendue ne se termine pas tant que le filtre n’a pas reçu d’exemple.</span><span class="sxs-lookup"><span data-stu-id="8990a-114">In general, the transition to paused does not finish until the filter receives a sample.</span></span> <span data-ttu-id="8990a-115">Toutefois, dans certaines situations, la transition se termine immédiatement : par exemple, si le filtre n’est pas connecté ou si la fin du flux a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="8990a-115">However, in some situations the transition completes immediately: for example, if the filter is unconnected, or if the end of the stream was reached.</span></span> <span data-ttu-id="8990a-116">Cette méthode vérifie les différents critères, puis appelle la méthode [**CBaseRenderer :: Ready**](cbaserenderer-ready.md) ou la méthode [**CBaseRenderer :: nochapy**](cbaserenderer-notready.md) pour mettre à jour l’état de transition.</span><span class="sxs-lookup"><span data-stu-id="8990a-116">This method checks the various criteria and then calls the [**CBaseRenderer::Ready**](cbaserenderer-ready.md) method or the [**CBaseRenderer::NotReady**](cbaserenderer-notready.md) method to update the transition status.</span></span>

## <a name="requirements"></a><span data-ttu-id="8990a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8990a-117">Requirements</span></span>



| <span data-ttu-id="8990a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8990a-118">Requirement</span></span> | <span data-ttu-id="8990a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8990a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8990a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8990a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8990a-121"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8990a-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8990a-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8990a-122">Library</span></span><br/> | <dl> <span data-ttu-id="8990a-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8990a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8990a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8990a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8990a-125">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="8990a-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




