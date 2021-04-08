---
description: La \_ structure FOLLOWENTRY de PF définit un protocole que Moniteur réseau ajoute au jeu suivant d’un analyseur.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Structure de PF_FOLLOWENTRY (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866262"
---
# <a name="pf_followentry-structure"></a><span data-ttu-id="4f1b5-103">PF \_ FOLLOWENTRY, structure</span><span class="sxs-lookup"><span data-stu-id="4f1b5-103">PF\_FOLLOWENTRY structure</span></span>

<span data-ttu-id="4f1b5-104">La **structure \_ FOLLOWENTRY de PF** définit un protocole que Moniteur réseau ajoute au jeu suivant d’un analyseur.</span><span class="sxs-lookup"><span data-stu-id="4f1b5-104">The **PF\_FOLLOWENTRY** structure defines a protocol that Network Monitor adds to the follow set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f1b5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f1b5-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a><span data-ttu-id="4f1b5-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4f1b5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f1b5-107">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="4f1b5-107">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="4f1b5-108">Nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="4f1b5-108">The name of the protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f1b5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4f1b5-109">Remarks</span></span>

<span data-ttu-id="4f1b5-110">La [structure \_ FOLLOWSET de PF](pf-followset.md) utilise un tableau de structures **\_ FOLLOWENTRY PF** .</span><span class="sxs-lookup"><span data-stu-id="4f1b5-110">The [PF\_FOLLOWSET](pf-followset.md) structure uses an array of **PF\_FOLLOWENTRY** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f1b5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f1b5-111">Requirements</span></span>



| <span data-ttu-id="4f1b5-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f1b5-112">Requirement</span></span> | <span data-ttu-id="4f1b5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f1b5-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1b5-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f1b5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4f1b5-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f1b5-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4f1b5-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f1b5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4f1b5-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f1b5-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4f1b5-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f1b5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f1b5-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f1b5-119"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f1b5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f1b5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f1b5-121">\_FOLLOWSET PF</span><span class="sxs-lookup"><span data-stu-id="4f1b5-121">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> </dl>

 

 




