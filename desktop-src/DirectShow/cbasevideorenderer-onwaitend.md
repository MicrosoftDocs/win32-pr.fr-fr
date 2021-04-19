---
description: La méthode OnWaitEnd est appelée lorsqu’un délai d’attente se termine.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Méthode CBaseVideoRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523903"
---
# <a name="cbasevideorendereronwaitend-method"></a><span data-ttu-id="c72bc-103">Méthode CBaseVideoRenderer. OnWaitEnd</span><span class="sxs-lookup"><span data-stu-id="c72bc-103">CBaseVideoRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="c72bc-104">La méthode OnWaitEnd est appelée lorsqu’un délai d’attente se termine.</span><span class="sxs-lookup"><span data-stu-id="c72bc-104">The OnWaitEnd method is called when a wait time ends.</span></span>

## <a name="syntax"></a><span data-ttu-id="c72bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c72bc-105">Syntax</span></span>


```C++
void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="c72bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c72bc-106">Parameters</span></span>

<span data-ttu-id="c72bc-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c72bc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c72bc-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c72bc-108">Return value</span></span>

<span data-ttu-id="c72bc-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c72bc-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c72bc-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c72bc-110">Remarks</span></span>

<span data-ttu-id="c72bc-111">Cette fonction membre effectue uniquement la journalisation des performances.</span><span class="sxs-lookup"><span data-stu-id="c72bc-111">This member function does only performance logging.</span></span> <span data-ttu-id="c72bc-112">Elle est appelée lorsque le thread est activé d’attendre dans la fenêtre, ou lorsque l’exemple suivant est dû à un rendu.</span><span class="sxs-lookup"><span data-stu-id="c72bc-112">It is called when the thread is awoken from waiting in the window, or when the next sample is due to be rendered.</span></span> <span data-ttu-id="c72bc-113">Il peut ensuite être utilisé pour collecter des informations qui contrôlent la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="c72bc-113">It could eventually be used to gather information that controls synchronization.</span></span>

## <a name="requirements"></a><span data-ttu-id="c72bc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c72bc-114">Requirements</span></span>



| <span data-ttu-id="c72bc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c72bc-115">Requirement</span></span> | <span data-ttu-id="c72bc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c72bc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c72bc-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="c72bc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c72bc-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c72bc-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c72bc-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c72bc-119">Library</span></span><br/> | <dl> <span data-ttu-id="c72bc-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c72bc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c72bc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c72bc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72bc-122">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="c72bc-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




