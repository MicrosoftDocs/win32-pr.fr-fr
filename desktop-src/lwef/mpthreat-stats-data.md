---
title: Structure MPTHREAT_STATS_DATA (MpClient. h)
description: Données de statistiques sur les menaces supplémentaires.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPTHREAT_STATS_DATA
- PMPTHREAT_STATS_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103560"
---
# <a name="mpthreat_stats_data-structure"></a><span data-ttu-id="ddcf0-105">Structure de données des \_ statistiques de MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="ddcf0-105">MPTHREAT\_STATS\_DATA structure</span></span>

<span data-ttu-id="ddcf0-106">Données de statistiques sur les menaces supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ddcf0-106">Additional threat statistics data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddcf0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddcf0-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a><span data-ttu-id="ddcf0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ddcf0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ddcf0-109">**dwThreatCount**</span><span class="sxs-lookup"><span data-stu-id="ddcf0-109">**dwThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="ddcf0-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ddcf0-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ddcf0-111">Nombre de menaces.</span><span class="sxs-lookup"><span data-stu-id="ddcf0-111">Number of threats.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ddcf0-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddcf0-112">Requirements</span></span>



| <span data-ttu-id="ddcf0-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddcf0-113">Requirement</span></span> | <span data-ttu-id="ddcf0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddcf0-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddcf0-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddcf0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ddcf0-116">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddcf0-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ddcf0-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ddcf0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ddcf0-118">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ddcf0-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ddcf0-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddcf0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddcf0-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddcf0-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





