---
description: Indicateur qui spécifie si l’objet fournit des exemples dans des lots exacts.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Membre COutputQueue :: m_bBatchExact (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539991"
---
# <a name="coutputqueuem_bbatchexact-member"></a><span data-ttu-id="34adc-103">COutputQueue :: m \_ bBatchExact, membre</span><span class="sxs-lookup"><span data-stu-id="34adc-103">COutputQueue::m\_bBatchExact member</span></span>

<span data-ttu-id="34adc-104">Indicateur qui spécifie si l’objet fournit des exemples dans des lots exacts.</span><span class="sxs-lookup"><span data-stu-id="34adc-104">Flag that specifies whether the object delivers samples in exact batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="34adc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34adc-105">Syntax</span></span>


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a><span data-ttu-id="34adc-106">Notes</span><span class="sxs-lookup"><span data-stu-id="34adc-106">Remarks</span></span>

<span data-ttu-id="34adc-107">Si la valeur est **true**, l’objet attend jusqu’à ce qu’il dispose d’un lot complet d’exemples de supports avant d’en émettre un.</span><span class="sxs-lookup"><span data-stu-id="34adc-107">If the value is **TRUE**, the object waits until it has a complete batch of media samples before delivering any.</span></span> <span data-ttu-id="34adc-108">Dans le cas contraire, il fournit des exemples à mesure qu’ils arrivent.</span><span class="sxs-lookup"><span data-stu-id="34adc-108">Otherwise, it delivers samples as they arrive.</span></span> <span data-ttu-id="34adc-109">La variable membre [**COutputQueue :: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) définit la taille du lot.</span><span class="sxs-lookup"><span data-stu-id="34adc-109">The [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md) member variable defines the batch size.</span></span>

## <a name="requirements"></a><span data-ttu-id="34adc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34adc-110">Requirements</span></span>



| <span data-ttu-id="34adc-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34adc-111">Requirement</span></span> | <span data-ttu-id="34adc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="34adc-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34adc-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="34adc-113">Header</span></span><br/>  | <dl> <span data-ttu-id="34adc-114"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34adc-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34adc-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="34adc-115">Library</span></span><br/> | <dl> <span data-ttu-id="34adc-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34adc-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34adc-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34adc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34adc-118">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="34adc-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




