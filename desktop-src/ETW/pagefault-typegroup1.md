---
description: Cette classe est la classe de type d’événement pour les événements de défaut de page. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 59cb1091-af21-4fe6-87b8-17a262cc4467
title: Classe PageFault_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TypeGroup1
- PageFault_TypeGroup1.VirtualAddress
- PageFault_TypeGroup1.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4bf1f49c909833d75af844c8f2f943a01b6a5d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203611"
---
# <a name="pagefault_typegroup1-class"></a><span data-ttu-id="e70e8-104">PageFault \_ TypeGroup1, classe</span><span class="sxs-lookup"><span data-stu-id="e70e8-104">PageFault\_TypeGroup1 class</span></span>

<span data-ttu-id="e70e8-105">Cette classe est la classe de type d’événement pour les événements de défaut de page.</span><span class="sxs-lookup"><span data-stu-id="e70e8-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="e70e8-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="e70e8-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70e8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e70e8-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault", "AccessViolation"}]
class PageFault_TypeGroup1 : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="e70e8-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e70e8-108">Members</span></span>

<span data-ttu-id="e70e8-109">La classe **PageFault \_ TypeGroup1** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e70e8-109">The **PageFault\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="e70e8-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e70e8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e70e8-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e70e8-111">Properties</span></span>

<span data-ttu-id="e70e8-112">La classe **PageFault \_ TypeGroup1** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e70e8-112">The **PageFault\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e70e8-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="e70e8-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e8-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e70e8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e70e8-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e70e8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e70e8-116">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="e70e8-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e70e8-117">Pointeur vers l’instruction en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e70e8-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="e70e8-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="e70e8-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e70e8-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e70e8-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e70e8-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e70e8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e70e8-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="e70e8-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e70e8-122">Adresse virtuelle de la page qui a provoqué l’erreur de page.</span><span class="sxs-lookup"><span data-stu-id="e70e8-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e70e8-123">Notes</span><span class="sxs-lookup"><span data-stu-id="e70e8-123">Remarks</span></span>

<span data-ttu-id="e70e8-124">Une erreur de page se produit lorsqu’une page recherchée dans le cache mémoire est introuvable et doit être récupérée à partir d’un autre emplacement en mémoire (erreur logicielle) ou à partir d’un disque (défaillance matérielle).</span><span class="sxs-lookup"><span data-stu-id="e70e8-124">A page fault occurs when a page sought in the memory cache is not found there and must be retrieved from elsewhere in memory (a soft fault) or from disk (a hard fault).</span></span>

## <a name="requirements"></a><span data-ttu-id="e70e8-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e70e8-125">Requirements</span></span>



| <span data-ttu-id="e70e8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e70e8-126">Requirement</span></span> | <span data-ttu-id="e70e8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e70e8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e70e8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e70e8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e70e8-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e70e8-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e70e8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e70e8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e70e8-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e70e8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e70e8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e70e8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70e8-133">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="e70e8-133">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




