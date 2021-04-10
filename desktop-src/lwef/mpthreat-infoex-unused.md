---
title: Structure MPTHREAT_INFOEX_UNUSED (MpClient. h)
description: Structure factice pour les menaces de type modification de non-comportement.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_INFOEX_UNUSED
- PMPTHREAT_INFOEX_UNUSED des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104536"
---
# <a name="mpthreat_infoex_unused-structure"></a><span data-ttu-id="170f2-105">MPTHREAT \_ INFOEX, \_ structure inutilisée</span><span class="sxs-lookup"><span data-stu-id="170f2-105">MPTHREAT\_INFOEX\_UNUSED structure</span></span>

<span data-ttu-id="170f2-106">Structure factice pour les menaces de type modification de non-comportement.</span><span class="sxs-lookup"><span data-stu-id="170f2-106">Dummy structure for non-behavior modification type threats.</span></span>

## <a name="syntax"></a><span data-ttu-id="170f2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="170f2-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="170f2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="170f2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="170f2-109">**dwNone**</span><span class="sxs-lookup"><span data-stu-id="170f2-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="170f2-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="170f2-110">Type: **DWORD**</span></span>

<span data-ttu-id="170f2-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="170f2-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="170f2-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="170f2-112">Requirements</span></span>



| <span data-ttu-id="170f2-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="170f2-113">Requirement</span></span> | <span data-ttu-id="170f2-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="170f2-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="170f2-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="170f2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="170f2-116">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="170f2-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="170f2-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="170f2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="170f2-118">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="170f2-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="170f2-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="170f2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="170f2-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="170f2-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





