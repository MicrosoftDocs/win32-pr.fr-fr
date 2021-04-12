---
title: Énumération MPTHREAT_TYPE (MpClient. h)
description: Types de menaces possibles.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMPTHREAT_TYPE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed823b100c91f259252d7cad71e554099caf6a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384407"
---
# <a name="mpthreat_type-enumeration"></a><span data-ttu-id="f6e1a-105">\_Énumération de type MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="f6e1a-105">MPTHREAT\_TYPE enumeration</span></span>

<span data-ttu-id="f6e1a-106">Types de menaces possibles.</span><span class="sxs-lookup"><span data-stu-id="f6e1a-106">Possible threat types.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e1a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6e1a-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="f6e1a-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="f6e1a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f6e1a-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT \_ type \_ KNOWNBAD**</span><span class="sxs-lookup"><span data-stu-id="f6e1a-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT\_TYPE\_KNOWNBAD**</span></span>
</dt> <dd>

<span data-ttu-id="f6e1a-110">Menace connue connue détectée par le biais de la signature.</span><span class="sxs-lookup"><span data-stu-id="f6e1a-110">Known bad threat detected via signature.</span></span>

</dd> <dt>

<span data-ttu-id="f6e1a-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**\_comportement du type MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="f6e1a-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**MPTHREAT\_TYPE\_BEHAVIOR**</span></span>
</dt> <dd>

<span data-ttu-id="f6e1a-112">Menace suspecte détectée via la surveillance du comportement.</span><span class="sxs-lookup"><span data-stu-id="f6e1a-112">Suspicious threat detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="f6e1a-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**\_type MPTHREAT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="f6e1a-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**MPTHREAT\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="f6e1a-114">Menaces inconnues (non classifiées).</span><span class="sxs-lookup"><span data-stu-id="f6e1a-114">Unknown threats (unclassified).</span></span>

</dd> <dt>

<span data-ttu-id="f6e1a-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT \_ type \_ KNOWNGOOD**</span><span class="sxs-lookup"><span data-stu-id="f6e1a-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT\_TYPE\_KNOWNGOOD**</span></span>
</dt> <dd>

<span data-ttu-id="f6e1a-116">Bonne menace connue.</span><span class="sxs-lookup"><span data-stu-id="f6e1a-116">Known good threat.</span></span>

</dd> <dt>

<span data-ttu-id="f6e1a-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT \_ type \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="f6e1a-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT\_TYPE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="f6e1a-118">Détection des menaces NIS.</span><span class="sxs-lookup"><span data-stu-id="f6e1a-118">NIS threat detection.</span></span>

</dd> <dt>

<span data-ttu-id="f6e1a-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT \_ type \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="f6e1a-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="f6e1a-120">Valeur maximale possible.</span><span class="sxs-lookup"><span data-stu-id="f6e1a-120">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6e1a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6e1a-121">Requirements</span></span>



| <span data-ttu-id="f6e1a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6e1a-122">Requirement</span></span> | <span data-ttu-id="f6e1a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6e1a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e1a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6e1a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e1a-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6e1a-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f6e1a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6e1a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e1a-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6e1a-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6e1a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6e1a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6e1a-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6e1a-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





