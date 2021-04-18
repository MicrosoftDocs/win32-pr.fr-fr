---
description: La structure ANDEXP contient un tableau de correspondances de modèle utilisées pour évaluer les données de frame.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: ANDEXP, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319710"
---
# <a name="andexp-structure"></a><span data-ttu-id="e2e75-103">ANDEXP, structure</span><span class="sxs-lookup"><span data-stu-id="e2e75-103">ANDEXP structure</span></span>

<span data-ttu-id="e2e75-104">La structure **ANDEXP** contient un tableau de correspondances de modèle utilisées pour évaluer les données de frame.</span><span class="sxs-lookup"><span data-stu-id="e2e75-104">The **ANDEXP** structure contains an array of pattern matches used to evaluate frame data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e75-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2e75-105">Syntax</span></span>


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a><span data-ttu-id="e2e75-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e2e75-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2e75-107">**nPatternMatches**</span><span class="sxs-lookup"><span data-stu-id="e2e75-107">**nPatternMatches**</span></span>
</dt> <dd>

<span data-ttu-id="e2e75-108">Nombre de correspondances de modèle.</span><span class="sxs-lookup"><span data-stu-id="e2e75-108">Number of pattern matches.</span></span>

</dd> <dt>

<span data-ttu-id="e2e75-109">**PatternMatch**</span><span class="sxs-lookup"><span data-stu-id="e2e75-109">**PatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="e2e75-110">Tableau d’éléments de correspondance de modèle.</span><span class="sxs-lookup"><span data-stu-id="e2e75-110">Array of pattern match elements.</span></span> <span data-ttu-id="e2e75-111">Notez que chaque structure **ANDEXP** peut contenir jusqu’à quatre éléments de correspondance de modèle.</span><span class="sxs-lookup"><span data-stu-id="e2e75-111">Note that each **ANDEXP** structure can contain up to four pattern match elements.</span></span> <span data-ttu-id="e2e75-112">Pour plus d’informations sur ce membre, consultez [filtres de capture](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e2e75-112">For more information about this member, see [Capture Filters](capture-filters.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2e75-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e2e75-113">Remarks</span></span>

<span data-ttu-id="e2e75-114">Les modèles du  \[ tableau de modèles Max PatternMatch \_ \] sont joints en tant qu’homologues dans les instructions or logiques au format</span><span class="sxs-lookup"><span data-stu-id="e2e75-114">The patterns in the **PatternMatch**\[MAX\_PATTERNS\] array are joined as peers in logical OR statements in the format</span></span>

<span data-ttu-id="e2e75-115">(Modèle 1 \| \| Modèle 2 modèle \| \| 3).</span><span class="sxs-lookup"><span data-stu-id="e2e75-115">(Pattern 1 \|\| Pattern 2 \|\| Pattern 3).</span></span>

<span data-ttu-id="e2e75-116">Pour plus d’informations sur l’implémentation de cette structure, consultez [filtres de capture](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="e2e75-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md) .</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e75-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2e75-117">Requirements</span></span>



| <span data-ttu-id="e2e75-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2e75-118">Requirement</span></span> | <span data-ttu-id="e2e75-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2e75-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e75-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e75-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e75-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2e75-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e2e75-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2e75-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e75-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2e75-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e2e75-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2e75-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2e75-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2e75-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e75-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2e75-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e75-127">PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="e2e75-127">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




