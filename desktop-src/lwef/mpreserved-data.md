---
title: Structure MPRESERVED_DATA (MpClient. h)
description: Données de notification réservées.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPRESERVED_DATA
- PMPRESERVED_DATA des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104548"
---
# <a name="mpreserved_data-structure"></a><span data-ttu-id="68f4d-105">\_Structure de données MPRESERVED</span><span class="sxs-lookup"><span data-stu-id="68f4d-105">MPRESERVED\_DATA structure</span></span>

<span data-ttu-id="68f4d-106">Données de notification réservées.</span><span class="sxs-lookup"><span data-stu-id="68f4d-106">Reserved notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f4d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68f4d-107">Syntax</span></span>


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a><span data-ttu-id="68f4d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="68f4d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="68f4d-109">**cbReservedData**</span><span class="sxs-lookup"><span data-stu-id="68f4d-109">**cbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="68f4d-110">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="68f4d-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="68f4d-111">Taille des données réservées, en octets.</span><span class="sxs-lookup"><span data-stu-id="68f4d-111">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="68f4d-112">**pbReservedData**</span><span class="sxs-lookup"><span data-stu-id="68f4d-112">**pbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="68f4d-113">Type : **Byte \***</span><span class="sxs-lookup"><span data-stu-id="68f4d-113">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="68f4d-114">Pointeur vers les données réservées.</span><span class="sxs-lookup"><span data-stu-id="68f4d-114">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68f4d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68f4d-115">Requirements</span></span>



| <span data-ttu-id="68f4d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68f4d-116">Requirement</span></span> | <span data-ttu-id="68f4d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="68f4d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68f4d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68f4d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="68f4d-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68f4d-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="68f4d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68f4d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="68f4d-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68f4d-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68f4d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="68f4d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="68f4d-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="68f4d-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





