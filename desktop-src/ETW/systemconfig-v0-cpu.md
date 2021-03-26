---
description: Cette classe est la classe de type d’événement pour les événements de configuration de l’UC.
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: Classe SystemConfig_V0_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6963201f76afa40e9b1741dc2936fa2ab4433a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952824"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="c3cef-103">\_Classe de \_ processeur SystemConfig v0</span><span class="sxs-lookup"><span data-stu-id="c3cef-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="c3cef-104">Cette classe est la classe de type d’événement pour les événements de configuration de l’UC.</span><span class="sxs-lookup"><span data-stu-id="c3cef-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="c3cef-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="c3cef-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cef-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3cef-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a><span data-ttu-id="c3cef-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c3cef-107">Members</span></span>

<span data-ttu-id="c3cef-108">La classe d' **\_ \_ UC SystemConfig v0** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c3cef-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="c3cef-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3cef-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3cef-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3cef-110">Properties</span></span>

<span data-ttu-id="c3cef-111">La classe d' **\_ \_ UC SystemConfig v0** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c3cef-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3cef-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="c3cef-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cef-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3cef-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3cef-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-115">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="c3cef-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c3cef-116">Granularité avec laquelle la mémoire virtuelle est allouée.</span><span class="sxs-lookup"><span data-stu-id="c3cef-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="c3cef-117">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="c3cef-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cef-118">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="c3cef-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3cef-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-120">Qualificateurs : **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="c3cef-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c3cef-121">Nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c3cef-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c3cef-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="c3cef-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cef-123">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="c3cef-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3cef-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-125">Qualificateurs : **WmiDataId** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="c3cef-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="c3cef-126">Nom du domaine dans lequel l’ordinateur est membre.</span><span class="sxs-lookup"><span data-stu-id="c3cef-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="c3cef-127">**MemS**</span><span class="sxs-lookup"><span data-stu-id="c3cef-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cef-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3cef-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3cef-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-130">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="c3cef-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c3cef-131">Quantité totale de mémoire physique disponible pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c3cef-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="c3cef-132">**MHz**</span><span class="sxs-lookup"><span data-stu-id="c3cef-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cef-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3cef-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3cef-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-135">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="c3cef-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="c3cef-136">Vitesse maximale du processeur, en mégahertz.</span><span class="sxs-lookup"><span data-stu-id="c3cef-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="c3cef-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="c3cef-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cef-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3cef-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3cef-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-140">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="c3cef-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c3cef-141">Nombre de processeurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c3cef-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c3cef-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="c3cef-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3cef-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3cef-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3cef-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3cef-145">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="c3cef-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="c3cef-146">Taille d’une page d’échange, en octets.</span><span class="sxs-lookup"><span data-stu-id="c3cef-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3cef-147">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c3cef-147">Requirements</span></span>



| <span data-ttu-id="c3cef-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3cef-148">Requirement</span></span> | <span data-ttu-id="c3cef-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3cef-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3cef-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3cef-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c3cef-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3cef-151">None supported</span></span><br/>                            |
| <span data-ttu-id="c3cef-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3cef-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c3cef-153">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3cef-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3cef-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3cef-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cef-155">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="c3cef-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




