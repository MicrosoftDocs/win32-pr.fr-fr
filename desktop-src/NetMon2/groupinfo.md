---
description: Associe un nom de groupe et son descripteur.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: GROUPINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544614"
---
# <a name="groupinfo-structure"></a><span data-ttu-id="28e7c-103">GROUPINFO, structure</span><span class="sxs-lookup"><span data-stu-id="28e7c-103">GROUPINFO structure</span></span>

<span data-ttu-id="28e7c-104">La structure **GROUPINFO** associe un nom de groupe et son descripteur.</span><span class="sxs-lookup"><span data-stu-id="28e7c-104">The **GROUPINFO** structure associates a group name and its handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28e7c-105">Syntax</span></span>


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a><span data-ttu-id="28e7c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="28e7c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="28e7c-107">**szGroupName**</span><span class="sxs-lookup"><span data-stu-id="28e7c-107">**szGroupName**</span></span>
</dt> <dd>

<span data-ttu-id="28e7c-108">Valeur incrémentée d’un tableau dans la structure **GroupName** .</span><span class="sxs-lookup"><span data-stu-id="28e7c-108">Incremented value of an array in the **GROUPNAME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="28e7c-109">**hGroup**</span><span class="sxs-lookup"><span data-stu-id="28e7c-109">**hGroup**</span></span>
</dt> <dd>

<span data-ttu-id="28e7c-110">Handle vers un groupe.</span><span class="sxs-lookup"><span data-stu-id="28e7c-110">Handle to a group.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28e7c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28e7c-111">Requirements</span></span>



| <span data-ttu-id="28e7c-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28e7c-112">Requirement</span></span> | <span data-ttu-id="28e7c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="28e7c-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="28e7c-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28e7c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="28e7c-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28e7c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="28e7c-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28e7c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="28e7c-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28e7c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="28e7c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="28e7c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="28e7c-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="28e7c-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




