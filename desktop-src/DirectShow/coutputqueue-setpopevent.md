---
description: La méthode SetPopEvent spécifie un événement qui est signalé chaque fois que l’objet supprime un échantillon de la file d’attente.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Méthode COutputQueue. SetPopEvent (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527994"
---
# <a name="coutputqueuesetpopevent-method"></a><span data-ttu-id="cca99-103">Méthode COutputQueue. SetPopEvent</span><span class="sxs-lookup"><span data-stu-id="cca99-103">COutputQueue.SetPopEvent method</span></span>

<span data-ttu-id="cca99-104">La `SetPopEvent` méthode spécifie un événement qui est signalé chaque fois que l’objet supprime un échantillon de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="cca99-104">The `SetPopEvent` method specifies an event that is signaled whenever the object removes a sample from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca99-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cca99-105">Syntax</span></span>


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="cca99-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cca99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca99-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="cca99-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="cca99-108">Handle vers un événement créé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="cca99-108">Handle to an event created by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca99-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cca99-109">Return value</span></span>

<span data-ttu-id="cca99-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cca99-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cca99-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cca99-111">Requirements</span></span>



| <span data-ttu-id="cca99-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cca99-112">Requirement</span></span> | <span data-ttu-id="cca99-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="cca99-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca99-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="cca99-114">Header</span></span><br/>  | <dl> <span data-ttu-id="cca99-115"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cca99-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cca99-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cca99-116">Library</span></span><br/> | <dl> <span data-ttu-id="cca99-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cca99-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca99-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cca99-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca99-119">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="cca99-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




