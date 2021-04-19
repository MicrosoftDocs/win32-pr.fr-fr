---
description: L’énumération EXPERTSTATUSENUMERATION contient des valeurs d’État. Il est utilisé par le membre Status de la structure EXPERTSTATUS et le paramètre Status dans ExpertIndicateStatus.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: EXPERTSTATUSENUMERATION, énumération (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517447"
---
# <a name="expertstatusenumeration-enumeration"></a><span data-ttu-id="c069a-104">Énumération EXPERTSTATUSENUMERATION</span><span class="sxs-lookup"><span data-stu-id="c069a-104">EXPERTSTATUSENUMERATION enumeration</span></span>

<span data-ttu-id="c069a-105">L’énumération **EXPERTSTATUSENUMERATION** contient des valeurs d’État.</span><span class="sxs-lookup"><span data-stu-id="c069a-105">The **EXPERTSTATUSENUMERATION** enumeration contains status values.</span></span> <span data-ttu-id="c069a-106">Il est utilisé par le membre **Status** de la structure [EXPERTSTATUS](expertstatus.md) et le paramètre *Status* dans [ExpertIndicateStatus](expertindicatestatus.md).</span><span class="sxs-lookup"><span data-stu-id="c069a-106">It is used by the **Status** member of [EXPERTSTATUS](expertstatus.md) structure and the *Status* parameter in [ExpertIndicateStatus](expertindicatestatus.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c069a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c069a-107">Syntax</span></span>


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a><span data-ttu-id="c069a-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="c069a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c069a-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="c069a-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="c069a-110">L’expert n’a jamais démarré.</span><span class="sxs-lookup"><span data-stu-id="c069a-110">The expert never started.</span></span>

</dd> <dt>

<span data-ttu-id="c069a-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**début de EXPERTSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="c069a-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS\_STARTING**</span></span>
</dt> <dd>

<span data-ttu-id="c069a-112">L’expert démarre.</span><span class="sxs-lookup"><span data-stu-id="c069a-112">The expert is starting.</span></span>

</dd> <dt>

<span data-ttu-id="c069a-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="c069a-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="c069a-114">L’expert s’exécute normalement.</span><span class="sxs-lookup"><span data-stu-id="c069a-114">The expert is running normally.</span></span>

</dd> <dt>

<span data-ttu-id="c069a-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**\_problème EXPERTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="c069a-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**EXPERTSTATUS\_PROBLEM**</span></span>
</dt> <dd>

<span data-ttu-id="c069a-116">Un problème spécifié dans sous- *État* A arrêté l’expert.</span><span class="sxs-lookup"><span data-stu-id="c069a-116">A problem specified in *SubStatus* stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="c069a-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS \_ abandonné**</span><span class="sxs-lookup"><span data-stu-id="c069a-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="c069a-118">Moniteur réseau arrêté l’expert.</span><span class="sxs-lookup"><span data-stu-id="c069a-118">Network Monitor stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="c069a-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="c069a-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS\_DONE**</span></span>
</dt> <dd>

<span data-ttu-id="c069a-120">L’expert s’est terminé avec succès.</span><span class="sxs-lookup"><span data-stu-id="c069a-120">The expert finished successfully.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c069a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c069a-121">Requirements</span></span>



| <span data-ttu-id="c069a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c069a-122">Requirement</span></span> | <span data-ttu-id="c069a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c069a-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c069a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c069a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c069a-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c069a-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c069a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c069a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c069a-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c069a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c069a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c069a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c069a-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c069a-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




