---
title: Énumération MPRESOLVED_REASON (MpClient. h)
description: Raisons possibles d’une défaillance de correction en cours de résolution.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON énumération des fonctionnalités d’environnement Windows héritées
- PMPRESOLVED_REASON des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033025"
---
# <a name="mpresolved_reason-enumeration"></a><span data-ttu-id="0f49b-105">MPRESOLVED \_ Reason, énumération</span><span class="sxs-lookup"><span data-stu-id="0f49b-105">MPRESOLVED\_REASON enumeration</span></span>

<span data-ttu-id="0f49b-106">Raisons possibles d’une défaillance de correction en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="0f49b-106">Possible reasons for a remediation failure being resolved.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f49b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f49b-107">Syntax</span></span>


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a><span data-ttu-id="0f49b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="0f49b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0f49b-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**\_raison MPRESOLVED \_ inconnue**</span><span class="sxs-lookup"><span data-stu-id="0f49b-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MPRESOLVED\_REASON\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="0f49b-110">Dans un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0f49b-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="0f49b-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**\_ \_ analyse complète de la raison MPRESOLVED \_**</span><span class="sxs-lookup"><span data-stu-id="0f49b-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED\_REASON\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="0f49b-112">Une analyse complète a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="0f49b-112">A full scan was performed.</span></span>

</dd> <dt>

<span data-ttu-id="0f49b-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**la \_ raison MPRESOLVED \_ a expiré \_**</span><span class="sxs-lookup"><span data-stu-id="0f49b-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**MPRESOLVED\_REASON\_TIMED\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="0f49b-114">Suffisamment de temps s’est écoulé.</span><span class="sxs-lookup"><span data-stu-id="0f49b-114">Enough time has passed.</span></span> <span data-ttu-id="0f49b-115">La valeur par défaut est d’une semaine.</span><span class="sxs-lookup"><span data-stu-id="0f49b-115">The default is one week.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f49b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f49b-116">Requirements</span></span>



| <span data-ttu-id="0f49b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f49b-117">Requirement</span></span> | <span data-ttu-id="0f49b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f49b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f49b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f49b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f49b-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f49b-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0f49b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f49b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f49b-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f49b-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f49b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f49b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f49b-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f49b-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





