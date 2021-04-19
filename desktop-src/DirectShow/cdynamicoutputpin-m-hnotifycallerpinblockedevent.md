---
description: Événement signalé lorsque le code confidentiel se bloque correctement ou lorsque l’utilisateur annule un bloc en attente.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Membre CDynamicOutputPin :: m_hNotifyCallerPinBlockedEvent (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545368"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a><span data-ttu-id="c7c0d-103">CDynamicOutputPin :: m \_ hNotifyCallerPinBlockedEvent, membre</span><span class="sxs-lookup"><span data-stu-id="c7c0d-103">CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent member</span></span>

<span data-ttu-id="c7c0d-104">Événement signalé lorsque le code confidentiel se bloque correctement ou lorsque l’utilisateur annule un bloc en attente.</span><span class="sxs-lookup"><span data-stu-id="c7c0d-104">Event that is signaled when the pin successfully blocks, or the user cancels a pending block.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7c0d-105">Syntax</span></span>


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a><span data-ttu-id="c7c0d-106">Notes</span><span class="sxs-lookup"><span data-stu-id="c7c0d-106">Remarks</span></span>

<span data-ttu-id="c7c0d-107">Avant d’accéder à cette variable, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="c7c0d-107">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c0d-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7c0d-108">Requirements</span></span>



| <span data-ttu-id="c7c0d-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7c0d-109">Requirement</span></span> | <span data-ttu-id="c7c0d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7c0d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c0d-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7c0d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="c7c0d-112"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7c0d-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c7c0d-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c7c0d-113">Library</span></span><br/> | <dl> <span data-ttu-id="c7c0d-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c7c0d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c0d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7c0d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c0d-116">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="c7c0d-116">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




