---
description: Fournit des informations d’État pour une image de disque dur virtuel existante.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Classe Msvm_VirtualHardDiskState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484353"
---
# <a name="msvm_virtualharddiskstate-class"></a><span data-ttu-id="ef8d2-103">MSVM \_ VirtualHardDiskState, classe</span><span class="sxs-lookup"><span data-stu-id="ef8d2-103">Msvm\_VirtualHardDiskState class</span></span>

<span data-ttu-id="ef8d2-104">Fournit des informations d’État pour une image de disque dur virtuel existante.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-104">Provides state information for an existing virtual hard disk image.</span></span>

<span data-ttu-id="ef8d2-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef8d2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef8d2-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a><span data-ttu-id="ef8d2-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ef8d2-107">Members</span></span>

<span data-ttu-id="ef8d2-108">La classe **MSVM \_ VirtualHardDiskState** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ef8d2-108">The **Msvm\_VirtualHardDiskState** class has these types of members:</span></span>

-   [<span data-ttu-id="ef8d2-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef8d2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef8d2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef8d2-110">Properties</span></span>

<span data-ttu-id="ef8d2-111">La classe **MSVM \_ VirtualHardDiskState** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-111">The **Msvm\_VirtualHardDiskState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef8d2-112">**Alignment**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-112">**Alignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef8d2-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef8d2-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef8d2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef8d2-115">Spécifie le type d’alignement du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-115">Specifies the type of alignment of the virtual hard disk.</span></span> <span data-ttu-id="ef8d2-116">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-116">This will be one of the following values.</span></span>



| <span data-ttu-id="ef8d2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8d2-117">Value</span></span>                                                                        | <span data-ttu-id="ef8d2-118">Signification</span><span class="sxs-lookup"><span data-stu-id="ef8d2-118">Meaning</span></span>                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="ef8d2-119"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ef8d2-119"><dt>0</dt></span></span> </dl> | <span data-ttu-id="ef8d2-120">alignement de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-120">512 byte alignment.</span></span><br/> |
| <dl> <span data-ttu-id="ef8d2-121"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ef8d2-121"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ef8d2-122">alignement de 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-122">4 KB alignment.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="ef8d2-123">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-123">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef8d2-124">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef8d2-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef8d2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef8d2-126">Taille du fichier de disque dur virtuel (quantité réelle de stockage consommée par le fichier), en octets.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-126">The size of the virtual hard disk file (the actual amount of storage being consumed by the file), in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ef8d2-127">**FragmentationPercentage**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-127">**FragmentationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef8d2-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef8d2-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef8d2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef8d2-130">Approximation du pourcentage de blocs de disque virtuel fragmentés dans le fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-130">An approximation of the percentage of virtual disk blocks that are fragmented in the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="ef8d2-131">**Utilisées**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-131">**InUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef8d2-132">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef8d2-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef8d2-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef8d2-134">Cette propriété est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-134">This property is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="ef8d2-135">**MinInternalSize**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-135">**MinInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef8d2-136">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef8d2-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef8d2-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef8d2-138">Taille minimale d’un disque dur virtuel, en octets.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-138">The minimum size that the virtual hard disk can be shrunk to, in bytes.</span></span> <span data-ttu-id="ef8d2-139">Cette taille est arrondie au plus grand multiple de la taille de secteur suivante.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-139">This size is rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="ef8d2-140">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-140">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef8d2-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef8d2-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef8d2-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef8d2-143">Taille de secteur physique utilisée par le disque physique sous-jacent, en octets.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-143">The physical sector size used by the underlying physical disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ef8d2-144">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-144">**Timestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef8d2-145">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="ef8d2-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef8d2-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef8d2-147">Horodatage du disque dur virtuel</span><span class="sxs-lookup"><span data-stu-id="ef8d2-147">The timestamp of the virtual hard disk</span></span>

> [!Note]  
> <span data-ttu-id="ef8d2-148">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ef8d2-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef8d2-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef8d2-149">Requirements</span></span>



| <span data-ttu-id="ef8d2-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef8d2-150">Requirement</span></span> | <span data-ttu-id="ef8d2-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8d2-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8d2-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef8d2-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ef8d2-153">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef8d2-153">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef8d2-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef8d2-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ef8d2-155">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef8d2-155">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef8d2-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef8d2-156">Namespace</span></span><br/>                | <span data-ttu-id="ef8d2-157">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ef8d2-157">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef8d2-158">MOF</span><span class="sxs-lookup"><span data-stu-id="ef8d2-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef8d2-159"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef8d2-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef8d2-160">DLL</span><span class="sxs-lookup"><span data-stu-id="ef8d2-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef8d2-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef8d2-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef8d2-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef8d2-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef8d2-163">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="ef8d2-163">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




