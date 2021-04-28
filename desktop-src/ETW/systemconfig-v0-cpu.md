---
description: Classe SystemConfig_V0_CPU-cette classe est la classe de type d’événement pour les événements de configuration de l’UC.
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
ms.openlocfilehash: de3b63def40cb6ead40f6f4c95625603cfc581ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105987"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="7b9c6-103">\_Classe de \_ processeur SystemConfig v0</span><span class="sxs-lookup"><span data-stu-id="7b9c6-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="7b9c6-104">Cette classe est la classe de type d’événement pour les événements de configuration de l’UC.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="7b9c6-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9c6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b9c6-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="7b9c6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7b9c6-107">Members</span></span>

<span data-ttu-id="7b9c6-108">La classe d' **\_ \_ UC SystemConfig v0** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b9c6-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="7b9c6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b9c6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b9c6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b9c6-110">Properties</span></span>

<span data-ttu-id="7b9c6-111">La classe d' **\_ \_ UC SystemConfig v0** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b9c6-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9c6-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b9c6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-115">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="7b9c6-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="7b9c6-116">Granularité avec laquelle la mémoire virtuelle est allouée.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="7b9c6-117">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9c6-118">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b9c6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-120">Qualificateurs : **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="7b9c6-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="7b9c6-121">Nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="7b9c6-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9c6-123">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b9c6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-125">Qualificateurs : **WmiDataId** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="7b9c6-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="7b9c6-126">Nom du domaine dans lequel l’ordinateur est membre.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="7b9c6-127">**MemS**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9c6-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b9c6-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-130">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="7b9c6-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="7b9c6-131">Quantité totale de mémoire physique disponible pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7b9c6-132">**MHz**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9c6-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b9c6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-135">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="7b9c6-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="7b9c6-136">Vitesse maximale du processeur, en mégahertz.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="7b9c6-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9c6-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b9c6-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-140">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="7b9c6-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="7b9c6-141">Nombre de processeurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="7b9c6-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9c6-143">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7b9c6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b9c6-145">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="7b9c6-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="7b9c6-146">Taille d’une page d’échange, en octets.</span><span class="sxs-lookup"><span data-stu-id="7b9c6-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b9c6-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b9c6-147">Requirements</span></span>



| <span data-ttu-id="7b9c6-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b9c6-148">Requirement</span></span> | <span data-ttu-id="7b9c6-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b9c6-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b9c6-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b9c6-150">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9c6-151">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b9c6-151">None supported</span></span><br/>                            |
| <span data-ttu-id="7b9c6-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b9c6-152">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9c6-153">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b9c6-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b9c6-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b9c6-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9c6-155">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="7b9c6-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




