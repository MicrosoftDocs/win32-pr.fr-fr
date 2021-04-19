---
description: La méthode OnWaitEnd est appelée lorsque le filtre est en attente d’une heure de présentation d’un exemple.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Méthode CBaseRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537691"
---
# <a name="cbaserendereronwaitend-method"></a><span data-ttu-id="80ef5-103">Méthode CBaseRenderer. OnWaitEnd</span><span class="sxs-lookup"><span data-stu-id="80ef5-103">CBaseRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="80ef5-104">La `OnWaitEnd` méthode est appelée lorsque le filtre est terminé, en attendant l’heure de la présentation d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="80ef5-104">The `OnWaitEnd` method is called when the filter is done waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="80ef5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80ef5-105">Syntax</span></span>


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="80ef5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80ef5-106">Parameters</span></span>

<span data-ttu-id="80ef5-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="80ef5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="80ef5-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80ef5-108">Return value</span></span>

<span data-ttu-id="80ef5-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="80ef5-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80ef5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="80ef5-110">Remarks</span></span>

<span data-ttu-id="80ef5-111">La méthode [**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) appelle cette méthode lorsqu’elle a fini d’attendre l’heure de la présentation d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="80ef5-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it has finished waiting for a sample's presentation time.</span></span> <span data-ttu-id="80ef5-112">Cette méthode n’effectue aucune opération dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="80ef5-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="80ef5-113">Si vous implémentez le contrôle de qualité, vous pouvez substituer cette méthode avec la méthode [**CBaseRenderer :: OnWaitStart**](cbaserenderer-onwaitstart.md) .</span><span class="sxs-lookup"><span data-stu-id="80ef5-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method.</span></span> <span data-ttu-id="80ef5-114">Vous pouvez utiliser ces méthodes pour suivre les performances du filtre.</span><span class="sxs-lookup"><span data-stu-id="80ef5-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="80ef5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80ef5-115">Requirements</span></span>



| <span data-ttu-id="80ef5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80ef5-116">Requirement</span></span> | <span data-ttu-id="80ef5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="80ef5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80ef5-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="80ef5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="80ef5-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80ef5-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="80ef5-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80ef5-120">Library</span></span><br/> | <dl> <span data-ttu-id="80ef5-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="80ef5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80ef5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80ef5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80ef5-123">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="80ef5-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




