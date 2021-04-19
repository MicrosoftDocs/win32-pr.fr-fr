---
description: La \_ structure PERFINFO DShow \_ AVREND contient des données pour un événement de trace de type GUID \_ VIDEOREND. VMR enregistre cet événement immédiatement avant le rendu d’un frame.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: Structure PERFINFO_DSHOW_AVREND (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531092"
---
# <a name="perfinfo_dshow_avrend-structure"></a><span data-ttu-id="6c396-103">PERFINFO \_ DShow \_ AVREND, structure</span><span class="sxs-lookup"><span data-stu-id="6c396-103">PERFINFO\_DSHOW\_AVREND structure</span></span>

<span data-ttu-id="6c396-104">La `PERFINFO_DSHOW_AVREND` structure contient des données pour un événement de trace de type GUID \_ VIDEOREND.</span><span class="sxs-lookup"><span data-stu-id="6c396-104">The `PERFINFO_DSHOW_AVREND` structure contains data for a trace event of type GUID\_VIDEOREND.</span></span>

<span data-ttu-id="6c396-105">VMR enregistre cet événement immédiatement avant le rendu d’un frame.</span><span class="sxs-lookup"><span data-stu-id="6c396-105">The VMR logs this event immediately before rendering a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c396-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c396-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a><span data-ttu-id="6c396-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6c396-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6c396-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="6c396-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="6c396-109">Dernier nombre de cycles d’horloge (instruction RDTSC).</span><span class="sxs-lookup"><span data-stu-id="6c396-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="6c396-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="6c396-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="6c396-111">Heure de référence actuelle, telle qu’elle est retournée par la méthode [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="6c396-111">Current reference time, as returned by the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

</dd> <dt>

<span data-ttu-id="6c396-112">**sampleTime**</span><span class="sxs-lookup"><span data-stu-id="6c396-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="6c396-113">Heure de début de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="6c396-113">Start time of the sample.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c396-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6c396-114">Remarks</span></span>

<span data-ttu-id="6c396-115">Pour activer cet événement, vous devez définir l' \_ indicateur DXMPERF VIDEOREND dans le paramètre *EnableFlag* lorsque vous appelez **EnableTrace**.</span><span class="sxs-lookup"><span data-stu-id="6c396-115">To enable this event, you must set the DXMPERF\_VIDEOREND flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="6c396-116">Cet indicateur est défini dans le fichier d’en-tête Dxmperf. h, qui est inclus dans les classes de base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6c396-116">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="6c396-117">Pour enregistrer cet événement à partir d’un filtre DirectShow, utilisez la macro **PERFLOG \_ VIDEOREND** , qui est définie dans Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="6c396-117">To log this event from a DirectShow filter, use the **PERFLOG\_VIDEOREND** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c396-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c396-118">Requirements</span></span>



| <span data-ttu-id="6c396-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c396-119">Requirement</span></span> | <span data-ttu-id="6c396-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c396-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c396-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c396-121">Header</span></span><br/> | <dl> <span data-ttu-id="6c396-122"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c396-122"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c396-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c396-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c396-124">Structures DirectShow</span><span class="sxs-lookup"><span data-stu-id="6c396-124">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="6c396-125">Suivi d’événements dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="6c396-125">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="6c396-126">GUID d’événements de trace</span><span class="sxs-lookup"><span data-stu-id="6c396-126">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




