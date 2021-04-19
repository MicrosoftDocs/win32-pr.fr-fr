---
description: Le \_ type de données de temps de référence définit les unités pour les temps de référence dans DirectShow. Chaque unité de temps de référence est de 100 nanosecondes.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539305"
---
# <a name="reference_time"></a><span data-ttu-id="fac17-104">temps de référence \_</span><span class="sxs-lookup"><span data-stu-id="fac17-104">REFERENCE\_TIME</span></span>

<span data-ttu-id="fac17-105">Le type de données de **\_ temps de référence** définit les unités pour les temps de référence dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fac17-105">The **REFERENCE\_TIME** data type defines the units for reference times in DirectShow.</span></span> <span data-ttu-id="fac17-106">Chaque unité de temps de référence est de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="fac17-106">Each unit of reference time is 100 nanoseconds.</span></span>


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a><span data-ttu-id="fac17-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fac17-107">Remarks</span></span>

<span data-ttu-id="fac17-108">Le type de données de **\_ temps de référence** est un entier 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fac17-108">The **REFERENCE\_TIME** data type is a 64-bit integer.</span></span>

<span data-ttu-id="fac17-109">Les temps de référence sont généralement mesurés à partir de l’une des lignes de base suivantes :</span><span class="sxs-lookup"><span data-stu-id="fac17-109">Reference times are usually measured from one of the following baselines:</span></span>

-   <span data-ttu-id="fac17-110">Heure de l’horloge absolue.</span><span class="sxs-lookup"><span data-stu-id="fac17-110">An absolute clock time.</span></span> <span data-ttu-id="fac17-111">Dans ce cas, la base de référence dépend de l’implémentation de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="fac17-111">In this case, the baseline will depend on the implementation of the clock.</span></span> <span data-ttu-id="fac17-112">Pour plus d’informations, consultez [horloges de référence](reference-clocks.md).</span><span class="sxs-lookup"><span data-stu-id="fac17-112">For more information, see [Reference Clocks](reference-clocks.md).</span></span>
-   <span data-ttu-id="fac17-113">Par rapport au début de la lecture.</span><span class="sxs-lookup"><span data-stu-id="fac17-113">Relative to the start of playback.</span></span>

<span data-ttu-id="fac17-114">Pour plus d’informations sur les temps de référence, consultez [temps et horloges dans DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="fac17-114">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fac17-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fac17-115">Requirements</span></span>



| <span data-ttu-id="fac17-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fac17-116">Requirement</span></span> | <span data-ttu-id="fac17-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fac17-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac17-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="fac17-118">Header</span></span><br/> | <dl> <span data-ttu-id="fac17-119"><dt>Strmif. h (inclure DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fac17-119"><dt>Strmif.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac17-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fac17-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac17-121">Types de données DirectShow</span><span class="sxs-lookup"><span data-stu-id="fac17-121">DirectShow Data Types</span></span>](directshow-data-types.md)
</dt> </dl>

 

 




