---
title: Énumération MPCALLBACK_TYPE (MpClient. h)
description: Types de rappel possibles.
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- MPCALLBACK_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMPCALLBACK_TYPE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3fd310f3733d36dd92ace1c7a5286bcf73a75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464911"
---
# <a name="mpcallback_type-enumeration"></a><span data-ttu-id="79204-105">\_Énumération de type MPCALLBACK</span><span class="sxs-lookup"><span data-stu-id="79204-105">MPCALLBACK\_TYPE enumeration</span></span>

<span data-ttu-id="79204-106">Types de rappel possibles.</span><span class="sxs-lookup"><span data-stu-id="79204-106">Possible callback types.</span></span>

## <a name="syntax"></a><span data-ttu-id="79204-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79204-107">Syntax</span></span>


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="79204-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="79204-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="79204-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="79204-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**État de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="79204-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**MPCALLBACK\_STATUS**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**\_menace MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="79204-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**MPCALLBACK\_THREAT**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**\_analyse MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="79204-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**MPCALLBACK\_SCAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK \_ nettoyer**</span><span class="sxs-lookup"><span data-stu-id="79204-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**prévérification MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="79204-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**MPCALLBACK\_PRECHECK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK \_ SIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="79204-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK\_SIGUPDATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**\_exemple MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="79204-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**MPCALLBACK\_SAMPLE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK \_ réservé**</span><span class="sxs-lookup"><span data-stu-id="79204-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK\_RESERVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**\_notification de configuration MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="79204-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**MPCALLBACK\_CONFIGURATION\_NOTIFICATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK \_ FASTPATH**</span><span class="sxs-lookup"><span data-stu-id="79204-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK\_FASTPATH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**\_expiration du produit MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="79204-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**MPCALLBACK\_PRODUCT\_EXPIRATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK \_ NIS \_ privé**</span><span class="sxs-lookup"><span data-stu-id="79204-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK\_NIS\_PRIVATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**\_intégrité MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="79204-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**MPCALLBACK\_HEALTH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK \_ ENDOFLIFE**</span><span class="sxs-lookup"><span data-stu-id="79204-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK\_ENDOFLIFE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK \_ MALWARETOAST**</span><span class="sxs-lookup"><span data-stu-id="79204-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK\_MALWARETOAST**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79204-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="79204-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK\_MAXVALUE**</span></span>
<span data-ttu-id="79204-126"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="79204-126"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="79204-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79204-127">Requirements</span></span>



| <span data-ttu-id="79204-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79204-128">Requirement</span></span> | <span data-ttu-id="79204-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="79204-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79204-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79204-130">Minimum supported client</span></span><br/> | <span data-ttu-id="79204-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79204-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="79204-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79204-132">Minimum supported server</span></span><br/> | <span data-ttu-id="79204-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79204-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79204-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="79204-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="79204-135"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="79204-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





