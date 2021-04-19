---
description: Récupère l’élément suivant de la file d’attente.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Méthode CQueue. GetQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539298"
---
# <a name="cqueuegetqueueobject-method"></a><span data-ttu-id="4ed8e-103">Méthode CQueue. GetQueueObject</span><span class="sxs-lookup"><span data-stu-id="4ed8e-103">CQueue.GetQueueObject method</span></span>

<span data-ttu-id="4ed8e-104">Récupère l’élément suivant de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-104">Retrieves the next item from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ed8e-105">Syntax</span></span>


```C++
T GetQueueObject();
```



## <a name="parameters"></a><span data-ttu-id="4ed8e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ed8e-106">Parameters</span></span>

<span data-ttu-id="4ed8e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ed8e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ed8e-108">Return value</span></span>

<span data-ttu-id="4ed8e-109">Retourne un objet de type **T** (type de modèle).</span><span class="sxs-lookup"><span data-stu-id="4ed8e-109">Returns an object of type **T** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ed8e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4ed8e-110">Remarks</span></span>

<span data-ttu-id="4ed8e-111">Cette méthode bloque jusqu’à ce qu’un élément soit disponible dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4ed8e-111">This method blocks until an item is available on the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed8e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ed8e-112">Requirements</span></span>



| <span data-ttu-id="4ed8e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ed8e-113">Requirement</span></span> | <span data-ttu-id="4ed8e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ed8e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed8e-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ed8e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4ed8e-116"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ed8e-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4ed8e-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4ed8e-117">Library</span></span><br/> | <dl> <span data-ttu-id="4ed8e-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4ed8e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ed8e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ed8e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed8e-120">**CQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="4ed8e-120">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




