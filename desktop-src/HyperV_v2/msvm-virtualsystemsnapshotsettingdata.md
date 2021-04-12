---
description: Fournit des informations supplémentaires à utiliser avec la méthode CreateSnapshot de la \_ classe VirtualSystemSnapshotService MSVM.
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Classe Msvm_VirtualSystemSnapshotSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32ab52da97e9fcc943c3a70548bb6b1a6d7994a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393419"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a><span data-ttu-id="58c21-103">MSVM \_ VirtualSystemSnapshotSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="58c21-103">Msvm\_VirtualSystemSnapshotSettingData class</span></span>

<span data-ttu-id="58c21-104">Fournit des informations supplémentaires à utiliser avec la méthode [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) de la [**classe \_ VirtualSystemSnapshotService MSVM**](msvm-virtualsystemsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="58c21-104">Provides additional information to be used with the [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) method of the [**Msvm\_VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) class.</span></span>

<span data-ttu-id="58c21-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="58c21-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c21-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58c21-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a><span data-ttu-id="58c21-107">Membres</span><span class="sxs-lookup"><span data-stu-id="58c21-107">Members</span></span>

<span data-ttu-id="58c21-108">La classe **MSVM \_ VirtualSystemSnapshotSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="58c21-108">The **Msvm\_VirtualSystemSnapshotSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="58c21-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="58c21-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58c21-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="58c21-110">Properties</span></span>

<span data-ttu-id="58c21-111">La classe **MSVM \_ VirtualSystemSnapshotSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="58c21-111">The **Msvm\_VirtualSystemSnapshotSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58c21-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="58c21-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58c21-113">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="58c21-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="58c21-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58c21-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58c21-115">Niveau de cohérence de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="58c21-115">The consistency level of the snapshot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="58c21-116">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="58c21-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="58c21-117">**Cohérence des applications** (1)</span><span class="sxs-lookup"><span data-stu-id="58c21-117">**Application Consistent** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="58c21-118">**Cohérence des incidents** (2)</span><span class="sxs-lookup"><span data-stu-id="58c21-118">**Crash Consistent** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58c21-119">**GuestBackupType**</span><span class="sxs-lookup"><span data-stu-id="58c21-119">**GuestBackupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58c21-120">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="58c21-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="58c21-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58c21-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58c21-122">Type de sauvegarde à utiliser au sein de l’invité.</span><span class="sxs-lookup"><span data-stu-id="58c21-122">Backup type to be used inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="58c21-123">Propriété ajoutée dans Windows 10, version 1703</span><span class="sxs-lookup"><span data-stu-id="58c21-123">Property added in Windows 10, version 1703</span></span>

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="58c21-124">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="58c21-124">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="58c21-125">**Complète** (1)</span><span class="sxs-lookup"><span data-stu-id="58c21-125">**Full** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="58c21-126">**Copier** (2)</span><span class="sxs-lookup"><span data-stu-id="58c21-126">**Copy** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="58c21-127">**IgnoreNonSnapshottableDisks**</span><span class="sxs-lookup"><span data-stu-id="58c21-127">**IgnoreNonSnapshottableDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58c21-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="58c21-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58c21-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58c21-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58c21-130">Spécifie si des disques non snapshottable comme les disques relais et les disques Fibre Channel doivent être ignorés lors de la création de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="58c21-130">Specifies if non-snapshottable disks like passthrough disks and Fibre Channel Disks are to be ignored while creating the snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58c21-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58c21-131">Requirements</span></span>



| <span data-ttu-id="58c21-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58c21-132">Requirement</span></span> | <span data-ttu-id="58c21-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="58c21-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c21-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58c21-134">Minimum supported client</span></span><br/> | <span data-ttu-id="58c21-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58c21-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="58c21-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58c21-136">Minimum supported server</span></span><br/> | <span data-ttu-id="58c21-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="58c21-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="58c21-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="58c21-138">Namespace</span></span><br/>                | <span data-ttu-id="58c21-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="58c21-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="58c21-140">MOF</span><span class="sxs-lookup"><span data-stu-id="58c21-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58c21-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58c21-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58c21-142">DLL</span><span class="sxs-lookup"><span data-stu-id="58c21-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58c21-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58c21-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58c21-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58c21-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c21-145">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="58c21-145">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




