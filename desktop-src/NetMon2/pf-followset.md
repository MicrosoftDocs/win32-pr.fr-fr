---
description: La \_ structure FOLLOWSET de PF définit les protocoles qui peuvent précéder ou suivre un protocole.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: Structure de PF_FOLLOWSET (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534340"
---
# <a name="pf_followset-structure"></a><span data-ttu-id="202ab-103">PF \_ FOLLOWSET, structure</span><span class="sxs-lookup"><span data-stu-id="202ab-103">PF\_FOLLOWSET structure</span></span>

<span data-ttu-id="202ab-104">La **structure \_ FOLLOWSET de PF** définit les protocoles qui peuvent précéder ou suivre un protocole.</span><span class="sxs-lookup"><span data-stu-id="202ab-104">The **PF\_FOLLOWSET** structure defines the protocols that may precede or follow a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="202ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="202ab-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a><span data-ttu-id="202ab-106">Membres</span><span class="sxs-lookup"><span data-stu-id="202ab-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="202ab-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="202ab-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="202ab-108">Nombre de protocoles dans la liste.</span><span class="sxs-lookup"><span data-stu-id="202ab-108">Number of protocols in the list.</span></span>

</dd> <dt>

<span data-ttu-id="202ab-109">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="202ab-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="202ab-110">Tableau de [structures \_ FOLLOWENTRY PF](pf-followentry.md) qui décrivent chaque protocole.</span><span class="sxs-lookup"><span data-stu-id="202ab-110">Array of [PF\_FOLLOWENTRY](pf-followentry.md) structures that describe each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="202ab-111">Notes</span><span class="sxs-lookup"><span data-stu-id="202ab-111">Remarks</span></span>

<span data-ttu-id="202ab-112">La [structure \_ PARSERINFO de PF](pf-parserinfo.md) utilise la structure **\_ FOLLOWSET de PF** pour répertorier les protocoles qui peuvent précéder ou suivre le protocole détecté par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="202ab-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_FOLLOWSET** structure to list the protocols that may precede or follow the protocol that the parser detects.</span></span>

<span data-ttu-id="202ab-113">Moniteur réseau utilise les informations de la **structure \_ FOLLOWSET de PF** pour mettre à jour les ensembles suivants d’analyseurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="202ab-113">Network Monitor uses the information in the **PF\_FOLLOWSET** structure to update the follow sets of specific parsers.</span></span> <span data-ttu-id="202ab-114">La **structure \_ FOLLOWSET de PF** doit être allouée à l’aide de **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="202ab-114">The **PF\_FOLLOWSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="202ab-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="202ab-115">Requirements</span></span>



| <span data-ttu-id="202ab-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="202ab-116">Requirement</span></span> | <span data-ttu-id="202ab-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="202ab-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="202ab-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="202ab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="202ab-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="202ab-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="202ab-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="202ab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="202ab-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="202ab-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="202ab-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="202ab-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="202ab-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="202ab-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="202ab-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="202ab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="202ab-125">\_FOLLOWENTRY PF</span><span class="sxs-lookup"><span data-stu-id="202ab-125">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)
</dt> <dt>

[<span data-ttu-id="202ab-126">\_PARSERINFO PF</span><span class="sxs-lookup"><span data-stu-id="202ab-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> </dl>

 

 




