---
title: Structure MPTHREAT_INFOEX_NIS (MpClient. h)
description: Contient des informations spécifiques à NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_INFOEX_NIS
- PMPTHREAT_INFOEX_NIS des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032808"
---
# <a name="mpthreat_infoex_nis-structure"></a><span data-ttu-id="fe9b8-105">\_Structure MPTHREAT INFOEX \_ NIS</span><span class="sxs-lookup"><span data-stu-id="fe9b8-105">MPTHREAT\_INFOEX\_NIS structure</span></span>

<span data-ttu-id="fe9b8-106">Contient des informations spécifiques à NIS.</span><span class="sxs-lookup"><span data-stu-id="fe9b8-106">Contains NIS-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe9b8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe9b8-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a><span data-ttu-id="fe9b8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fe9b8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe9b8-109">**SourceIP**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-109">**SourceIP**</span></span>
</dt> <dd>

<span data-ttu-id="fe9b8-110">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="fe9b8-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="fe9b8-111">**DestinationIP**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-111">**DestinationIP**</span></span>
</dt> <dd>

<span data-ttu-id="fe9b8-112">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="fe9b8-112">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="fe9b8-113">**dwSourceport**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-113">**dwSourceport**</span></span>
</dt> <dd>

<span data-ttu-id="fe9b8-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-114">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="fe9b8-115">**dwDestinationport**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-115">**dwDestinationport**</span></span>
</dt> <dd>

<span data-ttu-id="fe9b8-116">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-116">Type: **DWORD**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="fe9b8-117">**Protocole**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-117">**Protocol**</span></span>
</dt> <dd>

<span data-ttu-id="fe9b8-118">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="fe9b8-118">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd></dd> <dt>

<span data-ttu-id="fe9b8-119">**Lien**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-119">**Link**</span></span>
</dt> <dd>

<span data-ttu-id="fe9b8-120">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="fe9b8-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

<span data-ttu-id="fe9b8-121"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fe9b8-121"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="fe9b8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe9b8-122">Requirements</span></span>



| <span data-ttu-id="fe9b8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe9b8-123">Requirement</span></span> | <span data-ttu-id="fe9b8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe9b8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9b8-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe9b8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fe9b8-126">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe9b8-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fe9b8-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe9b8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fe9b8-128">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe9b8-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe9b8-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe9b8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe9b8-130"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe9b8-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





