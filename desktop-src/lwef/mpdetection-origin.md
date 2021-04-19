---
title: Énumération MPDETECTION_ORIGIN (MpClient. h)
description: Origine de la détection.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN énumération des fonctionnalités d’environnement Windows héritées
- PMPDETECTION_ORIGIN des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106529075"
---
# <a name="mpdetection_origin-enumeration"></a><span data-ttu-id="ae431-105">\_Énumération d’origine MPDETECTION</span><span class="sxs-lookup"><span data-stu-id="ae431-105">MPDETECTION\_ORIGIN enumeration</span></span>

<span data-ttu-id="ae431-106">Origine de la détection.</span><span class="sxs-lookup"><span data-stu-id="ae431-106">Detection origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae431-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae431-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a><span data-ttu-id="ae431-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="ae431-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ae431-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION \_ origine \_ inconnue**</span><span class="sxs-lookup"><span data-stu-id="ae431-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION\_ORIGIN\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ae431-110">Origine de la menace détectée inconnue.</span><span class="sxs-lookup"><span data-stu-id="ae431-110">Threat detected origin unknown.</span></span>

</dd> <dt>

<span data-ttu-id="ae431-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**\_ \_ machine locale d’origine MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="ae431-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MPDETECTION\_ORIGIN\_LOCAL\_MACHINE**</span></span>
</dt> <dd>

<span data-ttu-id="ae431-112">Menace détectée sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="ae431-112">Threat detected on local machine.</span></span>

</dd> <dt>

<span data-ttu-id="ae431-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ origine \_ NETWORKSHARE**</span><span class="sxs-lookup"><span data-stu-id="ae431-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION\_ORIGIN\_NETWORKSHARE**</span></span>
</dt> <dd>

<span data-ttu-id="ae431-114">Menace détectée sur le partage réseau.</span><span class="sxs-lookup"><span data-stu-id="ae431-114">Threat detected on network share.</span></span>

</dd> <dt>

<span data-ttu-id="ae431-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**\_Internet MPDETECTION Origin \_**</span><span class="sxs-lookup"><span data-stu-id="ae431-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION\_ORIGIN\_INTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="ae431-116">Menace détectée sur Internet.</span><span class="sxs-lookup"><span data-stu-id="ae431-116">Threat detected on internet.</span></span>

</dd> <dt>

<span data-ttu-id="ae431-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION \_ origine \_ sortante**</span><span class="sxs-lookup"><span data-stu-id="ae431-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION\_ORIGIN\_OUTBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="ae431-118">Menace détectée sur une connexion sortante.</span><span class="sxs-lookup"><span data-stu-id="ae431-118">Threat detected on an outbound connection.</span></span>

</dd> <dt>

<span data-ttu-id="ae431-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION \_ origine \_ entrante**</span><span class="sxs-lookup"><span data-stu-id="ae431-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION\_ORIGIN\_INBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="ae431-120">Menace détectée sur une connexion entrante.</span><span class="sxs-lookup"><span data-stu-id="ae431-120">Threat detected on an inbound connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae431-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae431-121">Requirements</span></span>



| <span data-ttu-id="ae431-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae431-122">Requirement</span></span> | <span data-ttu-id="ae431-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae431-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae431-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae431-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ae431-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae431-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ae431-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae431-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ae431-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae431-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae431-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae431-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae431-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae431-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





