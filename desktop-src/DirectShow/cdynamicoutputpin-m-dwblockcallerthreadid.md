---
description: 'Identificateur du thread qui a appelé la méthode IPinFlowControl :: Block sur ce code confidentiel. Cette variable membre est valide uniquement lorsque le code confidentiel est bloqué.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Membre CDynamicOutputPin :: m_dwBlockCallerThreadID (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542782"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a><span data-ttu-id="9135c-104">CDynamicOutputPin :: m \_ dwBlockCallerThreadID, membre</span><span class="sxs-lookup"><span data-stu-id="9135c-104">CDynamicOutputPin::m\_dwBlockCallerThreadID member</span></span>

<span data-ttu-id="9135c-105">Identificateur du thread qui a appelé la méthode [**IPinFlowControl :: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) sur ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="9135c-105">The identifier of the thread that last called the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method on this pin.</span></span> <span data-ttu-id="9135c-106">Cette variable membre est valide uniquement lorsque le code confidentiel est bloqué.</span><span class="sxs-lookup"><span data-stu-id="9135c-106">This member variable is only valid while the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="9135c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9135c-107">Syntax</span></span>


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a><span data-ttu-id="9135c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="9135c-108">Remarks</span></span>

<span data-ttu-id="9135c-109">Avant d’accéder à cette variable, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="9135c-109">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="9135c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9135c-110">Requirements</span></span>



| <span data-ttu-id="9135c-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9135c-111">Requirement</span></span> | <span data-ttu-id="9135c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9135c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9135c-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="9135c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9135c-114"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9135c-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9135c-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9135c-115">Library</span></span><br/> | <dl> <span data-ttu-id="9135c-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9135c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9135c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9135c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9135c-118">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="9135c-118">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




