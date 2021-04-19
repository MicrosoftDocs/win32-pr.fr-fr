---
description: La \_ structure HANDOFFSET de PF définit les protocoles qui sont confiés à l’analyseur, ou les protocoles que l’analyseur transmet.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: Structure de PF_HANDOFFSET (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541216"
---
# <a name="pf_handoffset-structure"></a><span data-ttu-id="2a6bf-103">PF \_ HANDOFFSET, structure</span><span class="sxs-lookup"><span data-stu-id="2a6bf-103">PF\_HANDOFFSET structure</span></span>

<span data-ttu-id="2a6bf-104">La **structure \_ HANDOFFSET de PF** définit les protocoles qui sont confiés à l’analyseur, ou les protocoles que l’analyseur transmet.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-104">The **PF\_HANDOFFSET** structure defines the protocols that hand off to the parser, or the protocols that the parser hands off to.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a6bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a6bf-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a><span data-ttu-id="2a6bf-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2a6bf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a6bf-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-108">Nombre de protocoles.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-108">Number of protocols.</span></span>

</dd> <dt>

<span data-ttu-id="2a6bf-109">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="2a6bf-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="2a6bf-110">Tableau de structures [ \_ HANDOFFENTRY PF](pf-handoffentry.md) qui définissent chaque protocole.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-110">An array of [PF\_HANDOFFENTRY](pf-handoffentry.md) structures that define each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a6bf-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2a6bf-111">Remarks</span></span>

<span data-ttu-id="2a6bf-112">La [structure \_ PARSERINFO de PF](pf-parserinfo.md) utilise la structure **\_ HANDOFFSET de PF** pour répertorier les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2a6bf-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_HANDOFFSET** structure to list the following:</span></span>

-   <span data-ttu-id="2a6bf-113">Les protocoles qui sont confiés à l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-113">Which protocols hand off to the parser.</span></span>
-   <span data-ttu-id="2a6bf-114">Les protocoles que l’analyseur transmet.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-114">Which protocols the parser hands off to.</span></span>

<span data-ttu-id="2a6bf-115">La **structure \_ HANDOFFSET de PF** doit être allouée à l’aide de **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="2a6bf-115">The **PF\_HANDOFFSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a6bf-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a6bf-116">Requirements</span></span>



| <span data-ttu-id="2a6bf-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a6bf-117">Requirement</span></span> | <span data-ttu-id="2a6bf-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a6bf-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2a6bf-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a6bf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2a6bf-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a6bf-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2a6bf-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a6bf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2a6bf-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a6bf-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2a6bf-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a6bf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a6bf-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a6bf-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a6bf-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a6bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a6bf-126">\_PARSERINFO PF</span><span class="sxs-lookup"><span data-stu-id="2a6bf-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="2a6bf-127">\_HANDOFFENTRY PF</span><span class="sxs-lookup"><span data-stu-id="2a6bf-127">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)
</dt> </dl>

 

 




