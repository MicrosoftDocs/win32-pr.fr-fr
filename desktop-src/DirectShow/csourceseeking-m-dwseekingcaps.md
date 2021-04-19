---
description: Fonctionnalités de recherche.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Membre CSourceSeeking :: m_dwSeekingCaps (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525505"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a><span data-ttu-id="5f85e-103">CSourceSeeking :: m \_ dwSeekingCaps, membre</span><span class="sxs-lookup"><span data-stu-id="5f85e-103">CSourceSeeking::m\_dwSeekingCaps member</span></span>

<span data-ttu-id="5f85e-104">Fonctionnalités de recherche.</span><span class="sxs-lookup"><span data-stu-id="5f85e-104">Seeking capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f85e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f85e-105">Syntax</span></span>


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a><span data-ttu-id="5f85e-106">Notes</span><span class="sxs-lookup"><span data-stu-id="5f85e-106">Remarks</span></span>

<span data-ttu-id="5f85e-107">Par défaut, la valeur est définie sur la combinaison d’opérations de bits des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="5f85e-107">By default, the value is set to the bitwise combination of the following flags:</span></span>

-   <span data-ttu-id="5f85e-108">\_Recherche de \_ CanSeekForwards</span><span class="sxs-lookup"><span data-stu-id="5f85e-108">AM\_SEEKING\_CanSeekForwards</span></span>
-   <span data-ttu-id="5f85e-109">\_Recherche de \_ CanSeekBackwards</span><span class="sxs-lookup"><span data-stu-id="5f85e-109">AM\_SEEKING\_CanSeekBackwards</span></span>
-   <span data-ttu-id="5f85e-110">\_Recherche de \_ CanSeekAbsolute</span><span class="sxs-lookup"><span data-stu-id="5f85e-110">AM\_SEEKING\_CanSeekAbsolute</span></span>
-   <span data-ttu-id="5f85e-111">\_Recherche de \_ CanGetStopPos</span><span class="sxs-lookup"><span data-stu-id="5f85e-111">AM\_SEEKING\_CanGetStopPos</span></span>
-   <span data-ttu-id="5f85e-112">\_Recherche de \_ CanGetDuration</span><span class="sxs-lookup"><span data-stu-id="5f85e-112">AM\_SEEKING\_CanGetDuration</span></span>

<span data-ttu-id="5f85e-113">Si le filtre prend en charge un ensemble de fonctionnalités différent, remplacez cette valeur.</span><span class="sxs-lookup"><span data-stu-id="5f85e-113">If the filter supports a different set of capabilities, override this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f85e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f85e-114">Requirements</span></span>



| <span data-ttu-id="5f85e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f85e-115">Requirement</span></span> | <span data-ttu-id="5f85e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f85e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f85e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f85e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5f85e-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f85e-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5f85e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f85e-119">Library</span></span><br/> | <dl> <span data-ttu-id="5f85e-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5f85e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f85e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f85e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f85e-122">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="5f85e-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




