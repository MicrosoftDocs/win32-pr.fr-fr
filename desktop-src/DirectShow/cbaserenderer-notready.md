---
description: La méthode nochapy signale qu’une transition d’État n’est pas encore terminée.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Méthode CBaseRenderer. nochapy (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533246"
---
# <a name="cbaserenderernotready-method"></a><span data-ttu-id="9d80e-103">Méthode CBaseRenderer. nochapy</span><span class="sxs-lookup"><span data-stu-id="9d80e-103">CBaseRenderer.NotReady method</span></span>

<span data-ttu-id="9d80e-104">La `NotReady` méthode signale qu’une transition d’État n’est pas encore terminée.</span><span class="sxs-lookup"><span data-stu-id="9d80e-104">The `NotReady` method signals that a state transition is not yet complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d80e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d80e-105">Syntax</span></span>


```C++
void NotReady();
```



## <a name="parameters"></a><span data-ttu-id="9d80e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d80e-106">Parameters</span></span>

<span data-ttu-id="9d80e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9d80e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d80e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d80e-108">Return value</span></span>

<span data-ttu-id="9d80e-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9d80e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d80e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9d80e-110">Remarks</span></span>

<span data-ttu-id="9d80e-111">Cette méthode force la méthode [**CBaseRenderer :: GetState**](cbaserenderer-getstate.md) à retourner le niveau intermédiaire de l' \_ État VFW S, ce \_ \_ qui indique que le filtre passe toujours à son état actuel.</span><span class="sxs-lookup"><span data-stu-id="9d80e-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return VFW\_S\_STATE\_INTERMEDIATE, which indicates that the filter is still transitioning to its current state.</span></span> <span data-ttu-id="9d80e-112">Le filtre appelle cette méthode chaque fois qu’une transition d’État est en attente.</span><span class="sxs-lookup"><span data-stu-id="9d80e-112">The filter calls this method whenever a state transition is pending.</span></span> <span data-ttu-id="9d80e-113">(Cela se produit lorsque le filtre est suspendu, jusqu’à ce qu’il reçoive un exemple.)</span><span class="sxs-lookup"><span data-stu-id="9d80e-113">(This occurs when the filter pauses, until it receives a sample.)</span></span>

## <a name="requirements"></a><span data-ttu-id="9d80e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d80e-114">Requirements</span></span>



| <span data-ttu-id="9d80e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d80e-115">Requirement</span></span> | <span data-ttu-id="9d80e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d80e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d80e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d80e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9d80e-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d80e-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9d80e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d80e-119">Library</span></span><br/> | <dl> <span data-ttu-id="9d80e-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9d80e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d80e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d80e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d80e-122">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="9d80e-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="9d80e-123">**CheckReady**</span><span class="sxs-lookup"><span data-stu-id="9d80e-123">**CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="9d80e-124">**Ready**</span><span class="sxs-lookup"><span data-stu-id="9d80e-124">**Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




