---
title: Énumération MP_HASH_TYPE (MpClient. h)
description: Types de hachage possibles.
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- MP_HASH_TYPE énumération des fonctionnalités d’environnement Windows héritées
- PMP_HASH_TYPE des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c36e709d165845b729673df4aaea1042a7ee49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466662"
---
# <a name="mp_hash_type-enumeration"></a><span data-ttu-id="fd1d2-105">\_Énumération de type de hachage MP \_</span><span class="sxs-lookup"><span data-stu-id="fd1d2-105">MP\_HASH\_TYPE enumeration</span></span>

<span data-ttu-id="fd1d2-106">Types de hachage possibles.</span><span class="sxs-lookup"><span data-stu-id="fd1d2-106">Possible hash types.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd1d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd1d2-107">Syntax</span></span>


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="fd1d2-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="fd1d2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd1d2-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**\_type de hachage MP \_ \_ None**</span><span class="sxs-lookup"><span data-stu-id="fd1d2-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**MP\_HASH\_TYPE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="fd1d2-110">Aucun hachage.</span><span class="sxs-lookup"><span data-stu-id="fd1d2-110">No hash.</span></span>

</dd> <dt>

<span data-ttu-id="fd1d2-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**\_Type de hachage MP \_ \_ CRC32**</span><span class="sxs-lookup"><span data-stu-id="fd1d2-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**MP\_HASH\_TYPE\_CRC32**</span></span>
</dt> <dd>

<span data-ttu-id="fd1d2-112">CRC32</span><span class="sxs-lookup"><span data-stu-id="fd1d2-112">CRC32</span></span>

</dd> <dt>

<span data-ttu-id="fd1d2-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**\_Type de hachage MP \_ \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="fd1d2-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**MP\_HASH\_TYPE\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="fd1d2-114">MD5</span><span class="sxs-lookup"><span data-stu-id="fd1d2-114">MD5</span></span>

</dd> <dt>

<span data-ttu-id="fd1d2-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**\_Type de hachage MP \_ \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="fd1d2-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**MP\_HASH\_TYPE\_SHA1**</span></span>
</dt> <dd>

<span data-ttu-id="fd1d2-116">SHA1</span><span class="sxs-lookup"><span data-stu-id="fd1d2-116">SHA1</span></span>

</dd> <dt>

<span data-ttu-id="fd1d2-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**\_Type de hachage MP \_ \_ SHA256**</span><span class="sxs-lookup"><span data-stu-id="fd1d2-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**MP\_HASH\_TYPE\_SHA256**</span></span>
</dt> <dd>

<span data-ttu-id="fd1d2-118">SHA 256</span><span class="sxs-lookup"><span data-stu-id="fd1d2-118">SHA 256</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd1d2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd1d2-119">Requirements</span></span>



| <span data-ttu-id="fd1d2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd1d2-120">Requirement</span></span> | <span data-ttu-id="fd1d2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd1d2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1d2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd1d2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1d2-123">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd1d2-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fd1d2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd1d2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1d2-125">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd1d2-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd1d2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd1d2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd1d2-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd1d2-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





