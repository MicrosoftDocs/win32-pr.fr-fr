---
title: Énumération MP_SIGNATURE_TYPE (MpClient. h)
description: Types de signature possibles.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMP_SIGNATURE_TYPE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465166"
---
# <a name="mp_signature_type-enumeration"></a><span data-ttu-id="107d1-105">\_Énumération du type de signature MP \_</span><span class="sxs-lookup"><span data-stu-id="107d1-105">MP\_SIGNATURE\_TYPE enumeration</span></span>

<span data-ttu-id="107d1-106">Types de signature possibles.</span><span class="sxs-lookup"><span data-stu-id="107d1-106">Possible signature types.</span></span>

## <a name="syntax"></a><span data-ttu-id="107d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="107d1-107">Syntax</span></span>


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="107d1-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="107d1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="107d1-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**\_ \_ logiciel anti-programme malveillant de signature MP**</span><span class="sxs-lookup"><span data-stu-id="107d1-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP\_SIGNATURE\_ANTIMALWARE**</span></span>
</dt> <dd>

<span data-ttu-id="107d1-110">Signatures antivirus et antispyware.</span><span class="sxs-lookup"><span data-stu-id="107d1-110">Both antivirus and antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="107d1-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**SIGNATURE du pack d' \_ \_ antivirus**</span><span class="sxs-lookup"><span data-stu-id="107d1-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP\_SIGNATURE\_ANTIVIRUS**</span></span>
</dt> <dd>

<span data-ttu-id="107d1-112">Signatures d’antivirus uniquement.</span><span class="sxs-lookup"><span data-stu-id="107d1-112">Only antivirus signatures.</span></span>

</dd> <dt>

<span data-ttu-id="107d1-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**antispyware de \_ signature MP \_**</span><span class="sxs-lookup"><span data-stu-id="107d1-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP\_SIGNATURE\_ANTISPYWARE**</span></span>
</dt> <dd>

<span data-ttu-id="107d1-114">Uniquement les signatures anti-espion.</span><span class="sxs-lookup"><span data-stu-id="107d1-114">Only antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="107d1-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**\_signature MP \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="107d1-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP\_SIGNATURE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="107d1-116">Signatures NIS.</span><span class="sxs-lookup"><span data-stu-id="107d1-116">NIS signatures.</span></span>

</dd> <dt>

<span data-ttu-id="107d1-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**\_types de signature MP \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="107d1-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MP\_SIGNATURE\_TYPES\_MAXVALUE**</span></span>
<span data-ttu-id="107d1-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="107d1-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="107d1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="107d1-119">Requirements</span></span>



| <span data-ttu-id="107d1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="107d1-120">Requirement</span></span> | <span data-ttu-id="107d1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="107d1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="107d1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="107d1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="107d1-123">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="107d1-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="107d1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="107d1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="107d1-125">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="107d1-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="107d1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="107d1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="107d1-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="107d1-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





