---
description: La structure HANDOFFTABLE définit les protocoles d’une table de remise.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: HANDOFFTABLE, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517444"
---
# <a name="handofftable-structure"></a><span data-ttu-id="3b602-103">HANDOFFTABLE, structure</span><span class="sxs-lookup"><span data-stu-id="3b602-103">HANDOFFTABLE structure</span></span>

<span data-ttu-id="3b602-104">La structure **HANDOFFTABLE** définit les protocoles d’une table de remise.</span><span class="sxs-lookup"><span data-stu-id="3b602-104">The **HANDOFFTABLE** structure defines the protocols of a handoff table.</span></span>

<span data-ttu-id="3b602-105">Cette structure est renseignée par Moniteur réseau en fonction des informations contenues dans un fichier. ini fourni par l’utilisateur fourni lors de l’appel de la fonction [**CreateHandoffTable**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="3b602-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b602-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b602-106">Syntax</span></span>


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a><span data-ttu-id="3b602-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3b602-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b602-108">**\_SIG chaud**</span><span class="sxs-lookup"><span data-stu-id="3b602-108">**hot\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="3b602-109">Signature qui identifie cette table comme table de remise.</span><span class="sxs-lookup"><span data-stu-id="3b602-109">Signature that identifies this table as a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="3b602-110">**\_NumEntries chaud**</span><span class="sxs-lookup"><span data-stu-id="3b602-110">**hot\_NumEntries**</span></span>
</dt> <dd>

<span data-ttu-id="3b602-111">Nombre d’entrées qui Moniteur réseau ajoutées à la table de remise.</span><span class="sxs-lookup"><span data-stu-id="3b602-111">Number of entries that Network Monitor added to the handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="3b602-112">**entrées réactives \_**</span><span class="sxs-lookup"><span data-stu-id="3b602-112">**hot\_Entries**</span></span>
</dt> <dd>

<span data-ttu-id="3b602-113">Table de remise.</span><span class="sxs-lookup"><span data-stu-id="3b602-113">Handoff table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b602-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3b602-114">Remarks</span></span>

<span data-ttu-id="3b602-115">Cette structure, ainsi que les structures HANDOFFENTRY associées, sont renseignées par Moniteur réseau lorsque Moniteur réseau crée une table de remise.</span><span class="sxs-lookup"><span data-stu-id="3b602-115">This structure, and its associated HANDOFFENTRY structures, are filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

<span data-ttu-id="3b602-116">Les informations de protocole qui sont utilisées lors de la création d’une table de remise sont fournies dans un fichier. ini fourni par l’application lorsque [**CreateHandoffTable**](createhandofftable.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="3b602-116">The protocol information that is used when creating a handoff table is provided in an .ini file supplied by the application when [**CreateHandoffTable**](createhandofftable.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b602-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b602-117">Requirements</span></span>



| <span data-ttu-id="3b602-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b602-118">Requirement</span></span> | <span data-ttu-id="3b602-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b602-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b602-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b602-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b602-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b602-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b602-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b602-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b602-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b602-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b602-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b602-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b602-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b602-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b602-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b602-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b602-127">HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="3b602-127">HANDOFFENTRY</span></span>](handoffentry.md)
</dt> <dt>

[<span data-ttu-id="3b602-128">CreateHandoffTable</span><span class="sxs-lookup"><span data-stu-id="3b602-128">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> </dl>

 

 




