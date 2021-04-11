---
title: Énumération MPTHREAT_ACTION (MpClient. h)
description: Actions possibles sur les menaces.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- MPTHREAT_ACTION énumération des fonctionnalités d’environnement Windows héritées
- PMPTHREAT_ACTION des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0377517af590072b797a57c051ad062842ea9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103561"
---
# <a name="mpthreat_action-enumeration"></a><span data-ttu-id="f296f-105">\_Énumération d’action MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="f296f-105">MPTHREAT\_ACTION enumeration</span></span>

<span data-ttu-id="f296f-106">Actions possibles sur les menaces.</span><span class="sxs-lookup"><span data-stu-id="f296f-106">Possible threat actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f296f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f296f-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a><span data-ttu-id="f296f-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="f296f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f296f-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**\_action de menace MP \_ \_ inconnue**</span><span class="sxs-lookup"><span data-stu-id="f296f-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP\_THREAT\_ACTION\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f296f-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**ACTION de menace de point de gestion \_ \_ \_ nettoyée**</span><span class="sxs-lookup"><span data-stu-id="f296f-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP\_THREAT\_ACTION\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f296f-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**\_mise en \_ quarantaine des actions de menace MP \_**</span><span class="sxs-lookup"><span data-stu-id="f296f-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**MP\_THREAT\_ACTION\_QUARANTINE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f296f-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**suppression de l' \_ action de menace MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f296f-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP\_THREAT\_ACTION\_REMOVE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f296f-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**\_autorisation d' \_ action de menace MP \_**</span><span class="sxs-lookup"><span data-stu-id="f296f-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP\_THREAT\_ACTION\_ALLOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f296f-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**USERDEFINED d’action sur les \_ menaces MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f296f-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**MP\_THREAT\_ACTION\_USERDEFINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f296f-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**\_ \_ ACTION \_ NoAction sur les menaces MP**</span><span class="sxs-lookup"><span data-stu-id="f296f-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP\_THREAT\_ACTION\_NOACTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f296f-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**\_bloc d' \_ action de menace MP \_**</span><span class="sxs-lookup"><span data-stu-id="f296f-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP\_THREAT\_ACTION\_BLOCK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="f296f-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**\_ \_ \_ valeur maximale de l’action de menace MP \_**</span><span class="sxs-lookup"><span data-stu-id="f296f-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**MP\_THREAT\_ACTION\_MAX\_VALUE**</span></span>
<span data-ttu-id="f296f-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f296f-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f296f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f296f-119">Requirements</span></span>



| <span data-ttu-id="f296f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f296f-120">Requirement</span></span> | <span data-ttu-id="f296f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f296f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f296f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f296f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f296f-123">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f296f-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f296f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f296f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f296f-125">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f296f-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f296f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f296f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f296f-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f296f-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





