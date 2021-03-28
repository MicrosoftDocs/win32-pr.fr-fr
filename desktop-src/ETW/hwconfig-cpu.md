---
description: La \_ classe UC HWConfig est la classe de type d’événement pour les événements de configuration de l’UC. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: Classe HWConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 493952e25080d4a64e018477ca1b45033c8747af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972510"
---
# <a name="hwconfig_cpu-class"></a><span data-ttu-id="03f22-104">\_Classe UC HWConfig</span><span class="sxs-lookup"><span data-stu-id="03f22-104">HWConfig\_CPU class</span></span>

<span data-ttu-id="03f22-105">La **classe \_ UC HWConfig** est la classe de type d’événement pour les événements de configuration de l’UC.</span><span class="sxs-lookup"><span data-stu-id="03f22-105">The **HWConfig\_CPU** class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="03f22-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="03f22-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f22-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03f22-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a><span data-ttu-id="03f22-108">Membres</span><span class="sxs-lookup"><span data-stu-id="03f22-108">Members</span></span>

<span data-ttu-id="03f22-109">La **classe \_ UC HWConfig** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="03f22-109">The **HWConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="03f22-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="03f22-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03f22-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="03f22-111">Properties</span></span>

<span data-ttu-id="03f22-112">La **classe \_ UC HWConfig** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="03f22-112">The **HWConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03f22-113">AllocationGranularity</span><span class="sxs-lookup"><span data-stu-id="03f22-113">AllocationGranularity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f22-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03f22-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f22-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03f22-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f22-116">Qualificateurs : WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="03f22-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="03f22-117">Granularité avec laquelle la mémoire virtuelle est allouée.</span><span class="sxs-lookup"><span data-stu-id="03f22-117">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="03f22-118">ComputerName</span><span class="sxs-lookup"><span data-stu-id="03f22-118">ComputerName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f22-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="03f22-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f22-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03f22-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f22-121">Qualificateurs : WmiDataId (6), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="03f22-121">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="03f22-122">Nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="03f22-122">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="03f22-123">MemS</span><span class="sxs-lookup"><span data-stu-id="03f22-123">MemSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f22-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03f22-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f22-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03f22-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f22-126">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="03f22-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="03f22-127">Quantité totale de mémoire physique disponible pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="03f22-127">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="03f22-128">MHz</span><span class="sxs-lookup"><span data-stu-id="03f22-128">MHz</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f22-129">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03f22-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f22-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03f22-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f22-131">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="03f22-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="03f22-132">Vitesse maximale du processeur, en mégahertz.</span><span class="sxs-lookup"><span data-stu-id="03f22-132">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="03f22-133">NumberOfProcessors</span><span class="sxs-lookup"><span data-stu-id="03f22-133">NumberOfProcessors</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f22-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03f22-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f22-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03f22-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f22-136">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="03f22-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="03f22-137">Nombre de processeurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="03f22-137">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="03f22-138">PageSize</span><span class="sxs-lookup"><span data-stu-id="03f22-138">PageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f22-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03f22-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f22-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="03f22-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f22-141">Qualificateurs : WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="03f22-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="03f22-142">Taille d’une page d’échange, en octets.</span><span class="sxs-lookup"><span data-stu-id="03f22-142">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03f22-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="03f22-143">Requirements</span></span>



| <span data-ttu-id="03f22-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03f22-144">Requirement</span></span> | <span data-ttu-id="03f22-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f22-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="03f22-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03f22-146">Minimum supported client</span></span><br/> | <span data-ttu-id="03f22-147">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03f22-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="03f22-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03f22-148">Minimum supported server</span></span><br/> | <span data-ttu-id="03f22-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="03f22-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="03f22-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03f22-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f22-151">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="03f22-151">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




