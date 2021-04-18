---
title: Énumération MPTHREAT_SEVERITY (MpClient. h)
description: Risque de gravité des menaces.
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- MPTHREAT_SEVERITY énumération des fonctionnalités d’environnement Windows héritées
- PMPTHREAT_SEVERITY des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPTHREAT_SEVERITY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eec7bff3b23a89ce8187798d8a69a9968cbc2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509522"
---
# <a name="mpthreat_severity-enumeration"></a><span data-ttu-id="0b96b-105">\_Énumération MPTHREAT Severity</span><span class="sxs-lookup"><span data-stu-id="0b96b-105">MPTHREAT\_SEVERITY enumeration</span></span>

<span data-ttu-id="0b96b-106">Risque de gravité des menaces.</span><span class="sxs-lookup"><span data-stu-id="0b96b-106">Possible threat severities.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b96b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b96b-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_SEVERITY { 
  MP_THREAT_SEVERITY_UNKNOWN   = 0,
  MP_THREAT_SEVERITY_LOW       = 1,
  MP_THREAT_SEVERITY_MODERATE  = 2,
  MP_THREAT_SEVERITY_HIGH      = 4,
  MP_THREAT_SEVERITY_SEVERE    = 5,
  MP_THREAT_SEVERITY_MAXVALUE  = 5
} MPTHREAT_SEVERITY, *PMPTHREAT_SEVERITY;
```



## <a name="constants"></a><span data-ttu-id="0b96b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="0b96b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0b96b-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**gravité de la menace de MP \_ \_ \_ inconnue**</span><span class="sxs-lookup"><span data-stu-id="0b96b-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**MP\_THREAT\_SEVERITY\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0b96b-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**gravité de menace de la MP \_ \_ \_ faible**</span><span class="sxs-lookup"><span data-stu-id="0b96b-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**MP\_THREAT\_SEVERITY\_LOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0b96b-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**gravité des menaces de MP \_ \_ \_ modéré**</span><span class="sxs-lookup"><span data-stu-id="0b96b-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**MP\_THREAT\_SEVERITY\_MODERATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0b96b-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**gravité des menaces de MP \_ \_ \_ élevé**</span><span class="sxs-lookup"><span data-stu-id="0b96b-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**MP\_THREAT\_SEVERITY\_HIGH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0b96b-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**gravité des menaces de la MP \_ \_ \_ critique**</span><span class="sxs-lookup"><span data-stu-id="0b96b-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**MP\_THREAT\_SEVERITY\_SEVERE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="0b96b-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**niveau de \_ gravité des menaces MP \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="0b96b-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**MP\_THREAT\_SEVERITY\_MAXVALUE**</span></span>
<span data-ttu-id="0b96b-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0b96b-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0b96b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b96b-116">Requirements</span></span>



| <span data-ttu-id="0b96b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b96b-117">Requirement</span></span> | <span data-ttu-id="0b96b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b96b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b96b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b96b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0b96b-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b96b-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0b96b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b96b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0b96b-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b96b-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b96b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b96b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b96b-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b96b-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





