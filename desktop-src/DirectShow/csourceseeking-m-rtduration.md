---
description: 'Durée du flux. Par défaut, la valeur est définie sur la valeur de la variable membre CSourceSeeking :: m \_ rtStop.'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Membre CSourceSeeking :: m_rtDuration (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535278"
---
# <a name="csourceseekingm_rtduration-member"></a><span data-ttu-id="097fc-104">CSourceSeeking :: m \_ rtDuration, membre</span><span class="sxs-lookup"><span data-stu-id="097fc-104">CSourceSeeking::m\_rtDuration member</span></span>

<span data-ttu-id="097fc-105">Durée du flux.</span><span class="sxs-lookup"><span data-stu-id="097fc-105">Duration of the stream.</span></span> <span data-ttu-id="097fc-106">Par défaut, la valeur est définie sur la valeur de la variable membre [**CSourceSeeking :: m \_ rtStop**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="097fc-106">By default, the value is set to the value of the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="097fc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="097fc-107">Syntax</span></span>


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a><span data-ttu-id="097fc-108">Notes</span><span class="sxs-lookup"><span data-stu-id="097fc-108">Remarks</span></span>

<span data-ttu-id="097fc-109">Conservez la section critique **m \_ pLock** avant d’accéder à cette variable.</span><span class="sxs-lookup"><span data-stu-id="097fc-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="097fc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="097fc-110">Requirements</span></span>



| <span data-ttu-id="097fc-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="097fc-111">Requirement</span></span> | <span data-ttu-id="097fc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="097fc-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="097fc-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="097fc-113">Header</span></span><br/>  | <dl> <span data-ttu-id="097fc-114"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="097fc-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="097fc-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="097fc-115">Library</span></span><br/> | <dl> <span data-ttu-id="097fc-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="097fc-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="097fc-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="097fc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097fc-118">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="097fc-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




