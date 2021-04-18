---
description: Place un élément dans la file d’attente.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Méthode CQueue. PutQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533177"
---
# <a name="cqueueputqueueobject-method"></a><span data-ttu-id="5ade0-103">Méthode CQueue. PutQueueObject</span><span class="sxs-lookup"><span data-stu-id="5ade0-103">CQueue.PutQueueObject method</span></span>

<span data-ttu-id="5ade0-104">Place un élément dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="5ade0-104">Puts an item onto the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ade0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ade0-105">Syntax</span></span>


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a><span data-ttu-id="5ade0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ade0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ade0-107">*object*</span><span class="sxs-lookup"><span data-stu-id="5ade0-107">*object*</span></span> 
</dt> <dd>

<span data-ttu-id="5ade0-108">Objet de type **T** (type de modèle).</span><span class="sxs-lookup"><span data-stu-id="5ade0-108">Object of type **T** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ade0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ade0-109">Return value</span></span>

<span data-ttu-id="5ade0-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5ade0-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ade0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5ade0-111">Remarks</span></span>

<span data-ttu-id="5ade0-112">Cette méthode bloque jusqu’à ce qu’il y ait de l’espace dans la file d’attente pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="5ade0-112">This method blocks until there is space in the queue for the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ade0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ade0-113">Requirements</span></span>



| <span data-ttu-id="5ade0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ade0-114">Requirement</span></span> | <span data-ttu-id="5ade0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ade0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ade0-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ade0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5ade0-117"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ade0-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5ade0-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ade0-118">Library</span></span><br/> | <dl> <span data-ttu-id="5ade0-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5ade0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ade0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ade0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ade0-121">**CQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="5ade0-121">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




