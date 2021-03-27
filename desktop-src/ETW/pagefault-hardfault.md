---
description: Cette classe est la classe de type d’événement pour les événements de défaut de page matérielle. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: Classe PageFault_HardFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: 08afd3df20260a8ede63f4d741b3045ce3a39c1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952322"
---
# <a name="pagefault_hardfault-class"></a><span data-ttu-id="9f7d0-104">PageFault \_ HardFault, classe</span><span class="sxs-lookup"><span data-stu-id="9f7d0-104">PageFault\_HardFault class</span></span>

<span data-ttu-id="9f7d0-105">Cette classe est la classe de type d’événement pour les événements de défaut de page matérielle.</span><span class="sxs-lookup"><span data-stu-id="9f7d0-105">This class is the event type class for hard page fault events.</span></span>

<span data-ttu-id="9f7d0-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="9f7d0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f7d0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f7d0-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a><span data-ttu-id="9f7d0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9f7d0-108">Members</span></span>

<span data-ttu-id="9f7d0-109">La classe **PageFault \_ HardFault** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9f7d0-109">The **PageFault\_HardFault** class has these types of members:</span></span>

-   [<span data-ttu-id="9f7d0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9f7d0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f7d0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9f7d0-111">Properties</span></span>

<span data-ttu-id="9f7d0-112">La classe **PageFault \_ HardFault** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f7d0-112">The **PageFault\_HardFault** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f7d0-113">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-113">**ByteCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f7d0-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f7d0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-116">Qualificateurs : WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="9f7d0-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="9f7d0-117">Quantité de données lues à partir de ReadOffset pour répondre à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="9f7d0-117">Amount of data read from ReadOffset to satisfy the fault.</span></span>

</dd> <dt>

<span data-ttu-id="9f7d0-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f7d0-119">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f7d0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-121">Qualificateurs : WmiDataId (4), pointeur</span><span class="sxs-lookup"><span data-stu-id="9f7d0-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9f7d0-122">Faire correspondre la valeur de ce pointeur à la valeur de pointeur **FileObject** dans un événement de [**\_ nom FileIo**](fileio-name.md) pour déterminer le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="9f7d0-122">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="9f7d0-123">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-123">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f7d0-124">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f7d0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-126">Qualificateurs : WmiDataId (1), extension (« WmiTime »)</span><span class="sxs-lookup"><span data-stu-id="9f7d0-126">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="9f7d0-127">Horodatage de début auquel une erreur de page s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9f7d0-127">Start time stamp at which page fault occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9f7d0-128">**ReadOffset**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-128">**ReadOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f7d0-129">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f7d0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-131">Qualificateurs : WmiDataId (2), format ("x")</span><span class="sxs-lookup"><span data-stu-id="9f7d0-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="9f7d0-132">Décalage de fichier à partir duquel les données ont été lues pour satisfaire l’erreur.</span><span class="sxs-lookup"><span data-stu-id="9f7d0-132">File offset from which data was read to satisfy fault.</span></span>

</dd> <dt>

<span data-ttu-id="9f7d0-133">**TThreadId**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-133">**TThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f7d0-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f7d0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-136">Qualificateurs : WmiDataId (5), format ("x")</span><span class="sxs-lookup"><span data-stu-id="9f7d0-136">Qualifiers: WmiDataId(5), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="9f7d0-137">Identificateur du thread qui a rencontré l’erreur de page.</span><span class="sxs-lookup"><span data-stu-id="9f7d0-137">Thread identifier of the thread that encountered the page fault.</span></span>

</dd> <dt>

<span data-ttu-id="9f7d0-138">**VirtualAddress**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-138">**VirtualAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f7d0-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f7d0-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f7d0-141">Qualificateurs : WmiDataId (3), pointeur</span><span class="sxs-lookup"><span data-stu-id="9f7d0-141">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9f7d0-142">Adresse défaillante.</span><span class="sxs-lookup"><span data-stu-id="9f7d0-142">Faulting address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f7d0-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9f7d0-143">Requirements</span></span>



| <span data-ttu-id="9f7d0-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f7d0-144">Requirement</span></span> | <span data-ttu-id="9f7d0-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f7d0-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f7d0-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f7d0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9f7d0-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f7d0-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9f7d0-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f7d0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9f7d0-149">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f7d0-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f7d0-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f7d0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f7d0-151">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="9f7d0-151">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




