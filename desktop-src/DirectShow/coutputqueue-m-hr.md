---
description: Valeur HRESULT qui indique si l’objet accepte des exemples. Si la valeur est \_ OK, l’objet accepte des exemples. Dans le cas contraire, il rejette les exemples.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Membre COutputQueue :: m_hr (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540429"
---
# <a name="coutputqueuem_hr-member"></a><span data-ttu-id="e1f5a-105">COutputQueue :: m \_ membre HR</span><span class="sxs-lookup"><span data-stu-id="e1f5a-105">COutputQueue::m\_hr member</span></span>

<span data-ttu-id="e1f5a-106">Valeur **HRESULT** qui indique si l’objet accepte des exemples.</span><span class="sxs-lookup"><span data-stu-id="e1f5a-106">**HRESULT** value that indicates whether the object will accept samples.</span></span> <span data-ttu-id="e1f5a-107">Si la valeur est \_ OK, l’objet accepte des exemples.</span><span class="sxs-lookup"><span data-stu-id="e1f5a-107">If the value is S\_OK, the object will accept samples.</span></span> <span data-ttu-id="e1f5a-108">Dans le cas contraire, il rejette les exemples.</span><span class="sxs-lookup"><span data-stu-id="e1f5a-108">Otherwise, it rejects samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f5a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1f5a-109">Syntax</span></span>


```C++
HRESULT m_hr;
```



## <a name="remarks"></a><span data-ttu-id="e1f5a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e1f5a-110">Remarks</span></span>

<span data-ttu-id="e1f5a-111">Cette variable membre est utilisée pour coordonner les activités entre les threads.</span><span class="sxs-lookup"><span data-stu-id="e1f5a-111">This member variable is used to coordinate activities across threads.</span></span> <span data-ttu-id="e1f5a-112">Si la broche d’entrée en aval rejette un échantillon, ou si l’objet commence à être vidé, la valeur est définie sur S \_ false ou sur un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e1f5a-112">If the downstream input pin rejects a sample, or if the object begins flushing, the value is set to S\_FALSE or an error code.</span></span> <span data-ttu-id="e1f5a-113">L’objet ne remet plus d’exemples jusqu’à ce que le vidage soit terminé ou jusqu’à ce que la méthode [**COutputQueue :: Reset**](coutputqueue-reset.md) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="e1f5a-113">The object will not deliver any more samples until flushing is complete, or until the [**COutputQueue::Reset**](coutputqueue-reset.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f5a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1f5a-114">Requirements</span></span>



| <span data-ttu-id="e1f5a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1f5a-115">Requirement</span></span> | <span data-ttu-id="e1f5a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1f5a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f5a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1f5a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e1f5a-118"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1f5a-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1f5a-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e1f5a-119">Library</span></span><br/> | <dl> <span data-ttu-id="e1f5a-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e1f5a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f5a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1f5a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f5a-122">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="e1f5a-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




