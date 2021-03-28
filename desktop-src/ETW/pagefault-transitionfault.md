---
description: Cette classe est la classe de type d’événement pour les événements de défaut de page. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: cc2b7a93-6974-4872-98f3-d6cb81861ae5
title: Classe PageFault_TransitionFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_TransitionFault
- PageFault_TransitionFault.VirtualAddress
- PageFault_TransitionFault.ProgramCounter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4721e2d342750b12baa58bb69f72606511c14143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866425"
---
# <a name="pagefault_transitionfault-class"></a><span data-ttu-id="47088-104">PageFault \_ TransitionFault, classe</span><span class="sxs-lookup"><span data-stu-id="47088-104">PageFault\_TransitionFault class</span></span>

<span data-ttu-id="47088-105">Cette classe est la classe de type d’événement pour les événements de défaut de page.</span><span class="sxs-lookup"><span data-stu-id="47088-105">This class is the event type class for page fault events.</span></span>

<span data-ttu-id="47088-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="47088-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="47088-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47088-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14}, EventTypeName{"TransitionFault", "DemandZeroFault", "CopyOnWrite", "GuardPageFault", "HardPageFault"}]
class PageFault_TransitionFault : PageFault_V2
{
  uint32 VirtualAddress;
  uint32 ProgramCounter;
};
```

## <a name="members"></a><span data-ttu-id="47088-108">Membres</span><span class="sxs-lookup"><span data-stu-id="47088-108">Members</span></span>

<span data-ttu-id="47088-109">La classe **PageFault \_ TransitionFault** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="47088-109">The **PageFault\_TransitionFault** class has these types of members:</span></span>

-   [<span data-ttu-id="47088-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="47088-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47088-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="47088-111">Properties</span></span>

<span data-ttu-id="47088-112">La classe **PageFault \_ TransitionFault** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="47088-112">The **PageFault\_TransitionFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47088-113">ProgramCounter</span><span class="sxs-lookup"><span data-stu-id="47088-113">ProgramCounter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47088-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47088-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47088-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="47088-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47088-116">Qualificateurs : WmiDataId (2), pointeur</span><span class="sxs-lookup"><span data-stu-id="47088-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="47088-117">Pointeur vers l’instruction en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="47088-117">Pointer to the current instruction being executed.</span></span>

</dd> <dt>

<span data-ttu-id="47088-118">VirtualAddress</span><span class="sxs-lookup"><span data-stu-id="47088-118">VirtualAddress</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47088-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="47088-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47088-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="47088-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47088-121">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="47088-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="47088-122">Adresse virtuelle de la page qui a provoqué l’erreur de page.</span><span class="sxs-lookup"><span data-stu-id="47088-122">Virtual address of the page that caused the page fault.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47088-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="47088-123">Requirements</span></span>



| <span data-ttu-id="47088-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47088-124">Requirement</span></span> | <span data-ttu-id="47088-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="47088-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="47088-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47088-126">Minimum supported client</span></span><br/> | <span data-ttu-id="47088-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47088-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="47088-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47088-128">Minimum supported server</span></span><br/> | <span data-ttu-id="47088-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47088-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="47088-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47088-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47088-131">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="47088-131">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




