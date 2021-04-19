---
description: La méthode OnWaitStart met à jour les heures d’attente et de non-attente.
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: Méthode CBaseVideoRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4fab7e1a1f24c3d00f46018db9478990be71666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525160"
---
# <a name="cbasevideorendereronwaitstart-method"></a><span data-ttu-id="03a93-103">Méthode CBaseVideoRenderer. OnWaitStart</span><span class="sxs-lookup"><span data-stu-id="03a93-103">CBaseVideoRenderer.OnWaitStart method</span></span>

<span data-ttu-id="03a93-104">La `OnWaitStart` méthode met à jour les heures d’attente et de non-attente.</span><span class="sxs-lookup"><span data-stu-id="03a93-104">The `OnWaitStart` method updates times spent waiting and not waiting.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a93-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03a93-105">Syntax</span></span>


```C++
void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="03a93-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03a93-106">Parameters</span></span>

<span data-ttu-id="03a93-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="03a93-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03a93-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03a93-108">Return value</span></span>

<span data-ttu-id="03a93-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="03a93-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03a93-110">Notes</span><span class="sxs-lookup"><span data-stu-id="03a93-110">Remarks</span></span>

<span data-ttu-id="03a93-111">Cette fonction membre est appelée lors du démarrage de l’attente d’un événement de rendu.</span><span class="sxs-lookup"><span data-stu-id="03a93-111">This member function is called when starting to wait for a rendering event.</span></span> <span data-ttu-id="03a93-112">Elle est utilisée uniquement pour les mesures de performances.</span><span class="sxs-lookup"><span data-stu-id="03a93-112">It is used only for performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a93-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03a93-113">Requirements</span></span>



| <span data-ttu-id="03a93-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03a93-114">Requirement</span></span> | <span data-ttu-id="03a93-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="03a93-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a93-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="03a93-116">Header</span></span><br/>  | <dl> <span data-ttu-id="03a93-117"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03a93-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03a93-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="03a93-118">Library</span></span><br/> | <dl> <span data-ttu-id="03a93-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="03a93-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a93-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03a93-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a93-121">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="03a93-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




