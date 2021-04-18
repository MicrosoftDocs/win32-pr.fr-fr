---
description: Heure d’arrêt. Par défaut, la valeur est définie sur un très grand nombre. La classe dérivée peut réinitialiser la valeur dans son constructeur, ou lorsque le filtre est initialisé.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Membre CSourceSeeking :: m_rtStop (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540561"
---
# <a name="csourceseekingm_rtstop-member"></a><span data-ttu-id="5bf7f-105">CSourceSeeking :: m \_ rtStop, membre</span><span class="sxs-lookup"><span data-stu-id="5bf7f-105">CSourceSeeking::m\_rtStop member</span></span>

<span data-ttu-id="5bf7f-106">Heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5bf7f-106">Stop time.</span></span> <span data-ttu-id="5bf7f-107">Par défaut, la valeur est définie sur un très grand nombre.</span><span class="sxs-lookup"><span data-stu-id="5bf7f-107">By default, the value is set to a very large number.</span></span> <span data-ttu-id="5bf7f-108">La classe dérivée peut réinitialiser la valeur dans son constructeur, ou lorsque le filtre est initialisé.</span><span class="sxs-lookup"><span data-stu-id="5bf7f-108">The derived class can reset the value in its constructor, or when the filter is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf7f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bf7f-109">Syntax</span></span>


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a><span data-ttu-id="5bf7f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5bf7f-110">Remarks</span></span>

<span data-ttu-id="5bf7f-111">Conservez la section critique **m \_ pLock** avant d’accéder à cette variable.</span><span class="sxs-lookup"><span data-stu-id="5bf7f-111">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf7f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bf7f-112">Requirements</span></span>



| <span data-ttu-id="5bf7f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bf7f-113">Requirement</span></span> | <span data-ttu-id="5bf7f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bf7f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf7f-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="5bf7f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5bf7f-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bf7f-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5bf7f-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5bf7f-117">Library</span></span><br/> | <dl> <span data-ttu-id="5bf7f-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5bf7f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bf7f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bf7f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf7f-120">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="5bf7f-120">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




