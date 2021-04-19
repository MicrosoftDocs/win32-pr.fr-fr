---
description: L' \_ \_ énumération de type principal de la chronologie spécifie le type principal d’un objet.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Énumération TIMELINE_MAJOR_TYPE (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528651"
---
# <a name="timeline_major_type-enumeration"></a><span data-ttu-id="e15b1-103">\_Énumération de type principal de chronologie \_</span><span class="sxs-lookup"><span data-stu-id="e15b1-103">TIMELINE\_MAJOR\_TYPE enumeration</span></span>

> [!Note]  
> <span data-ttu-id="e15b1-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e15b1-104">\[Deprecated.</span></span> <span data-ttu-id="e15b1-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e15b1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e15b1-106">L' `TIMELINE_MAJOR_TYPE` énumération spécifie le type principal d’un objet.</span><span class="sxs-lookup"><span data-stu-id="e15b1-106">The `TIMELINE_MAJOR_TYPE` enumeration specifies the major type of an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e15b1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e15b1-107">Syntax</span></span>


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="e15b1-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e15b1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e15b1-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TYPE principal de la chronologie \_ \_ \_ composite**</span><span class="sxs-lookup"><span data-stu-id="e15b1-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TIMELINE\_MAJOR\_TYPE\_COMPOSITE**</span></span>
</dt> <dd>

<span data-ttu-id="e15b1-110">Objet composite.</span><span class="sxs-lookup"><span data-stu-id="e15b1-110">Composite object.</span></span> <span data-ttu-id="e15b1-111">Contient une ou plusieurs pistes.</span><span class="sxs-lookup"><span data-stu-id="e15b1-111">Holds one or more tracks.</span></span>

</dd> <dt>

<span data-ttu-id="e15b1-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**\_piste de \_ type \_ principal de la chronologie**</span><span class="sxs-lookup"><span data-stu-id="e15b1-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**TIMELINE\_MAJOR\_TYPE\_TRACK**</span></span>
</dt> <dd>

<span data-ttu-id="e15b1-113">Objet Track.</span><span class="sxs-lookup"><span data-stu-id="e15b1-113">Track object.</span></span> <span data-ttu-id="e15b1-114">Contient une ou plusieurs sources.</span><span class="sxs-lookup"><span data-stu-id="e15b1-114">Holds one or more sources.</span></span>

</dd> <dt>

<span data-ttu-id="e15b1-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**\_source de \_ type \_ principal de la chronologie**</span><span class="sxs-lookup"><span data-stu-id="e15b1-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**TIMELINE\_MAJOR\_TYPE\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="e15b1-116">Objet source.</span><span class="sxs-lookup"><span data-stu-id="e15b1-116">Source object.</span></span> <span data-ttu-id="e15b1-117">Contient une référence à une source de média.</span><span class="sxs-lookup"><span data-stu-id="e15b1-117">Contains a reference to a media source.</span></span>

</dd> <dt>

<span data-ttu-id="e15b1-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**\_transition de \_ type \_ principal de la chronologie**</span><span class="sxs-lookup"><span data-stu-id="e15b1-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TIMELINE\_MAJOR\_TYPE\_TRANSITION**</span></span>
</dt> <dd>

<span data-ttu-id="e15b1-119">Objet de transition.</span><span class="sxs-lookup"><span data-stu-id="e15b1-119">Transition object.</span></span> <span data-ttu-id="e15b1-120">Définit une transition entre des composites, des pistes ou des sources.</span><span class="sxs-lookup"><span data-stu-id="e15b1-120">Defines a transition between composites, tracks, or sources.</span></span>

</dd> <dt>

<span data-ttu-id="e15b1-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_effet de \_ type \_ principal de la chronologie**</span><span class="sxs-lookup"><span data-stu-id="e15b1-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**TIMELINE\_MAJOR\_TYPE\_EFFECT**</span></span>
</dt> <dd>

<span data-ttu-id="e15b1-122">Objet Effect.</span><span class="sxs-lookup"><span data-stu-id="e15b1-122">Effect object.</span></span> <span data-ttu-id="e15b1-123">Définit un effet d’entrée unique à appliquer à un objet composite, Track ou source.</span><span class="sxs-lookup"><span data-stu-id="e15b1-123">Defines a single-input effect to be applied to a composite, track, or source object.</span></span>

</dd> <dt>

<span data-ttu-id="e15b1-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**\_groupe de \_ types \_ principaux de la chronologie**</span><span class="sxs-lookup"><span data-stu-id="e15b1-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**TIMELINE\_MAJOR\_TYPE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="e15b1-125">Objet Group.</span><span class="sxs-lookup"><span data-stu-id="e15b1-125">Group object.</span></span> <span data-ttu-id="e15b1-126">Contient une ou plusieurs pistes d’un type donné.</span><span class="sxs-lookup"><span data-stu-id="e15b1-126">Contains one or more tracks of a given type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e15b1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e15b1-127">Requirements</span></span>



| <span data-ttu-id="e15b1-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e15b1-128">Requirement</span></span> | <span data-ttu-id="e15b1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e15b1-129">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e15b1-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="e15b1-130">Header</span></span><br/> | <dl> <span data-ttu-id="e15b1-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e15b1-131"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e15b1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e15b1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e15b1-133">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="e15b1-133">**IAMTimeline**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="e15b1-134">**IAMTimelineComp::GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="e15b1-134">**IAMTimelineComp::GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[<span data-ttu-id="e15b1-135">**IAMTimelineObj::GetTimelineType**</span><span class="sxs-lookup"><span data-stu-id="e15b1-135">**IAMTimelineObj::GetTimelineType**</span></span>](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




