---
description: Contient des informations sur un processeur.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Structure PROCESSOR_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319170"
---
# <a name="processor_power_information-structure"></a><span data-ttu-id="e976d-103">\_Structure des informations d’alimentation du processeur \_</span><span class="sxs-lookup"><span data-stu-id="e976d-103">PROCESSOR\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="e976d-104">Contient des informations sur un processeur.</span><span class="sxs-lookup"><span data-stu-id="e976d-104">Contains information about a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="e976d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e976d-105">Syntax</span></span>


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="e976d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e976d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e976d-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="e976d-107">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="e976d-108">Numéro du processeur système.</span><span class="sxs-lookup"><span data-stu-id="e976d-108">The system processor number.</span></span>

</dd> <dt>

<span data-ttu-id="e976d-109">**MaxMhz**</span><span class="sxs-lookup"><span data-stu-id="e976d-109">**MaxMhz**</span></span>
</dt> <dd>

<span data-ttu-id="e976d-110">Fréquence d’horloge maximale spécifiée du processeur système, en mégahertz.</span><span class="sxs-lookup"><span data-stu-id="e976d-110">The maximum specified clock frequency of the system processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="e976d-111">**CurrentMhz**</span><span class="sxs-lookup"><span data-stu-id="e976d-111">**CurrentMhz**</span></span>
</dt> <dd>

<span data-ttu-id="e976d-112">Fréquence d’horloge du processeur, en mégahertz.</span><span class="sxs-lookup"><span data-stu-id="e976d-112">The processor clock frequency, in megahertz.</span></span> <span data-ttu-id="e976d-113">Ce nombre correspond à la fréquence d’horloge du processeur spécifiée, multiplié par la limite actuelle du processeur.</span><span class="sxs-lookup"><span data-stu-id="e976d-113">This number is the maximum specified processor clock frequency multiplied by the current processor throttle.</span></span>

</dd> <dt>

<span data-ttu-id="e976d-114">**MhzLimit**</span><span class="sxs-lookup"><span data-stu-id="e976d-114">**MhzLimit**</span></span>
</dt> <dd>

<span data-ttu-id="e976d-115">Limite de fréquence d’horloge du processeur, en mégahertz.</span><span class="sxs-lookup"><span data-stu-id="e976d-115">The limit on the processor clock frequency, in megahertz.</span></span> <span data-ttu-id="e976d-116">Ce nombre correspond à la fréquence d’horloge du processeur spécifiée, multipliée par la limite actuelle de limitation thermique du processeur.</span><span class="sxs-lookup"><span data-stu-id="e976d-116">This number is the maximum specified processor clock frequency multiplied by the current processor thermal throttle limit.</span></span>

</dd> <dt>

<span data-ttu-id="e976d-117">**MaxIdleState**</span><span class="sxs-lookup"><span data-stu-id="e976d-117">**MaxIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="e976d-118">État d’inactivité maximal de ce processeur.</span><span class="sxs-lookup"><span data-stu-id="e976d-118">The maximum idle state of this processor.</span></span>

</dd> <dt>

<span data-ttu-id="e976d-119">**CurrentIdleState**</span><span class="sxs-lookup"><span data-stu-id="e976d-119">**CurrentIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="e976d-120">État d’inactivité actuel de ce processeur.</span><span class="sxs-lookup"><span data-stu-id="e976d-120">The current idle state of this processor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e976d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="e976d-121">Remarks</span></span>

<span data-ttu-id="e976d-122">Notez que cette définition de structure a été omise par erreur dans Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="e976d-122">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="e976d-123">Cette erreur sera corrigée à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="e976d-123">This error will be corrected in the future.</span></span> <span data-ttu-id="e976d-124">En attendant, pour compiler votre application, incluez la définition de structure contenue dans cette rubrique dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="e976d-124">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e976d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e976d-125">Requirements</span></span>



| <span data-ttu-id="e976d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e976d-126">Requirement</span></span> | <span data-ttu-id="e976d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e976d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e976d-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e976d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e976d-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e976d-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e976d-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e976d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e976d-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e976d-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e976d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e976d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e976d-133">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="e976d-133">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




