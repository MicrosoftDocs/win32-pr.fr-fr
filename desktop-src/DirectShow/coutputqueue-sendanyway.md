---
description: La méthode SendAnyway fournit tous les exemples en attente.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Méthode COutputQueue. SendAnyway (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533728"
---
# <a name="coutputqueuesendanyway-method"></a><span data-ttu-id="49b34-103">Méthode COutputQueue. SendAnyway</span><span class="sxs-lookup"><span data-stu-id="49b34-103">COutputQueue.SendAnyway method</span></span>

<span data-ttu-id="49b34-104">La `SendAnyway` méthode remet tous les échantillons en attente.</span><span class="sxs-lookup"><span data-stu-id="49b34-104">The `SendAnyway` method delivers any pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b34-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49b34-105">Syntax</span></span>


```C++
void SendAnyway();
```



## <a name="parameters"></a><span data-ttu-id="49b34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49b34-106">Parameters</span></span>

<span data-ttu-id="49b34-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="49b34-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49b34-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49b34-108">Return value</span></span>

<span data-ttu-id="49b34-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="49b34-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49b34-110">Notes</span><span class="sxs-lookup"><span data-stu-id="49b34-110">Remarks</span></span>

<span data-ttu-id="49b34-111">Si la variable membre [**COutputQueue :: m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) a la **valeur true**, l’objet remplit le tableau [**COutputQueue :: m \_ ppSamples**](coutputqueue-m-ppsamples.md) avant de fournir un lot d’exemples.</span><span class="sxs-lookup"><span data-stu-id="49b34-111">If the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) member variable is **TRUE**, the object fills the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array before it delivers a batch of samples.</span></span> <span data-ttu-id="49b34-112">Appelez cette méthode pour remettre un lot partiel.</span><span class="sxs-lookup"><span data-stu-id="49b34-112">Call this method to deliver a partial batch.</span></span> <span data-ttu-id="49b34-113">Par exemple, la méthode [**COutputQueue :: EOS**](coutputqueue-eos.md) appelle `SendAnyway` pour sérialiser les messages de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="49b34-113">For example, the [**COutputQueue::EOS**](coutputqueue-eos.md) method calls `SendAnyway` to serialize end-of-stream messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="49b34-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49b34-114">Requirements</span></span>



| <span data-ttu-id="49b34-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49b34-115">Requirement</span></span> | <span data-ttu-id="49b34-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="49b34-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49b34-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="49b34-117">Header</span></span><br/>  | <dl> <span data-ttu-id="49b34-118"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49b34-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49b34-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49b34-119">Library</span></span><br/> | <dl> <span data-ttu-id="49b34-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="49b34-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49b34-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49b34-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b34-122">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="49b34-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




