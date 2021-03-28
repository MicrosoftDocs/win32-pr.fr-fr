---
description: Cette classe est la classe de type d’événement pour les événements d’allocation virtuelle. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: Classe PageFault_VirtualAlloc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: f9e754bc3dc09f492682d5a522a6489cfde27ceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318577"
---
# <a name="pagefault_virtualalloc-class"></a><span data-ttu-id="7086d-104">PageFault \_ VirtualAlloc (classe)</span><span class="sxs-lookup"><span data-stu-id="7086d-104">PageFault\_VirtualAlloc class</span></span>

<span data-ttu-id="7086d-105">Cette classe est la classe de type d’événement pour les événements d’allocation virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7086d-105">This class is the event type class for virtual allocation events.</span></span>

<span data-ttu-id="7086d-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="7086d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7086d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7086d-107">Syntax</span></span>

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="7086d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7086d-108">Members</span></span>

<span data-ttu-id="7086d-109">La classe **PageFault \_ VirtualAlloc** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7086d-109">The **PageFault\_VirtualAlloc** class has these types of members:</span></span>

-   [<span data-ttu-id="7086d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7086d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7086d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7086d-111">Properties</span></span>

<span data-ttu-id="7086d-112">La classe **PageFault \_ VirtualAlloc** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7086d-112">The **PageFault\_VirtualAlloc** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7086d-113">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="7086d-113">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7086d-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7086d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7086d-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7086d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7086d-116">Qualificateurs : WmiDataId (1), pointeur</span><span class="sxs-lookup"><span data-stu-id="7086d-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7086d-117">Adresse de départ à laquelle la mémoire a été allouée ou libérée.</span><span class="sxs-lookup"><span data-stu-id="7086d-117">The starting address at which memory was allocated or freed.</span></span>

</dd> <dt>

<span data-ttu-id="7086d-118">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="7086d-118">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7086d-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7086d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7086d-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7086d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7086d-121">Qualificateurs : WmiDataId (4), format ("x")</span><span class="sxs-lookup"><span data-stu-id="7086d-121">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="7086d-122">Type d’allocation de mémoire qui a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="7086d-122">The type of memory allocation that was performed.</span></span> <span data-ttu-id="7086d-123">Pour connaître les valeurs possibles, consultez le paramètre *flAllocationType* de la fonction [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .</span><span class="sxs-lookup"><span data-stu-id="7086d-123">For possible values, see the *flAllocationType* parameter of the [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) function.</span></span>

</dd> <dt>

<span data-ttu-id="7086d-124">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="7086d-124">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7086d-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7086d-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7086d-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7086d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7086d-127">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="7086d-127">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="7086d-128">Le processus qui possédait la mémoire (peut être différent du thread qui a effectué l’allocation).</span><span class="sxs-lookup"><span data-stu-id="7086d-128">The process that owned the memory (can be different from the thread that performed the allocation).</span></span>

</dd> <dt>

<span data-ttu-id="7086d-129">**Région**</span><span class="sxs-lookup"><span data-stu-id="7086d-129">**RegionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7086d-130">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="7086d-130">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7086d-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7086d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7086d-132">Qualificateurs : WmiDataId (2), extension ("Sizet")</span><span class="sxs-lookup"><span data-stu-id="7086d-132">Qualifiers: WmiDataId(2), Extension("SizeT")</span></span>
</dt> </dl>

<span data-ttu-id="7086d-133">Taille, en octets, de la mémoire qui a été allouée ou libérée.</span><span class="sxs-lookup"><span data-stu-id="7086d-133">The size, in bytes, of the memory that was allocated or freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7086d-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7086d-134">Requirements</span></span>



| <span data-ttu-id="7086d-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7086d-135">Requirement</span></span> | <span data-ttu-id="7086d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="7086d-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="7086d-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7086d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7086d-138">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7086d-138">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="7086d-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7086d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7086d-140">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7086d-140">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7086d-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7086d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7086d-142">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="7086d-142">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 
