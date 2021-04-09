---
description: Contient des informations sur l’inactivité du système.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: Structure SYSTEM_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951982"
---
# <a name="system_power_information-structure"></a><span data-ttu-id="c5d62-103">Structure des informations de gestion de l’alimentation du système \_ \_</span><span class="sxs-lookup"><span data-stu-id="c5d62-103">SYSTEM\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="c5d62-104">Contient des informations sur l’inactivité du système.</span><span class="sxs-lookup"><span data-stu-id="c5d62-104">Contains information about the idleness of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d62-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5d62-105">Syntax</span></span>


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="c5d62-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c5d62-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5d62-107">**MaxIdlenessAllowed**</span><span class="sxs-lookup"><span data-stu-id="c5d62-107">**MaxIdlenessAllowed**</span></span>
</dt> <dd>

<span data-ttu-id="c5d62-108">Inactivité à laquelle le système est considéré comme inactif et dont le délai d’inactivité commence à compter, exprimé sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="c5d62-108">The idleness at which the system is considered idle and the idle time-out begins counting, expressed as a percentage.</span></span> <span data-ttu-id="c5d62-109">La suppression en dessous de ce nombre provoque l’annulation de la minuterie.</span><span class="sxs-lookup"><span data-stu-id="c5d62-109">Dropping below this number causes the timer to be canceled.</span></span>

</dd> <dt>

<span data-ttu-id="c5d62-110">**Inactivité**</span><span class="sxs-lookup"><span data-stu-id="c5d62-110">**Idleness**</span></span>
</dt> <dd>

<span data-ttu-id="c5d62-111">Niveau d’inactivité actuel, exprimé sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="c5d62-111">The current idle level, expressed as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="c5d62-112">**TimeRemaining**</span><span class="sxs-lookup"><span data-stu-id="c5d62-112">**TimeRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="c5d62-113">Temps restant dans le minuteur d’inactivité, en secondes.</span><span class="sxs-lookup"><span data-stu-id="c5d62-113">The time remaining in the idle timer, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c5d62-114">**CoolingMode**</span><span class="sxs-lookup"><span data-stu-id="c5d62-114">**CoolingMode**</span></span>
</dt> <dd>

<span data-ttu-id="c5d62-115">Mode de refroidissement du système actuel.</span><span class="sxs-lookup"><span data-stu-id="c5d62-115">The current system cooling mode.</span></span> <span data-ttu-id="c5d62-116">Ce membre doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5d62-116">This member must one of the following values.</span></span>



| <span data-ttu-id="c5d62-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d62-117">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="c5d62-118">Signification</span><span class="sxs-lookup"><span data-stu-id="c5d62-118">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <span data-ttu-id="c5d62-119"><dt>**Bon de commande \_ TZ \_ actif**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c5d62-119"><dt>**PO\_TZ\_ACTIVE**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="c5d62-120">Le système est actuellement en mode de refroidissement actif.</span><span class="sxs-lookup"><span data-stu-id="c5d62-120">The system is currently in Active cooling mode.</span></span><br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <span data-ttu-id="c5d62-121"><dt>**Bon de commande \_ TZ \_ - \_ mode 2 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c5d62-121"><dt>**PO\_TZ\_INVALID\_MODE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="c5d62-122">Le système ne prend pas en charge la limitation de l’UC ou aucune zone thermique n’est définie dans le système.</span><span class="sxs-lookup"><span data-stu-id="c5d62-122">The system does not support CPU throttling, or there is no thermal zone defined in the system.</span></span><br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <span data-ttu-id="c5d62-123"><dt>**Bon de commande \_ TZ \_ passif**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c5d62-123"><dt>**PO\_TZ\_PASSIVE**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="c5d62-124">Le système est actuellement en mode de refroidissement passif.</span><span class="sxs-lookup"><span data-stu-id="c5d62-124">The system is currently in Passive cooling mode.</span></span><br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5d62-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c5d62-125">Remarks</span></span>

<span data-ttu-id="c5d62-126">Notez que cette définition de structure a été omise par erreur dans Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="c5d62-126">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="c5d62-127">Cette erreur sera corrigée à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="c5d62-127">This error will be corrected in the future.</span></span> <span data-ttu-id="c5d62-128">En attendant, pour compiler votre application, incluez la définition de structure contenue dans cette rubrique dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="c5d62-128">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d62-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5d62-129">Requirements</span></span>



| <span data-ttu-id="c5d62-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5d62-130">Requirement</span></span> | <span data-ttu-id="c5d62-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d62-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5d62-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5d62-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d62-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5d62-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c5d62-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5d62-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d62-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5d62-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5d62-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5d62-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d62-137">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="c5d62-137">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




