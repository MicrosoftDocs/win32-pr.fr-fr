---
title: Structure CHANGE_LOG_HEADER
description: En-tête du journal des modifications.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- Restauration du système de la structure CHANGE_LOG_HEADER
- PCHANGE_LOG_HEADER de la restauration du système du pointeur de structure
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383995"
---
# <a name="change_log_header-structure"></a><span data-ttu-id="a31be-105">MODIFIER \_ la \_ structure d’en-tête de journal</span><span class="sxs-lookup"><span data-stu-id="a31be-105">CHANGE\_LOG\_HEADER structure</span></span>

<span data-ttu-id="a31be-106">\[Ces informations s’appliquent uniquement à Windows XP avec Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="a31be-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="a31be-107">En-tête du journal des modifications.</span><span class="sxs-lookup"><span data-stu-id="a31be-107">The change log header.</span></span>

## <a name="syntax"></a><span data-ttu-id="a31be-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a31be-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a><span data-ttu-id="a31be-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a31be-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="a31be-110">**RecordHeader**</span><span class="sxs-lookup"><span data-stu-id="a31be-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="a31be-111">Structure [**d' \_ en-tête d’enregistrement**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="a31be-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="a31be-112">Le membre **dwRecordType** doit être défini sur RecordTypeLogHeader (0).</span><span class="sxs-lookup"><span data-stu-id="a31be-112">The **dwRecordType** member should be set to RecordTypeLogHeader (0).</span></span> <span data-ttu-id="a31be-113">Le membre **dwRecordSize** doit tenir compte de tous les membres, ainsi que de la valeur **DWORD** supplémentaire qui suit cet en-tête.</span><span class="sxs-lookup"><span data-stu-id="a31be-113">The **dwRecordSize** member should account for all the members, plus the extra **DWORD** value that follows this header.</span></span> <span data-ttu-id="a31be-114">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a31be-114">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a31be-115">**dwMagicNum**</span><span class="sxs-lookup"><span data-stu-id="a31be-115">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="a31be-116">Ce membre doit être défini sur 0xabcdef12.</span><span class="sxs-lookup"><span data-stu-id="a31be-116">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="a31be-117">**dwLogVersion**</span><span class="sxs-lookup"><span data-stu-id="a31be-117">**dwLogVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a31be-118">Ce membre doit être défini sur 2.</span><span class="sxs-lookup"><span data-stu-id="a31be-118">This member should be set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="a31be-119">**DataHeader**</span><span class="sxs-lookup"><span data-stu-id="a31be-119">**DataHeader**</span></span>
</dt> <dd>

<span data-ttu-id="a31be-120">Structure [**d' \_ en-tête d’enregistrement**](record-header.md) .</span><span class="sxs-lookup"><span data-stu-id="a31be-120">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="a31be-121">Le membre **dwRecordType** doit être défini sur **RecordTypeVolumePath** (2).</span><span class="sxs-lookup"><span data-stu-id="a31be-121">The **dwRecordType** member should be set to **RecordTypeVolumePath** (2).</span></span>

</dd> <dt>

<span data-ttu-id="a31be-122">**byteData**</span><span class="sxs-lookup"><span data-stu-id="a31be-122">**byteData**</span></span>
</dt> <dd>

<span data-ttu-id="a31be-123">Début d’une chaîne terminée par le caractère null qui spécifie le chemin d’accès du volume.</span><span class="sxs-lookup"><span data-stu-id="a31be-123">The start of a null-terminated string that specifies the volume path.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a31be-124">Notes</span><span class="sxs-lookup"><span data-stu-id="a31be-124">Remarks</span></span>

<span data-ttu-id="a31be-125">Cet en-tête est suivi d’une valeur **DWORD** qui doit être identique à la valeur du membre **dwRecordSize** de **RecordHeader**.</span><span class="sxs-lookup"><span data-stu-id="a31be-125">This header is followed by a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a31be-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a31be-126">Requirements</span></span>



| <span data-ttu-id="a31be-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a31be-127">Requirement</span></span> | <span data-ttu-id="a31be-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a31be-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a31be-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a31be-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a31be-130">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a31be-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a31be-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a31be-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a31be-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a31be-132">None supported</span></span><br/>                            |
| <span data-ttu-id="a31be-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a31be-133">End of client support</span></span><br/>    | <span data-ttu-id="a31be-134">Windows XP SP2</span><span class="sxs-lookup"><span data-stu-id="a31be-134">Windows XP with SP2</span></span><br/>                       |



 

 





