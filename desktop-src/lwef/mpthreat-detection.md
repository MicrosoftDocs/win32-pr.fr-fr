---
title: Énumération MPTHREAT_DETECTION (MpClient. h)
description: Types de détection de menaces incorrects connus possibles.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION énumération des fonctionnalités d’environnement Windows héritées
- PMPTHREAT_DETECTION des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741005"
---
# <a name="mpthreat_detection-enumeration"></a><span data-ttu-id="55903-105">\_Énumération MPTHREAT Detection</span><span class="sxs-lookup"><span data-stu-id="55903-105">MPTHREAT\_DETECTION enumeration</span></span>

<span data-ttu-id="55903-106">Types de détection de menaces incorrects connus possibles.</span><span class="sxs-lookup"><span data-stu-id="55903-106">Possible known bad threat detection types.</span></span>

## <a name="syntax"></a><span data-ttu-id="55903-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55903-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a><span data-ttu-id="55903-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="55903-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="55903-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**\_ \_ béton détection des menaces MP \_**</span><span class="sxs-lookup"><span data-stu-id="55903-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP\_THREAT\_DETECTION\_CONCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="55903-110">Une menace a été détectée par le biais de signatures concrètes.</span><span class="sxs-lookup"><span data-stu-id="55903-110">Threat was detected via concrete signatures.</span></span>

</dd> <dt>

<span data-ttu-id="55903-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_heuristique de \_ détection des menaces MP \_**</span><span class="sxs-lookup"><span data-stu-id="55903-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP\_THREAT\_DETECTION\_HEURISTIC**</span></span>
</dt> <dd>

<span data-ttu-id="55903-112">Une menace a été détectée par le biais de l’heuristique.</span><span class="sxs-lookup"><span data-stu-id="55903-112">Threat was detected via heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="55903-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**\_générique de \_ détection des menaces MP \_**</span><span class="sxs-lookup"><span data-stu-id="55903-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP\_THREAT\_DETECTION\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="55903-114">Une menace a été détectée via des signatures génériques.</span><span class="sxs-lookup"><span data-stu-id="55903-114">Threat was detected via generic signatures.</span></span>

</dd> <dt>

<span data-ttu-id="55903-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**détection des menaces de MP \_ \_ \_ suspectes**</span><span class="sxs-lookup"><span data-stu-id="55903-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP\_THREAT\_DETECTION\_SUSPICIOUS**</span></span>
</dt> <dd>

<span data-ttu-id="55903-116">Une menace a été détectée via la surveillance du comportement.</span><span class="sxs-lookup"><span data-stu-id="55903-116">Threat was detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="55903-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**\_FASTPATH de \_ détection des menaces MP \_**</span><span class="sxs-lookup"><span data-stu-id="55903-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP\_THREAT\_DETECTION\_FASTPATH**</span></span>
</dt> <dd>

<span data-ttu-id="55903-118">Une menace a été détectée via FastPath.</span><span class="sxs-lookup"><span data-stu-id="55903-118">Threat was detected via fastpath.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55903-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55903-119">Requirements</span></span>



| <span data-ttu-id="55903-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55903-120">Requirement</span></span> | <span data-ttu-id="55903-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="55903-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55903-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55903-122">Minimum supported client</span></span><br/> | <span data-ttu-id="55903-123">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55903-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="55903-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55903-124">Minimum supported server</span></span><br/> | <span data-ttu-id="55903-125">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55903-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55903-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="55903-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="55903-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="55903-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





