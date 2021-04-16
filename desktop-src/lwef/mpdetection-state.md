---
title: Énumération MPDETECTION_STATE (MpClient. h)
description: État de la menace actuellement détectée.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE énumération des fonctionnalités d’environnement Windows héritées
- PMPDETECTION_STATE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464906"
---
# <a name="mpdetection_state-enumeration"></a><span data-ttu-id="451d3-105">\_Énumération de l’État MPDETECTION</span><span class="sxs-lookup"><span data-stu-id="451d3-105">MPDETECTION\_STATE enumeration</span></span>

<span data-ttu-id="451d3-106">État de la menace actuellement détectée.</span><span class="sxs-lookup"><span data-stu-id="451d3-106">The state of the currently detected threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="451d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="451d3-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a><span data-ttu-id="451d3-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="451d3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="451d3-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**État de MPDETECTION \_ \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="451d3-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION\_STATE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="451d3-110">Dans un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="451d3-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="451d3-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**État de MPDETECTION \_ \_ actif**</span><span class="sxs-lookup"><span data-stu-id="451d3-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION\_STATE\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="451d3-112">Menace active.</span><span class="sxs-lookup"><span data-stu-id="451d3-112">Active threat.</span></span>

</dd> <dt>

<span data-ttu-id="451d3-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**État de MPDETECTION \_ \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="451d3-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="451d3-114">En attente de 24 heures jusqu’au déplacement jusqu’à la suppression.</span><span class="sxs-lookup"><span data-stu-id="451d3-114">Pending 24 hours to a move to cleared.</span></span>

</dd> <dt>

<span data-ttu-id="451d3-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**\_ \_ actions supplémentaires de l’État MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="451d3-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION\_STATE\_ADDITIONAL\_ACTIONS**</span></span>
</dt> <dd>

<span data-ttu-id="451d3-116">Actions supplémentaires requises.</span><span class="sxs-lookup"><span data-stu-id="451d3-116">Additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="451d3-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**échec de l’état de MPDETECTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="451d3-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION\_STATE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="451d3-118">Échec de la mise à jour non critique.</span><span class="sxs-lookup"><span data-stu-id="451d3-118">Non-critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="451d3-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**\_ \_ échec critique de l’État MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="451d3-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION\_STATE\_CRITICALLY\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="451d3-120">Échec de la correction critique.</span><span class="sxs-lookup"><span data-stu-id="451d3-120">Critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="451d3-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**\_État MPDETECTION \_ effacé**</span><span class="sxs-lookup"><span data-stu-id="451d3-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**MPDETECTION\_STATE\_CLEARED**</span></span>
</dt> <dd>

<span data-ttu-id="451d3-122">La menace n’apparaît pas dans la requête d’État, uniquement dans l’historique.</span><span class="sxs-lookup"><span data-stu-id="451d3-122">Threat does not show up in the state query, only in history.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="451d3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="451d3-123">Requirements</span></span>



| <span data-ttu-id="451d3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="451d3-124">Requirement</span></span> | <span data-ttu-id="451d3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="451d3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="451d3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="451d3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="451d3-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="451d3-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="451d3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="451d3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="451d3-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="451d3-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="451d3-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="451d3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="451d3-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="451d3-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





