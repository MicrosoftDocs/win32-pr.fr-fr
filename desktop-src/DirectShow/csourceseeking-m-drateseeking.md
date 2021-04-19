---
description: Vitesse de lecture. Par défaut, la valeur est définie sur 1,0.
ms.assetid: 835ddbe8-2017-4a4a-8f10-b3f33a8215a7
title: 'Membre CSourceSeeking :: m_dRateSeeking (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dRateSeeking
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1055a420316868db6374798c0295339dd74ac172
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537757"
---
# <a name="csourceseekingm_drateseeking-member"></a><span data-ttu-id="79c39-104">CSourceSeeking :: m \_ dRateSeeking, membre</span><span class="sxs-lookup"><span data-stu-id="79c39-104">CSourceSeeking::m\_dRateSeeking member</span></span>

<span data-ttu-id="79c39-105">Vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="79c39-105">Playback rate.</span></span> <span data-ttu-id="79c39-106">Par défaut, la valeur est définie sur 1,0.</span><span class="sxs-lookup"><span data-stu-id="79c39-106">By default, the value is set to 1.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c39-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79c39-107">Syntax</span></span>


```C++
double m_dRateSeeking;
```



## <a name="remarks"></a><span data-ttu-id="79c39-108">Notes</span><span class="sxs-lookup"><span data-stu-id="79c39-108">Remarks</span></span>

<span data-ttu-id="79c39-109">Conservez la section critique **m \_ pLock** avant d’accéder à cette variable.</span><span class="sxs-lookup"><span data-stu-id="79c39-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c39-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79c39-110">Requirements</span></span>



| <span data-ttu-id="79c39-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79c39-111">Requirement</span></span> | <span data-ttu-id="79c39-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="79c39-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c39-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="79c39-113">Header</span></span><br/>  | <dl> <span data-ttu-id="79c39-114"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79c39-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79c39-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="79c39-115">Library</span></span><br/> | <dl> <span data-ttu-id="79c39-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="79c39-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79c39-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79c39-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c39-118">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="79c39-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




