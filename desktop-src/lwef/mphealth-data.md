---
title: Structure MPHEALTH_DATA (MpClient. h)
description: Données de notification d’intégrité.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPHEALTH_DATA
- PMPHEALTH_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106539016"
---
# <a name="mphealth_data-structure"></a><span data-ttu-id="7007c-105">\_Structure de données MPHEALTH</span><span class="sxs-lookup"><span data-stu-id="7007c-105">MPHEALTH\_DATA structure</span></span>

<span data-ttu-id="7007c-106">Données de notification d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="7007c-106">Health notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7007c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7007c-107">Syntax</span></span>


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a><span data-ttu-id="7007c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7007c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7007c-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="7007c-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="7007c-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7007c-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7007c-111">Type de notification.</span><span class="sxs-lookup"><span data-stu-id="7007c-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="7007c-112">**dwNotificationFlag**</span><span class="sxs-lookup"><span data-stu-id="7007c-112">**dwNotificationFlag**</span></span>
</dt> <dd>

<span data-ttu-id="7007c-113">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7007c-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7007c-114">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7007c-114">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7007c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7007c-115">Requirements</span></span>



| <span data-ttu-id="7007c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7007c-116">Requirement</span></span> | <span data-ttu-id="7007c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7007c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7007c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7007c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7007c-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7007c-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7007c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7007c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7007c-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7007c-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7007c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7007c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7007c-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7007c-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





