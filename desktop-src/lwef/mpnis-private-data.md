---
title: Structure MPNIS_PRIVATE_DATA (MpClient. h)
description: Notifications NIS privées.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPNIS_PRIVATE_DATA
- PMPNIS_PRIVATE_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740140"
---
# <a name="mpnis_private_data-structure"></a><span data-ttu-id="de887-105">\_Structure de \_ données privées MPNIS</span><span class="sxs-lookup"><span data-stu-id="de887-105">MPNIS\_PRIVATE\_DATA structure</span></span>

<span data-ttu-id="de887-106">Notifications NIS privées.</span><span class="sxs-lookup"><span data-stu-id="de887-106">Private NIS notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="de887-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de887-107">Syntax</span></span>


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a><span data-ttu-id="de887-108">Membres</span><span class="sxs-lookup"><span data-stu-id="de887-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="de887-109">**dwNotificationType**</span><span class="sxs-lookup"><span data-stu-id="de887-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="de887-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="de887-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="de887-111">Type de notification.</span><span class="sxs-lookup"><span data-stu-id="de887-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="de887-112">**cbDataSize**</span><span class="sxs-lookup"><span data-stu-id="de887-112">**cbDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="de887-113">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="de887-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="de887-114">Taille des données réservées, en octets.</span><span class="sxs-lookup"><span data-stu-id="de887-114">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="de887-115">**pbData**</span><span class="sxs-lookup"><span data-stu-id="de887-115">**pbData**</span></span>
</dt> <dd>

<span data-ttu-id="de887-116">Type : **Byte \***</span><span class="sxs-lookup"><span data-stu-id="de887-116">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="de887-117">Pointeur vers les données réservées.</span><span class="sxs-lookup"><span data-stu-id="de887-117">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de887-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de887-118">Requirements</span></span>



| <span data-ttu-id="de887-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de887-119">Requirement</span></span> | <span data-ttu-id="de887-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="de887-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de887-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de887-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de887-122">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de887-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="de887-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de887-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de887-124">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de887-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de887-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="de887-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="de887-126"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="de887-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





