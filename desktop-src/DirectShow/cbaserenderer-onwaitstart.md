---
description: La méthode OnWaitStart est appelée quand le filtre commence à attendre l’heure de la présentation d’un exemple.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Méthode CBaseRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526476"
---
# <a name="cbaserendereronwaitstart-method"></a><span data-ttu-id="6c747-103">Méthode CBaseRenderer. OnWaitStart</span><span class="sxs-lookup"><span data-stu-id="6c747-103">CBaseRenderer.OnWaitStart method</span></span>

<span data-ttu-id="6c747-104">La `OnWaitStart` méthode est appelée lorsque le filtre commence à attendre l’heure de la présentation d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="6c747-104">The `OnWaitStart` method is called when the filter starts waiting for a sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c747-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c747-105">Syntax</span></span>


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="6c747-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c747-106">Parameters</span></span>

<span data-ttu-id="6c747-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6c747-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c747-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c747-108">Return value</span></span>

<span data-ttu-id="6c747-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6c747-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c747-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6c747-110">Remarks</span></span>

<span data-ttu-id="6c747-111">La méthode [**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) appelle cette méthode lorsqu’elle commence à attendre l’heure de la présentation d’un exemple.</span><span class="sxs-lookup"><span data-stu-id="6c747-111">The [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method calls this method when it begins waiting for a sample's presentation time.</span></span> <span data-ttu-id="6c747-112">Cette méthode n’effectue aucune opération dans la classe de base, mais la classe dérivée peut la substituer.</span><span class="sxs-lookup"><span data-stu-id="6c747-112">This method does not do anything in the base class, but the derived class can override it.</span></span>

<span data-ttu-id="6c747-113">Si vous implémentez le contrôle de qualité, vous pouvez substituer cette méthode avec la méthode [**CBaseRenderer :: OnWaitEnd**](cbaserenderer-onwaitend.md) .</span><span class="sxs-lookup"><span data-stu-id="6c747-113">If you are implementing quality control, you might override this method along with the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method.</span></span> <span data-ttu-id="6c747-114">Vous pouvez utiliser ces méthodes pour suivre les performances du filtre.</span><span class="sxs-lookup"><span data-stu-id="6c747-114">You can use these methods to track the filter's performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c747-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c747-115">Requirements</span></span>



| <span data-ttu-id="6c747-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c747-116">Requirement</span></span> | <span data-ttu-id="6c747-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c747-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c747-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c747-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6c747-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c747-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c747-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6c747-120">Library</span></span><br/> | <dl> <span data-ttu-id="6c747-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6c747-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c747-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c747-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c747-123">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="6c747-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




