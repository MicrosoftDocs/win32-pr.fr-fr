---
description: La méthode IsIdle détermine si l’objet attend des données.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: Méthode COutputQueue. IsIdle (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9bf8b42189e356659e74398eaa3eefeb5f771a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526790"
---
# <a name="coutputqueueisidle-method"></a><span data-ttu-id="62b2c-103">Méthode COutputQueue. IsIdle</span><span class="sxs-lookup"><span data-stu-id="62b2c-103">COutputQueue.IsIdle method</span></span>

<span data-ttu-id="62b2c-104">La `IsIdle` méthode détermine si l’objet attend des données.</span><span class="sxs-lookup"><span data-stu-id="62b2c-104">The `IsIdle` method determines whether the object is waiting for data.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b2c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62b2c-105">Syntax</span></span>


```C++
BOOL IsIdle();
```



## <a name="parameters"></a><span data-ttu-id="62b2c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62b2c-106">Parameters</span></span>

<span data-ttu-id="62b2c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="62b2c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62b2c-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62b2c-108">Return value</span></span>

<span data-ttu-id="62b2c-109">Retourne la **valeur true** si le thread est en attente et que l’exemple de tableau est vide.</span><span class="sxs-lookup"><span data-stu-id="62b2c-109">Returns **TRUE** if the thread is waiting and the sample array is empty.</span></span> <span data-ttu-id="62b2c-110">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="62b2c-110">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62b2c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62b2c-111">Requirements</span></span>



| <span data-ttu-id="62b2c-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62b2c-112">Requirement</span></span> | <span data-ttu-id="62b2c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="62b2c-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b2c-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="62b2c-114">Header</span></span><br/>  | <dl> <span data-ttu-id="62b2c-115"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62b2c-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62b2c-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="62b2c-116">Library</span></span><br/> | <dl> <span data-ttu-id="62b2c-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="62b2c-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b2c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62b2c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b2c-119">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="62b2c-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




