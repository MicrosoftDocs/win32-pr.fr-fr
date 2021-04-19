---
description: Obsolète. Représente un instant, généralement exprimé sous la forme d’une date et d’une heure de jour et d’un calendrier correspondant.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: CALDATETIME, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524747"
---
# <a name="caldatetime-structure"></a><span data-ttu-id="7696b-104">CALDATETIME, structure</span><span class="sxs-lookup"><span data-stu-id="7696b-104">CALDATETIME structure</span></span>

<span data-ttu-id="7696b-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7696b-105">Deprecated.</span></span> <span data-ttu-id="7696b-106">Représente un instant, généralement exprimé sous la forme d’une date et d’une heure de jour et d’un calendrier correspondant.</span><span class="sxs-lookup"><span data-stu-id="7696b-106">Represents an instant in time, typically expressed as a date and time of day and a corresponding calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="7696b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7696b-107">Syntax</span></span>


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a><span data-ttu-id="7696b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7696b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7696b-109">**CalId**</span><span class="sxs-lookup"><span data-stu-id="7696b-109">**CalId**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-110">[Identificateur de calendrier](calendar-identifiers.md) pour l’instant dans le temps.</span><span class="sxs-lookup"><span data-stu-id="7696b-110">The [calendar identifier](calendar-identifiers.md) for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="7696b-111">**Européen**</span><span class="sxs-lookup"><span data-stu-id="7696b-111">**Era**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-112">Informations sur l’ère pour l’instant dans le temps.</span><span class="sxs-lookup"><span data-stu-id="7696b-112">The era information for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="7696b-113">**Year**</span><span class="sxs-lookup"><span data-stu-id="7696b-113">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-114">Année pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="7696b-114">The year for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="7696b-115">**Chronique**</span><span class="sxs-lookup"><span data-stu-id="7696b-115">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-116">Mois pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="7696b-116">The month for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="7696b-117">**Jour**</span><span class="sxs-lookup"><span data-stu-id="7696b-117">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-118">Jour de l’instant dans le temps.</span><span class="sxs-lookup"><span data-stu-id="7696b-118">The day for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="7696b-119">**DayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="7696b-119">**DayOfWeek**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-120">Jour de la semaine pour l’instant dans le temps.</span><span class="sxs-lookup"><span data-stu-id="7696b-120">The day of the week for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="7696b-121">**Plages**</span><span class="sxs-lookup"><span data-stu-id="7696b-121">**Hour**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-122">Heure de l’instant dans le temps.</span><span class="sxs-lookup"><span data-stu-id="7696b-122">The hour for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="7696b-123">**Dernières**</span><span class="sxs-lookup"><span data-stu-id="7696b-123">**Minute**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-124">Minute pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="7696b-124">The minute for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="7696b-125">**Tache**</span><span class="sxs-lookup"><span data-stu-id="7696b-125">**Second**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-126">Seconde pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="7696b-126">The second for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="7696b-127">**Graduations**</span><span class="sxs-lookup"><span data-stu-id="7696b-127">**Tick**</span></span>
</dt> <dd>

<span data-ttu-id="7696b-128">Cycle de l’instant dans le temps.</span><span class="sxs-lookup"><span data-stu-id="7696b-128">The tick for the instant in time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7696b-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7696b-129">Requirements</span></span>



| <span data-ttu-id="7696b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7696b-130">Requirement</span></span> | <span data-ttu-id="7696b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7696b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7696b-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7696b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7696b-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7696b-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7696b-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7696b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7696b-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7696b-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7696b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7696b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7696b-137">Structures de prise en charge linguistique nationale</span><span class="sxs-lookup"><span data-stu-id="7696b-137">National Language Support Structures</span></span>](national-language-support-structures.md)
</dt> </dl>

 

 




