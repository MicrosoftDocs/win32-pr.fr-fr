---
title: Structure MPSTATUS_DATAEX_UNUSED (MpClient. h)
description: Structure factice pour non-SRP.
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSTATUS_DATAEX_UNUSED
- PMPSTATUS_DATAEX_UNUSED des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSTATUS_DATAEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfcbc987a97a8cc47501a24e633c5da2d776a42d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106294"
---
# <a name="mpstatus_dataex_unused-structure"></a><span data-ttu-id="f0199-105">MPSTATUS \_ DATAEX, \_ structure inutilisée</span><span class="sxs-lookup"><span data-stu-id="f0199-105">MPSTATUS\_DATAEX\_UNUSED structure</span></span>

<span data-ttu-id="f0199-106">Structure factice pour non-SRP.</span><span class="sxs-lookup"><span data-stu-id="f0199-106">Dummy structure for non-SRP.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0199-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0199-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATAEX_UNUSED {
  DWORD dwNone;
} MPSTATUS_DATAEX_UNUSED, *PMPSTATUS_DATAEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="f0199-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f0199-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f0199-109">**dwNone**</span><span class="sxs-lookup"><span data-stu-id="f0199-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="f0199-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f0199-110">Type: **DWORD**</span></span>

<span data-ttu-id="f0199-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f0199-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f0199-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0199-112">Requirements</span></span>



| <span data-ttu-id="f0199-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0199-113">Requirement</span></span> | <span data-ttu-id="f0199-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0199-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0199-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0199-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f0199-116">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0199-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f0199-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0199-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f0199-118">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0199-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0199-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0199-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0199-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0199-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





