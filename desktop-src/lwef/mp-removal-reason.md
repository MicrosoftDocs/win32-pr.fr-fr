---
title: Énumération MP_REMOVAL_REASON (MpClient. h)
description: Raison de la suppression de la signature FastPath.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- MP_REMOVAL_REASON énumération des fonctionnalités d’environnement Windows héritées
- PMP_REMOVAL_REASON des fonctionnalités d’environnement Windows héritées d’un pointeur d’énumération
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ce70f46bd95d4183343990b40594326ed5d3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743188"
---
# <a name="mp_removal_reason-enumeration"></a><span data-ttu-id="b2a48-105">Énumération des raisons de suppression du pack d' \_ installation \_</span><span class="sxs-lookup"><span data-stu-id="b2a48-105">MP\_REMOVAL\_REASON enumeration</span></span>

<span data-ttu-id="b2a48-106">Raison de la suppression de la signature FastPath.</span><span class="sxs-lookup"><span data-stu-id="b2a48-106">FastPath signature removal reason.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2a48-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2a48-107">Syntax</span></span>


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a><span data-ttu-id="b2a48-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b2a48-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b2a48-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**suppression du pack d' \_ installation \_ inconnue**</span><span class="sxs-lookup"><span data-stu-id="b2a48-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**MP\_REMOVAL\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="b2a48-110">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="b2a48-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="b2a48-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**Manuel de suppression du pack d' \_ installation \_**</span><span class="sxs-lookup"><span data-stu-id="b2a48-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**MP\_REMOVAL\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="b2a48-112">Manuelles.</span><span class="sxs-lookup"><span data-stu-id="b2a48-112">Manual.</span></span>

</dd> <dt>

<span data-ttu-id="b2a48-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**désinstallation automatique du pack d' \_ installation \_**</span><span class="sxs-lookup"><span data-stu-id="b2a48-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**MP\_REMOVAL\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="b2a48-114">Automatique.</span><span class="sxs-lookup"><span data-stu-id="b2a48-114">Automatic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2a48-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2a48-115">Requirements</span></span>



| <span data-ttu-id="b2a48-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2a48-116">Requirement</span></span> | <span data-ttu-id="b2a48-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2a48-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a48-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2a48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2a48-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2a48-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b2a48-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2a48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2a48-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2a48-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2a48-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2a48-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2a48-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2a48-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





