---
description: L' \_ \_ énumération DEXTERF Track Search \_ Flags spécifie les conditions limites sur une recherche d’un objet dans la chronologie.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Énumération DEXTERF_TRACK_SEARCH_FLAGS (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537589"
---
# <a name="dexterf_track_search_flags-enumeration"></a><span data-ttu-id="22f88-103">\_ \_ Énumération d’indicateurs de recherche DEXTERF Track \_</span><span class="sxs-lookup"><span data-stu-id="22f88-103">DEXTERF\_TRACK\_SEARCH\_FLAGS enumeration</span></span>

> [!Note]  
> <span data-ttu-id="22f88-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="22f88-104">\[Deprecated.</span></span> <span data-ttu-id="22f88-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22f88-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22f88-106">L' `DEXTERF_TRACK_SEARCH_FLAGS` énumération spécifie les conditions limites sur une recherche d’un objet dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="22f88-106">The `DEXTERF_TRACK_SEARCH_FLAGS` enumeration specifies the boundary conditions on a search for an object in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="22f88-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22f88-107">Syntax</span></span>


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="22f88-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="22f88-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="22f88-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**délimitation DEXTERF \_**</span><span class="sxs-lookup"><span data-stu-id="22f88-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DEXTERF\_BOUNDING**</span></span>
</dt> <dd>

<span data-ttu-id="22f88-110">Recherche un objet qui s’étend sur l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="22f88-110">Search for an object that spans the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="22f88-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ exactement \_ à**</span><span class="sxs-lookup"><span data-stu-id="22f88-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF\_EXACTLY\_AT**</span></span>
</dt> <dd>

<span data-ttu-id="22f88-112">Recherche un objet qui démarre exactement à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="22f88-112">Search for an object that starts exactly at the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="22f88-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF les \_ transferts**</span><span class="sxs-lookup"><span data-stu-id="22f88-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF\_FORWARDS**</span></span>
</dt> <dd>

<span data-ttu-id="22f88-114">Recherchez un objet qui commence à l’heure spécifiée ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="22f88-114">Search for an object that starts at the specified time or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22f88-115">Notes</span><span class="sxs-lookup"><span data-stu-id="22f88-115">Remarks</span></span>

<span data-ttu-id="22f88-116">Ces conditions limites sont résumées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22f88-116">These boundary conditions are summarized in the following table.</span></span>



| <span data-ttu-id="22f88-117">Valeur d'énumération</span><span class="sxs-lookup"><span data-stu-id="22f88-117">Enumeration value</span></span>    | <span data-ttu-id="22f88-118">Condition limite</span><span class="sxs-lookup"><span data-stu-id="22f88-118">Boundary condition</span></span>                        |
|----------------------|-------------------------------------------|
| <span data-ttu-id="22f88-119">délimitation DEXTERF \_</span><span class="sxs-lookup"><span data-stu-id="22f88-119">DEXTERF\_BOUNDING</span></span>    | <span data-ttu-id="22f88-120">Start <= TimeStop > Time</span><span class="sxs-lookup"><span data-stu-id="22f88-120">Start <= TimeStop > Time</span></span><br/> |
| <span data-ttu-id="22f88-121">DEXTERF \_ exactement \_ à</span><span class="sxs-lookup"><span data-stu-id="22f88-121">DEXTERF\_EXACTLY\_AT</span></span> | <span data-ttu-id="22f88-122">Start = = heure</span><span class="sxs-lookup"><span data-stu-id="22f88-122">Start == Time</span></span>                             |
| <span data-ttu-id="22f88-123">DEXTERF les \_ transferts</span><span class="sxs-lookup"><span data-stu-id="22f88-123">DEXTERF\_FORWARDS</span></span>    | <span data-ttu-id="22f88-124">>de début = heure</span><span class="sxs-lookup"><span data-stu-id="22f88-124">Start >= Time</span></span>                          |



 

-   <span data-ttu-id="22f88-125">Start : heure de début de l’objet récupéré.</span><span class="sxs-lookup"><span data-stu-id="22f88-125">Start: start time of the retrieved object.</span></span>
-   <span data-ttu-id="22f88-126">Arrêter : heure d’arrêt de l’objet récupéré.</span><span class="sxs-lookup"><span data-stu-id="22f88-126">Stop: stop time of the retrieved object.</span></span>
-   <span data-ttu-id="22f88-127">Heure : durée de recherche spécifiée.</span><span class="sxs-lookup"><span data-stu-id="22f88-127">Time: specified search time.</span></span>

## <a name="requirements"></a><span data-ttu-id="22f88-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22f88-128">Requirements</span></span>



| <span data-ttu-id="22f88-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22f88-129">Requirement</span></span> | <span data-ttu-id="22f88-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="22f88-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22f88-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="22f88-131">Header</span></span><br/> | <dl> <span data-ttu-id="22f88-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="22f88-132"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22f88-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22f88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22f88-134">**IAMTimelineTrack::GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="22f88-134">**IAMTimelineTrack::GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




