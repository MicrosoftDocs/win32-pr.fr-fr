---
description: État de blocage.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: 'Membre CDynamicOutputPin :: m_BlockState (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f02a59854b381db5e7b13a85ccca0754cc38f51d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541370"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a><span data-ttu-id="ffed9-103">CDynamicOutputPin :: m \_ BlockState, membre</span><span class="sxs-lookup"><span data-stu-id="ffed9-103">CDynamicOutputPin::m\_BlockState member</span></span>

<span data-ttu-id="ffed9-104">État de blocage.</span><span class="sxs-lookup"><span data-stu-id="ffed9-104">Blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffed9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffed9-105">Syntax</span></span>


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a><span data-ttu-id="ffed9-106">Notes</span><span class="sxs-lookup"><span data-stu-id="ffed9-106">Remarks</span></span>

<span data-ttu-id="ffed9-107">Les États suivants sont définis :</span><span class="sxs-lookup"><span data-stu-id="ffed9-107">The following states are defined:</span></span>

-   <span data-ttu-id="ffed9-108">NON \_ bloqué</span><span class="sxs-lookup"><span data-stu-id="ffed9-108">NOT\_BLOCKED</span></span>
-   <span data-ttu-id="ffed9-109">PENDING</span><span class="sxs-lookup"><span data-stu-id="ffed9-109">PENDING</span></span>
-   <span data-ttu-id="ffed9-110">OBSTRUÉ</span><span class="sxs-lookup"><span data-stu-id="ffed9-110">BLOCKED</span></span>

<span data-ttu-id="ffed9-111">Avant d’accéder à cette variable, maintenez la section critique [**CDynamicOutputPin :: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="ffed9-111">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffed9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffed9-112">Requirements</span></span>



| <span data-ttu-id="ffed9-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffed9-113">Requirement</span></span> | <span data-ttu-id="ffed9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffed9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffed9-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffed9-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ffed9-116"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffed9-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ffed9-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ffed9-117">Library</span></span><br/> | <dl> <span data-ttu-id="ffed9-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ffed9-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffed9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffed9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffed9-120">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="ffed9-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




