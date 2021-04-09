---
title: Énumération MPEXECUTION_STATUS (MpClient. h)
description: État d’exécution de la menace possible.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS énumération des fonctionnalités d’environnement Windows héritées
- PMPEXECUTION_STATUS des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843369"
---
# <a name="mpexecution_status-enumeration"></a><span data-ttu-id="26645-105">\_Énumération de l’État MPEXECUTION</span><span class="sxs-lookup"><span data-stu-id="26645-105">MPEXECUTION\_STATUS enumeration</span></span>

<span data-ttu-id="26645-106">État d’exécution de la menace possible.</span><span class="sxs-lookup"><span data-stu-id="26645-106">Possible threat execution status.</span></span>

## <a name="syntax"></a><span data-ttu-id="26645-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26645-107">Syntax</span></span>


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a><span data-ttu-id="26645-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="26645-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="26645-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**État d’exécution du point de gestion \_ \_ \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="26645-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP\_EXECUTION\_STATUS\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="26645-110">L’état d’exécution n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="26645-110">Execution status is not known.</span></span>

</dd> <dt>

<span data-ttu-id="26645-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**État de l’exécution du point de gestion \_ \_ \_ bloqué**</span><span class="sxs-lookup"><span data-stu-id="26645-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP\_EXECUTION\_STATUS\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="26645-112">Blocage de l’exécution par mini-filtre.</span><span class="sxs-lookup"><span data-stu-id="26645-112">Blocked from execution by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="26645-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**État d’exécution du point de gestion \_ \_ \_ autorisé**</span><span class="sxs-lookup"><span data-stu-id="26645-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**MP\_EXECUTION\_STATUS\_ALLOWED**</span></span>
</dt> <dd>

<span data-ttu-id="26645-114">Autorisé à s’exécuter par mini-filtre.</span><span class="sxs-lookup"><span data-stu-id="26645-114">Allowed to execute by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="26645-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**\_État de l’exécution du pack d’exécution \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26645-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**MP\_EXECUTION\_STATUS\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="26645-116">La menace est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="26645-116">Threat is executing.</span></span>

</dd> <dt>

<span data-ttu-id="26645-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**État d’exécution du pack d' \_ exécution \_ \_ non \_ exécuté**</span><span class="sxs-lookup"><span data-stu-id="26645-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP\_EXECUTION\_STATUS\_NOT\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="26645-118">La menace n’est pas en cours d’exécution et n’est disponible qu’à partir du moteur pendant la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="26645-118">Threat is not executing, and is only available from the engine during remediation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26645-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26645-119">Requirements</span></span>



| <span data-ttu-id="26645-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26645-120">Requirement</span></span> | <span data-ttu-id="26645-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="26645-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26645-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26645-122">Minimum supported client</span></span><br/> | <span data-ttu-id="26645-123">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26645-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="26645-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26645-124">Minimum supported server</span></span><br/> | <span data-ttu-id="26645-125">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26645-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26645-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="26645-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="26645-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="26645-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





