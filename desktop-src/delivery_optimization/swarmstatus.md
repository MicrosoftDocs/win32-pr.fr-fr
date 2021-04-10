---
title: Énumération SwarmStatus (Deliveryoptimization. h)
description: Définit l’état d’un fichier dans le client d’optimisation de la remise.
ms.assetid: D40ABDD3-5573-4A8D-8608-4CB0F396CCAD
keywords:
- Énumération SwarmStatus
topic_type:
- apiref
api_name:
- SwarmStatus
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3622f819679c2fd2b28d66e371a8b88e0a2d2f70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105319"
---
# <a name="swarmstatus-enumeration"></a><span data-ttu-id="1281c-104">Énumération SwarmStatus</span><span class="sxs-lookup"><span data-stu-id="1281c-104">SwarmStatus enumeration</span></span>

<span data-ttu-id="1281c-105">Définit l’état d’un fichier dans le client d’optimisation de la remise.</span><span class="sxs-lookup"><span data-stu-id="1281c-105">Defines the status of a file within the delivery optimization client.</span></span>

## <a name="syntax"></a><span data-ttu-id="1281c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1281c-106">Syntax</span></span>


```C++
typedef enum _SwarmStatus { 
  SwarmStatus_Downloading  = 0,
  SwarmStatus_Complete     = 1,
  SwarmStatus_Caching      = 2,
  SwarmStatus_Paused       = 3
} SwarmStatus;
```



## <a name="constants"></a><span data-ttu-id="1281c-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="1281c-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1281c-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span><span class="sxs-lookup"><span data-stu-id="1281c-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span></span>
</dt> <dd>

<span data-ttu-id="1281c-109">Le fichier est en téléchargement.</span><span class="sxs-lookup"><span data-stu-id="1281c-109">The file is downloading.</span></span>

</dd> <dt>

<span data-ttu-id="1281c-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span><span class="sxs-lookup"><span data-stu-id="1281c-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span></span>
</dt> <dd>

<span data-ttu-id="1281c-111">Le téléchargement du fichier est terminé.</span><span class="sxs-lookup"><span data-stu-id="1281c-111">The file download is complete.</span></span>

</dd> <dt>

<span data-ttu-id="1281c-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span><span class="sxs-lookup"><span data-stu-id="1281c-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span></span>
</dt> <dd>

<span data-ttu-id="1281c-113">Le fichier est en cours de mise en cache.</span><span class="sxs-lookup"><span data-stu-id="1281c-113">The file is being cached.</span></span>

</dd> <dt>

<span data-ttu-id="1281c-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span><span class="sxs-lookup"><span data-stu-id="1281c-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="1281c-115">Le téléchargement du fichier est suspendu.</span><span class="sxs-lookup"><span data-stu-id="1281c-115">The file download is paused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1281c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1281c-116">Requirements</span></span>



| <span data-ttu-id="1281c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1281c-117">Requirement</span></span> | <span data-ttu-id="1281c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1281c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1281c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1281c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1281c-120">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1281c-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1281c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1281c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1281c-122">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1281c-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1281c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1281c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1281c-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1281c-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





