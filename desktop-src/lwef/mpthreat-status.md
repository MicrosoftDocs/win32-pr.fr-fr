---
title: Énumération MPTHREAT_STATUS (MpClient. h)
description: État possible de la menace.
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- MPTHREAT_STATUS énumération des fonctionnalités d’environnement Windows héritées
- PMPTHREAT_STATUS des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPTHREAT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978a152d6f14d7b3577ece0a2e8bd5a8ba741a3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510314"
---
# <a name="mpthreat_status-enumeration"></a><span data-ttu-id="6d895-105">\_Énumération de l’État MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="6d895-105">MPTHREAT\_STATUS enumeration</span></span>

<span data-ttu-id="6d895-106">État possible de la menace.</span><span class="sxs-lookup"><span data-stu-id="6d895-106">Possible threat status.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d895-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d895-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_STATUS { 
  MP_THREAT_STATUS_UNKNOWN            = 0,
  MP_THREAT_STATUS_DETECTED           = 1,
  MP_THREAT_STATUS_CLEANED            = 2,
  MP_THREAT_STATUS_QUARANTINED        = 3,
  MP_THREAT_STATUS_REMOVED            = 4,
  MP_THREAT_STATUS_ALLOWED            = 5,
  MP_THREAT_STATUS_BLOCKED            = 6,
  MP_THREAT_STATUS_CLEAN_FAILED       = 102,
  MP_THREAT_STATUS_QUARANTINE_FAILED  = 103,
  MP_THREAT_STATUS_REMOVE_FAILED      = 104,
  MP_THREAT_STATUS_ALLOW_FAILED       = 105,
  MP_THREAT_STATUS_ABANDONED          = 106,
  MP_THREAT_STATUS_BLOCK_FAILED       = 107
} MPTHREAT_STATUS, *PMPTHREAT_STATUS;
```



## <a name="constants"></a><span data-ttu-id="6d895-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6d895-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6d895-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**État de la menace de Pack d’e \_ \_ \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="6d895-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP\_THREAT\_STATUS\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**État de la \_ menace MP \_ \_ détecté**</span><span class="sxs-lookup"><span data-stu-id="6d895-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**MP\_THREAT\_STATUS\_DETECTED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**\_État des menaces MP \_ \_ nettoyé**</span><span class="sxs-lookup"><span data-stu-id="6d895-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**MP\_THREAT\_STATUS\_CLEANED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**État des menaces de MP en \_ \_ \_ quarantaine**</span><span class="sxs-lookup"><span data-stu-id="6d895-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**MP\_THREAT\_STATUS\_QUARANTINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**\_État des menaces MP \_ \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="6d895-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**MP\_THREAT\_STATUS\_REMOVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**\_État des menaces MP \_ \_ autorisé**</span><span class="sxs-lookup"><span data-stu-id="6d895-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**MP\_THREAT\_STATUS\_ALLOWED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**État de la menace du pack d’accès \_ \_ \_ bloqué**</span><span class="sxs-lookup"><span data-stu-id="6d895-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP\_THREAT\_STATUS\_BLOCKED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**échec du nettoyage de l' \_ État des menaces MP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d895-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**MP\_THREAT\_STATUS\_CLEAN\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**échec de la mise en quarantaine de l' \_ État des menaces MP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d895-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**MP\_THREAT\_STATUS\_QUARANTINE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**échec de la suppression de l' \_ État des menaces MP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d895-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**MP\_THREAT\_STATUS\_REMOVE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**échec de l’état de la \_ menace MP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d895-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**MP\_THREAT\_STATUS\_ALLOW\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**\_État des menaces MP \_ \_ abandonné**</span><span class="sxs-lookup"><span data-stu-id="6d895-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**MP\_THREAT\_STATUS\_ABANDONED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6d895-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**\_échec du \_ bloc d’état des menaces MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d895-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**MP\_THREAT\_STATUS\_BLOCK\_FAILED**</span></span>
<span data-ttu-id="6d895-122"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6d895-122"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6d895-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d895-123">Requirements</span></span>



| <span data-ttu-id="6d895-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d895-124">Requirement</span></span> | <span data-ttu-id="6d895-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d895-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d895-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d895-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6d895-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d895-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6d895-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d895-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6d895-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d895-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d895-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d895-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d895-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d895-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





