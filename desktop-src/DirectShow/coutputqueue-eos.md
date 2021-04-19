---
description: La méthode EOS fournit un appel de fin de flux à la broche d’entrée.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: COutputQueue. EOS, méthode (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534787"
---
# <a name="coutputqueueeos-method"></a><span data-ttu-id="232a0-103">COutputQueue. EOS, méthode</span><span class="sxs-lookup"><span data-stu-id="232a0-103">COutputQueue.EOS method</span></span>

<span data-ttu-id="232a0-104">La `EOS` méthode fournit un appel de fin de flux à la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="232a0-104">The `EOS` method delivers an end-of-stream call to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="232a0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="232a0-105">Syntax</span></span>


```C++
void EOS();
```



## <a name="parameters"></a><span data-ttu-id="232a0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="232a0-106">Parameters</span></span>

<span data-ttu-id="232a0-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="232a0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="232a0-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="232a0-108">Return value</span></span>

<span data-ttu-id="232a0-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="232a0-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="232a0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="232a0-110">Remarks</span></span>

<span data-ttu-id="232a0-111">Si l’objet utilise un thread, il met en file d’attente un \_ message de contrôle de paquet EOS.</span><span class="sxs-lookup"><span data-stu-id="232a0-111">If the object is using a thread, it queues an EOS\_PACKET control message.</span></span> <span data-ttu-id="232a0-112">Le thread remet tous les échantillons en attente et appelle la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="232a0-112">The thread delivers any pending samples and calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

<span data-ttu-id="232a0-113">Si l’objet n’utilise pas de thread, il appelle la méthode [**COutputQueue :: SendAnyway**](coutputqueue-sendanyway.md) pour remettre tous les échantillons en attente.</span><span class="sxs-lookup"><span data-stu-id="232a0-113">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="232a0-114">Ensuite, il appelle **IPIN :: EndOfStream** sur la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="232a0-114">Then it calls **IPin::EndOfStream** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="232a0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="232a0-115">Requirements</span></span>



| <span data-ttu-id="232a0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="232a0-116">Requirement</span></span> | <span data-ttu-id="232a0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="232a0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="232a0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="232a0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="232a0-119"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="232a0-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="232a0-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="232a0-120">Library</span></span><br/> | <dl> <span data-ttu-id="232a0-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="232a0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="232a0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="232a0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="232a0-123">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="232a0-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




