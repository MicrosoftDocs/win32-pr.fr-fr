---
description: Classe SystemConfig_CPU-cette classe est la classe de type d’événement pour les événements de configuration de l’UC.
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: Classe SystemConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: 07efa01bf58aeadfdfe12cd5db4d010a7f6dbca0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106117"
---
# <a name="systemconfig_cpu-class"></a><span data-ttu-id="b994d-103">\_Classe UC SystemConfig</span><span class="sxs-lookup"><span data-stu-id="b994d-103">SystemConfig\_CPU class</span></span>

<span data-ttu-id="b994d-104">Cette classe est la classe de type d’événement pour les événements de configuration de l’UC.</span><span class="sxs-lookup"><span data-stu-id="b994d-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="b994d-105">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="b994d-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b994d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b994d-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a><span data-ttu-id="b994d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b994d-107">Members</span></span>

<span data-ttu-id="b994d-108">La **classe \_ UC SystemConfig** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b994d-108">The **SystemConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="b994d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b994d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b994d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b994d-110">Properties</span></span>

<span data-ttu-id="b994d-111">La **classe \_ UC SystemConfig** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b994d-111">The **SystemConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b994d-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="b994d-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b994d-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b994d-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b994d-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b994d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b994d-115">Qualificateurs : **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="b994d-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="b994d-116">Granularité avec laquelle la mémoire virtuelle est allouée.</span><span class="sxs-lookup"><span data-stu-id="b994d-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="b994d-117">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="b994d-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b994d-118">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="b994d-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b994d-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b994d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b994d-120">Qualificateurs : **WmiDataId** (6), **Max** (256), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="b994d-120">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="b994d-121">Nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b994d-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b994d-122">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="b994d-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b994d-123">Type de données : tableau **char16**</span><span class="sxs-lookup"><span data-stu-id="b994d-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b994d-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b994d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b994d-125">Qualificateurs : **WmiDataId** (7), **Max** (132), **format ("s")**</span><span class="sxs-lookup"><span data-stu-id="b994d-125">Qualifiers: **WmiDataId** (7), **Max** (132), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="b994d-126">Nom du domaine dans lequel l’ordinateur est membre.</span><span class="sxs-lookup"><span data-stu-id="b994d-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="b994d-127">**HyperThreadingFlag**</span><span class="sxs-lookup"><span data-stu-id="b994d-127">**HyperThreadingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b994d-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b994d-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b994d-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b994d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b994d-130">Qualificateurs : **WmiDataId** (8), pointeur</span><span class="sxs-lookup"><span data-stu-id="b994d-130">Qualifiers: **WmiDataId** (8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b994d-131">Indique si l’option d’Hyper-Threading est activée ou désactivée pour un processeur.</span><span class="sxs-lookup"><span data-stu-id="b994d-131">Indicates if the hyper-threading option is on or off for a processor.</span></span> <span data-ttu-id="b994d-132">Chaque bit reflète l’état de l’Hyper-Threading d’un processeur sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b994d-132">Each bit reflects the hyper-threading state of a CPU on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b994d-133">**MemS**</span><span class="sxs-lookup"><span data-stu-id="b994d-133">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b994d-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b994d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b994d-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b994d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b994d-136">Qualificateurs : **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="b994d-136">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="b994d-137">Quantité totale de mémoire physique disponible pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b994d-137">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="b994d-138">**MHz**</span><span class="sxs-lookup"><span data-stu-id="b994d-138">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b994d-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b994d-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b994d-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b994d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b994d-141">Qualificateurs : **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="b994d-141">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="b994d-142">Vitesse maximale du processeur, en mégahertz.</span><span class="sxs-lookup"><span data-stu-id="b994d-142">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="b994d-143">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="b994d-143">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b994d-144">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b994d-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b994d-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b994d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b994d-146">Qualificateurs : **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="b994d-146">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="b994d-147">Nombre de processeurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b994d-147">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b994d-148">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="b994d-148">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b994d-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b994d-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b994d-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b994d-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b994d-151">Qualificateurs : **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="b994d-151">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="b994d-152">Taille d’une page d’échange, en octets.</span><span class="sxs-lookup"><span data-stu-id="b994d-152">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b994d-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b994d-153">Requirements</span></span>



| <span data-ttu-id="b994d-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b994d-154">Requirement</span></span> | <span data-ttu-id="b994d-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="b994d-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b994d-156">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b994d-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b994d-157">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b994d-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b994d-158">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b994d-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b994d-159">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b994d-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b994d-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b994d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b994d-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="b994d-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




