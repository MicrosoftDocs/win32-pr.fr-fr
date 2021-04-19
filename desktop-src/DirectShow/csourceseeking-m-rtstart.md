---
description: Heure de début La valeur par défaut est définie à zéro.
ms.assetid: bafa69c3-ead0-4409-abbf-4e8cc325e5f9
title: 'Membre CSourceSeeking :: m_rtStart (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStart
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc7bf18f23177095328c1faee8dd8da28e830b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539960"
---
# <a name="csourceseekingm_rtstart-member"></a><span data-ttu-id="7ec7b-104">CSourceSeeking :: m \_ rtStart, membre</span><span class="sxs-lookup"><span data-stu-id="7ec7b-104">CSourceSeeking::m\_rtStart member</span></span>

<span data-ttu-id="7ec7b-105">Heure de début</span><span class="sxs-lookup"><span data-stu-id="7ec7b-105">Start time.</span></span> <span data-ttu-id="7ec7b-106">La valeur par défaut est définie à zéro.</span><span class="sxs-lookup"><span data-stu-id="7ec7b-106">By default, the value is set to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec7b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ec7b-107">Syntax</span></span>


```C++
CRefTime m_rtStart;
```



## <a name="remarks"></a><span data-ttu-id="7ec7b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7ec7b-108">Remarks</span></span>

<span data-ttu-id="7ec7b-109">Conservez la section critique **m \_ pLock** avant d’accéder à cette variable.</span><span class="sxs-lookup"><span data-stu-id="7ec7b-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec7b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ec7b-110">Requirements</span></span>



| <span data-ttu-id="7ec7b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ec7b-111">Requirement</span></span> | <span data-ttu-id="7ec7b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ec7b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec7b-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ec7b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7ec7b-114"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ec7b-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7ec7b-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ec7b-115">Library</span></span><br/> | <dl> <span data-ttu-id="7ec7b-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7ec7b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ec7b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ec7b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec7b-118">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="7ec7b-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




