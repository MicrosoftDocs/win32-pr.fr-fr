---
description: La \_ structure PERFINFO DShow \_ AUDIOBREAK contient des données pour un événement de trace de type GUID \_ AUDIOBREAK. Le filtre de convertisseur DirectSound enregistre cet événement en cas de rupture dans le flux audio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: Structure PERFINFO_DSHOW_AUDIOBREAK (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544118"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a><span data-ttu-id="745a3-103">PERFINFO \_ DShow \_ AUDIOBREAK, structure</span><span class="sxs-lookup"><span data-stu-id="745a3-103">PERFINFO\_DSHOW\_AUDIOBREAK structure</span></span>

<span data-ttu-id="745a3-104">La `PERFINFO_DSHOW_AUDIOBREAK` structure contient des données pour un événement de trace de type GUID \_ AUDIOBREAK.</span><span class="sxs-lookup"><span data-stu-id="745a3-104">The `PERFINFO_DSHOW_AUDIOBREAK` structure contains data for a trace event of type GUID\_AUDIOBREAK.</span></span>

<span data-ttu-id="745a3-105">Le filtre de [convertisseur DirectSound](directsound-renderer-filter.md) enregistre cet événement en cas de rupture dans le flux audio.</span><span class="sxs-lookup"><span data-stu-id="745a3-105">The [DirectSound Renderer](directsound-renderer-filter.md) filter logs this event when there is a break in the audio stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="745a3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="745a3-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a><span data-ttu-id="745a3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="745a3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="745a3-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="745a3-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="745a3-109">Dernier nombre de cycles d’horloge (instruction RDTSC).</span><span class="sxs-lookup"><span data-stu-id="745a3-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="745a3-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="745a3-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="745a3-111">Position d’écriture actuelle dans la mémoire tampon DirectSound.</span><span class="sxs-lookup"><span data-stu-id="745a3-111">Current write position in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="745a3-112">**sampleTime**</span><span class="sxs-lookup"><span data-stu-id="745a3-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="745a3-113">Début de la coupure audio dans la mémoire tampon DirectSound.</span><span class="sxs-lookup"><span data-stu-id="745a3-113">Start of the audio break in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="745a3-114">**sampleDuration**</span><span class="sxs-lookup"><span data-stu-id="745a3-114">**sampleDuration**</span></span>
</dt> <dd>

<span data-ttu-id="745a3-115">Durée de l’arrêt, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="745a3-115">Duration of the break, in milliseconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="745a3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="745a3-116">Remarks</span></span>

<span data-ttu-id="745a3-117">Pour activer cet événement, vous devez définir l' \_ indicateur de bit AUDIOBREAK dans le paramètre *EnableFlag* lorsque vous appelez **EnableTrace**.</span><span class="sxs-lookup"><span data-stu-id="745a3-117">To enable this event, you must set the AUDIOBREAK\_BIT flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="745a3-118">Cet indicateur est défini dans le fichier d’en-tête Dxmperf. h, qui est inclus dans les classes de base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="745a3-118">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="745a3-119">Pour enregistrer cet événement à partir d’un filtre DirectShow, utilisez la macro **PERFLOG \_ AUDIOBREAK** , qui est définie dans Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="745a3-119">To log this event from a DirectShow filter, use the **PERFLOG\_AUDIOBREAK** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="745a3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="745a3-120">Requirements</span></span>



| <span data-ttu-id="745a3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="745a3-121">Requirement</span></span> | <span data-ttu-id="745a3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="745a3-122">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="745a3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="745a3-123">Header</span></span><br/> | <dl> <span data-ttu-id="745a3-124"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="745a3-124"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="745a3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="745a3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="745a3-126">Structures DirectShow</span><span class="sxs-lookup"><span data-stu-id="745a3-126">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="745a3-127">Suivi d’événements dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="745a3-127">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="745a3-128">GUID d’événements de trace</span><span class="sxs-lookup"><span data-stu-id="745a3-128">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




