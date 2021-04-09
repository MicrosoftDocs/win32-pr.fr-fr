---
title: Structure MPSCAN_RESOURCES (MpClient. h)
description: Informations de ressource passées pendant une opération d’analyse.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPSCAN_RESOURCES
- PMPSCAN_RESOURCES des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942855"
---
# <a name="mpscan_resources-structure"></a><span data-ttu-id="74d6a-105">\_Structure des ressources MPSCAN</span><span class="sxs-lookup"><span data-stu-id="74d6a-105">MPSCAN\_RESOURCES structure</span></span>

<span data-ttu-id="74d6a-106">Informations de ressource passées pendant une opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="74d6a-106">Resource information passed during a scan operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="74d6a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74d6a-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a><span data-ttu-id="74d6a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="74d6a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="74d6a-109">**dwResourceCount**</span><span class="sxs-lookup"><span data-stu-id="74d6a-109">**dwResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="74d6a-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="74d6a-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="74d6a-111">Nombre de ressources.</span><span class="sxs-lookup"><span data-stu-id="74d6a-111">Count of resources.</span></span>

</dd> <dt>

<span data-ttu-id="74d6a-112">**pResourceList**</span><span class="sxs-lookup"><span data-stu-id="74d6a-112">**pResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="74d6a-113">Type : **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="74d6a-113">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="74d6a-114">Tableau de ressources.</span><span class="sxs-lookup"><span data-stu-id="74d6a-114">Array of resources.</span></span> <span data-ttu-id="74d6a-115">Consultez [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="74d6a-115">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74d6a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74d6a-116">Requirements</span></span>



| <span data-ttu-id="74d6a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74d6a-117">Requirement</span></span> | <span data-ttu-id="74d6a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="74d6a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74d6a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74d6a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="74d6a-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74d6a-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="74d6a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74d6a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="74d6a-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74d6a-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74d6a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="74d6a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="74d6a-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="74d6a-124"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74d6a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74d6a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74d6a-126">**\_informations MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="74d6a-126">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





