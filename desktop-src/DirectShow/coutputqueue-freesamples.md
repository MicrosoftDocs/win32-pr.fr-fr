---
description: La méthode FreeSamples libère tous les échantillons en attente.
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: Méthode COutputQueue. FreeSamples (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70d0680d2a1a3ac020be84f244e1cc02bb6efad0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525534"
---
# <a name="coutputqueuefreesamples-method"></a><span data-ttu-id="a7e30-103">Méthode COutputQueue. FreeSamples</span><span class="sxs-lookup"><span data-stu-id="a7e30-103">COutputQueue.FreeSamples method</span></span>

<span data-ttu-id="a7e30-104">La `FreeSamples` méthode libère tous les échantillons en attente.</span><span class="sxs-lookup"><span data-stu-id="a7e30-104">The `FreeSamples` method frees all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7e30-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7e30-105">Syntax</span></span>


```C++
void FreeSamples();
```



## <a name="parameters"></a><span data-ttu-id="a7e30-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7e30-106">Parameters</span></span>

<span data-ttu-id="a7e30-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a7e30-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7e30-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7e30-108">Return value</span></span>

<span data-ttu-id="a7e30-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a7e30-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7e30-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a7e30-110">Remarks</span></span>

<span data-ttu-id="a7e30-111">Cette méthode supprime tous les échantillons en attente de la file d’attente et de l’exemple de tableau.</span><span class="sxs-lookup"><span data-stu-id="a7e30-111">This method removes any pending samples from the queue and from the sample array.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7e30-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7e30-112">Requirements</span></span>



| <span data-ttu-id="a7e30-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7e30-113">Requirement</span></span> | <span data-ttu-id="a7e30-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7e30-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e30-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7e30-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a7e30-116"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7e30-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7e30-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a7e30-117">Library</span></span><br/> | <dl> <span data-ttu-id="a7e30-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a7e30-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7e30-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7e30-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e30-120">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="a7e30-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




