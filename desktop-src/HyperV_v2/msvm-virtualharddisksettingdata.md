---
description: Fournit des données de définition pour un disque dur virtuel.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Classe Msvm_VirtualHardDiskSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112294"
---
# <a name="msvm_virtualharddisksettingdata-class"></a><span data-ttu-id="27c2a-103">MSVM \_ VirtualHardDiskSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="27c2a-103">Msvm\_VirtualHardDiskSettingData class</span></span>

<span data-ttu-id="27c2a-104">Fournit des données de définition pour un disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-104">Provides setting data for a virtual hard disk.</span></span>

<span data-ttu-id="27c2a-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="27c2a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c2a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27c2a-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a><span data-ttu-id="27c2a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="27c2a-107">Members</span></span>

<span data-ttu-id="27c2a-108">La classe **MSVM \_ VirtualHardDiskSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="27c2a-108">The **Msvm\_VirtualHardDiskSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="27c2a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="27c2a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27c2a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="27c2a-110">Properties</span></span>

<span data-ttu-id="27c2a-111">La classe **MSVM \_ VirtualHardDiskSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="27c2a-111">The **Msvm\_VirtualHardDiskSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27c2a-112">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="27c2a-112">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-113">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27c2a-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-115">Taille de bloc utilisée par le disque dur virtuel, en octets.</span><span class="sxs-lookup"><span data-stu-id="27c2a-115">The block size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="27c2a-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27c2a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27c2a-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-119">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="27c2a-119">A short description of the object.</span></span> <span data-ttu-id="27c2a-120">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « données de paramètre de disque dur virtuel ».</span><span class="sxs-lookup"><span data-stu-id="27c2a-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Hard Disk Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-121">**DataAlignment**</span><span class="sxs-lookup"><span data-stu-id="27c2a-121">**DataAlignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-122">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27c2a-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-124">Spécifie l’alignement souhaité, en octets, pour la charge utile de données du disque virtuel</span><span class="sxs-lookup"><span data-stu-id="27c2a-124">Specifies the desired alignment, in bytes, for the data payload of the virtual disk</span></span>

> [!Note]  
> <span data-ttu-id="27c2a-125">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="27c2a-125">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="27c2a-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="27c2a-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27c2a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27c2a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-129">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="27c2a-129">A description of the object.</span></span> <span data-ttu-id="27c2a-130">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « définition des données pour un disque dur virtuel ».</span><span class="sxs-lookup"><span data-stu-id="27c2a-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Setting Data for a Virtual Hard Disk".</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="27c2a-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27c2a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27c2a-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-134">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="27c2a-134">A display name for the object.</span></span> <span data-ttu-id="27c2a-135">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="27c2a-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-136">**Format**</span><span class="sxs-lookup"><span data-stu-id="27c2a-136">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-137">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27c2a-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-139">Format du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-139">The format for the virtual hard disk.</span></span> <span data-ttu-id="27c2a-140">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="27c2a-140">This will be one of the following values.</span></span>

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span data-ttu-id="27c2a-141"><span id="VHD"></span><span id="vhd"></span>**Disque dur virtuel** (2)</span><span class="sxs-lookup"><span data-stu-id="27c2a-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span data-ttu-id="27c2a-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span><span class="sxs-lookup"><span data-stu-id="27c2a-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span data-ttu-id="27c2a-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span><span class="sxs-lookup"><span data-stu-id="27c2a-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="27c2a-144">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="27c2a-144">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27c2a-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="27c2a-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27c2a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27c2a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-148">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="27c2a-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-149">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="27c2a-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="27c2a-150">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="27c2a-150">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-151">**IsPmemCompatible**</span><span class="sxs-lookup"><span data-stu-id="27c2a-151">**IsPmemCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-152">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="27c2a-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-154">Spécifie si le disque virtuel peut être utilisé comme magasin de stockage pour un périphérique de mémoire persistante.</span><span class="sxs-lookup"><span data-stu-id="27c2a-154">Specifies whether the virtual disk can be used as the backing store for a persistent memory device.</span></span>

> [!Note]  
> <span data-ttu-id="27c2a-155">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="27c2a-155">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="27c2a-156">**LogicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="27c2a-156">**LogicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27c2a-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-159">Taille de secteur logique utilisée par le disque dur virtuel, en octets.</span><span class="sxs-lookup"><span data-stu-id="27c2a-159">The logical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-160">**MaxInternalSize**</span><span class="sxs-lookup"><span data-stu-id="27c2a-160">**MaxInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-161">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="27c2a-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-162">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-163">Taille maximale, en octets, du disque dur virtuel, tel qu’il est visible par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-163">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="27c2a-164">Cette taille sera arrondie au plus grand multiple de la taille de secteur suivante.</span><span class="sxs-lookup"><span data-stu-id="27c2a-164">This size will be rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-165">**ParentIdentifier**</span><span class="sxs-lookup"><span data-stu-id="27c2a-165">**ParentIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27c2a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27c2a-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-168">GUID utilisé pour identifier de manière unique le parent du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-168">The GUID used to uniquely identify the parent of the virtual hard disk.</span></span> <span data-ttu-id="27c2a-169">Si le disque dur virtuel n’a pas de parent, ce champ est vide.</span><span class="sxs-lookup"><span data-stu-id="27c2a-169">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="27c2a-170">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="27c2a-170">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="27c2a-171">**ParentPath**</span><span class="sxs-lookup"><span data-stu-id="27c2a-171">**ParentPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27c2a-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-174">Parent du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-174">The parent of the virtual hard disk.</span></span> <span data-ttu-id="27c2a-175">Si le disque dur virtuel n’a pas de parent, cette propriété est vide.</span><span class="sxs-lookup"><span data-stu-id="27c2a-175">If the virtual hard disk does not have a parent, then this property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-176">**ParentTimestamp**</span><span class="sxs-lookup"><span data-stu-id="27c2a-176">**ParentTimestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-177">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="27c2a-177">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27c2a-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-179">Horodateur du parent du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-179">The timestamp of the parent of the virtual hard disk.</span></span> <span data-ttu-id="27c2a-180">Si le disque dur virtuel n’a pas de parent, ce champ est vide.</span><span class="sxs-lookup"><span data-stu-id="27c2a-180">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="27c2a-181">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="27c2a-181">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="27c2a-182">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="27c2a-182">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27c2a-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-185">Le chemin d’accès complet du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-185">The fully qualified path of the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-186">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="27c2a-186">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-187">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27c2a-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-188">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-189">Taille de secteur physique utilisée par le disque dur virtuel, en octets.</span><span class="sxs-lookup"><span data-stu-id="27c2a-189">The physical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="27c2a-190">**PmemAddressAbstractionType**</span><span class="sxs-lookup"><span data-stu-id="27c2a-190">**PmemAddressAbstractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-191">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27c2a-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-192">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-193">Méthode d’abstraction d’adresse mémoire persistante à utiliser avec ce disque virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-193">The persistent memory address abstraction method to be used with this virtual disk.</span></span>

> [!Note]  
> <span data-ttu-id="27c2a-194">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="27c2a-194">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="27c2a-195">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="27c2a-195">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

<span data-ttu-id="27c2a-196">**BTT** (1)</span><span class="sxs-lookup"><span data-stu-id="27c2a-196">**BTT** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27c2a-197">**Inconnu** (65535)</span><span class="sxs-lookup"><span data-stu-id="27c2a-197">**Unknown** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27c2a-198">**Type**</span><span class="sxs-lookup"><span data-stu-id="27c2a-198">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-199">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27c2a-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-200">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-201">Type de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-201">The type of virtual hard disk.</span></span> <span data-ttu-id="27c2a-202">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="27c2a-202">This will be one of the following values.</span></span>

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="27c2a-203">**Résolu** (2)</span><span class="sxs-lookup"><span data-stu-id="27c2a-203">**Fixed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

<span data-ttu-id="27c2a-204">**Dynamique** (3)</span><span class="sxs-lookup"><span data-stu-id="27c2a-204">**Dynamic** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

<span data-ttu-id="27c2a-205">**Différenciation** (4)</span><span class="sxs-lookup"><span data-stu-id="27c2a-205">**Differencing** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27c2a-206">**VirtualDiskId**</span><span class="sxs-lookup"><span data-stu-id="27c2a-206">**VirtualDiskId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c2a-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="27c2a-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27c2a-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="27c2a-208">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27c2a-209">GUID utilisé pour identifier le disque virtuel de façon unique.</span><span class="sxs-lookup"><span data-stu-id="27c2a-209">The GUID that is used to uniquely identify the virtual disk.</span></span>

<span data-ttu-id="27c2a-210">Lorsque la méthode [**MSVM \_ ImageManagementService. GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) retourne une instance de **MSVM \_ VirtualHardDiskSettingData**, le client peut utiliser cette propriété pour récupérer l’ID de disque unique du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-210">When the [**Msvm\_ImageManagementService.GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) method returns an instance of **Msvm\_VirtualHardDiskSettingData**, the client can use this property to get the unique disk ID of the VHD.</span></span>

<span data-ttu-id="27c2a-211">Lors de la détection de conflit ou dans le cas contraire, un client peut définir la valeur **VirtualDiskId** sur un nouveau GUID et passer cette instance **MSVM \_ VirtualHardDiskSettingData** à la méthode [**MSVM \_ ImageManagementService. SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) pour modifier l’ID de disque du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-211">On conflict detection or otherwise, a client can set the **VirtualDiskId** value to a new GUID and pass this **Msvm\_VirtualHardDiskSettingData** instance to the [**Msvm\_ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) method to change the disk ID of the VHD.</span></span> <span data-ttu-id="27c2a-212">Si le disque dur virtuel n’est pas un disque dur virtuel VHDX, ou si le disque dur virtuel est attaché, l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="27c2a-212">If the VHD is not a VHDX VHD, or if the VHD is attached, the operation fails.</span></span> <span data-ttu-id="27c2a-213">L’opération échoue également si la valeur transmise est incorrecte, autrement dit, qu’il ne s’agit pas d’un GUID ou qu’il ne contient que des 0.</span><span class="sxs-lookup"><span data-stu-id="27c2a-213">The operation also fails if the passed value is malformed, that is, not a GUID or has all 0s.</span></span> <span data-ttu-id="27c2a-214">L’opération réussit silencieusement si la valeur passée est identique à l’ID de disque actuel.</span><span class="sxs-lookup"><span data-stu-id="27c2a-214">The operation silently succeeds if the passed value is the same as the current disk ID.</span></span>

<span data-ttu-id="27c2a-215">Les erreurs générées par la fonction [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) sont propagées par le biais de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="27c2a-215">Errors generated by the [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) function are bubbled up through this property.</span></span> <span data-ttu-id="27c2a-216">Un client peut également utiliser le même mécanisme pour fournir la valeur **VirtualDiskId** lors de la création d’un disque dur virtuel via la méthode [**MSVM \_ ImageManagementService. CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) dans le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="27c2a-216">A client can also use the same mechanism to provide the **VirtualDiskId** value at VHD creation via the [**Msvm\_ImageManagementService.CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) method in the same namespace.</span></span> <span data-ttu-id="27c2a-217">Cela peut être utilisé pour créer des disques durs virtuels VHD1 ou VHD2.</span><span class="sxs-lookup"><span data-stu-id="27c2a-217">This can be used to create VHD1 or VHD2 VHDs.</span></span>

<span data-ttu-id="27c2a-218">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="27c2a-218">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27c2a-219">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27c2a-219">Requirements</span></span>



| <span data-ttu-id="27c2a-220">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27c2a-220">Requirement</span></span> | <span data-ttu-id="27c2a-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="27c2a-221">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27c2a-222">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27c2a-222">Minimum supported client</span></span><br/> | <span data-ttu-id="27c2a-223">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27c2a-223">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="27c2a-224">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27c2a-224">Minimum supported server</span></span><br/> | <span data-ttu-id="27c2a-225">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27c2a-225">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27c2a-226">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="27c2a-226">Namespace</span></span><br/>                | <span data-ttu-id="27c2a-227">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="27c2a-227">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="27c2a-228">MOF</span><span class="sxs-lookup"><span data-stu-id="27c2a-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27c2a-229"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27c2a-229"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="27c2a-230">DLL</span><span class="sxs-lookup"><span data-stu-id="27c2a-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27c2a-231"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="27c2a-231"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="27c2a-232">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27c2a-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c2a-233">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="27c2a-233">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="27c2a-234">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="27c2a-234">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

