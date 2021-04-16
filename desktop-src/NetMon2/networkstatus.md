---
description: La structure NETWORKSTATUS décrit l’état actuel du NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: NETWORKSTATUS, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530226"
---
# <a name="networkstatus-structure"></a><span data-ttu-id="58295-103">NETWORKSTATUS, structure</span><span class="sxs-lookup"><span data-stu-id="58295-103">NETWORKSTATUS structure</span></span>

<span data-ttu-id="58295-104">La structure **NETWORKSTATUS** décrit l’état actuel du NPP.</span><span class="sxs-lookup"><span data-stu-id="58295-104">The **NETWORKSTATUS** structure describes the current status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="58295-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58295-105">Syntax</span></span>


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a><span data-ttu-id="58295-106">Membres</span><span class="sxs-lookup"><span data-stu-id="58295-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="58295-107">**State**</span><span class="sxs-lookup"><span data-stu-id="58295-107">**State**</span></span>
</dt> <dd>

<span data-ttu-id="58295-108">Indique l’état actuel du NPP.</span><span class="sxs-lookup"><span data-stu-id="58295-108">Indicates the current state of the NPP.</span></span>



| <span data-ttu-id="58295-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="58295-109">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="58295-110">Signification</span><span class="sxs-lookup"><span data-stu-id="58295-110">Meaning</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <span data-ttu-id="58295-111"><dt>**NETWORKSTATUS \_ état \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="58295-111"><dt>**NETWORKSTATUS\_STATE\_VOID**</dt></span></span> </dl>                | <span data-ttu-id="58295-112">Le NPP n’est pas connecté ou est connecté et la capture n’est pas démarrée.</span><span class="sxs-lookup"><span data-stu-id="58295-112">The NPP is not connected, or it is connected and the capture is not started.</span></span><br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <span data-ttu-id="58295-113"><dt>**capture de l' \_ État NETWORKSTATUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58295-113"><dt>**NETWORKSTATUS\_STATE\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="58295-114">Le NPP capture des données.</span><span class="sxs-lookup"><span data-stu-id="58295-114">The NPP is capturing data.</span></span><br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <span data-ttu-id="58295-115"><dt>**État de NETWORKSTATUS \_ \_ suspendu**</dt></span><span class="sxs-lookup"><span data-stu-id="58295-115"><dt>**NETWORKSTATUS\_STATE\_PAUSED**</dt></span></span> </dl>          | <span data-ttu-id="58295-116">Le NPP s’est interrompu lors de la capture des données.</span><span class="sxs-lookup"><span data-stu-id="58295-116">The NPP has paused while capturing data.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="58295-117">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="58295-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="58295-118">Indicateurs qui décrivent l’état actuel du NPP.</span><span class="sxs-lookup"><span data-stu-id="58295-118">Flags that describe the current state of the NPP.</span></span>



| <span data-ttu-id="58295-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="58295-119">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="58295-120">Signification</span><span class="sxs-lookup"><span data-stu-id="58295-120">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <span data-ttu-id="58295-121"><dt>**\_déclencheur d’indicateurs NETWORKSTATUS \_ \_ en attente**</dt></span><span class="sxs-lookup"><span data-stu-id="58295-121"><dt>**NETWORKSTATUS\_FLAGS\_TRIGGER\_PENDING**</dt></span></span> </dl> | <span data-ttu-id="58295-122">Il existe un déclencheur en attente pour le NPP.</span><span class="sxs-lookup"><span data-stu-id="58295-122">There is a trigger pending for the NPP.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58295-123">Notes</span><span class="sxs-lookup"><span data-stu-id="58295-123">Remarks</span></span>

<span data-ttu-id="58295-124">Lors de l’utilisation de cette structure, vous devez allouer la mémoire pour la structure avant de pouvoir l’utiliser et libérer la mémoire lorsque la structure n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="58295-124">When using this structure, you must allocate the memory for the structure before it can be used and free the memory when the structure is no longer needed.</span></span>

<span data-ttu-id="58295-125">La liste Voir aussi en bas de cette rubrique répertorie toutes les méthodes qui utilisent cette structure.</span><span class="sxs-lookup"><span data-stu-id="58295-125">The See Also list at the bottom of this topic lists all the methods that use this structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="58295-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58295-126">Requirements</span></span>



| <span data-ttu-id="58295-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58295-127">Requirement</span></span> | <span data-ttu-id="58295-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="58295-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="58295-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58295-129">Minimum supported client</span></span><br/> | <span data-ttu-id="58295-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58295-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="58295-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58295-131">Minimum supported server</span></span><br/> | <span data-ttu-id="58295-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58295-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="58295-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="58295-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="58295-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="58295-134"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58295-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58295-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58295-136">IDelaydC :: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="58295-136">IDelaydC::QueryStatus</span></span>](idelaydc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="58295-137">IESP :: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="58295-137">IESP::QueryStatus</span></span>](iesp-querystatus.md)
</dt> <dt>

[<span data-ttu-id="58295-138">IRTC :: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="58295-138">IRTC::QueryStatus</span></span>](irtc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="58295-139">IStats :: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="58295-139">IStats::QueryStatus</span></span>](istats-querystatus.md)
</dt> </dl>

 

 




