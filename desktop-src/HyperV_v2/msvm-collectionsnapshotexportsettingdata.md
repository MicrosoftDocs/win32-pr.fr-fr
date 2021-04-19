---
description: Exportez les données de paramètre à transmettre à la méthode temps de la \_ classe MSVM CollectionSnapshotService.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Classe Msvm_CollectionSnapshotExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516859"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a><span data-ttu-id="fba44-103">MSVM \_ CollectionSnapshotExportSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="fba44-103">Msvm\_CollectionSnapshotExportSettingData class</span></span>

<span data-ttu-id="fba44-104">Exportez les données de paramètre à transmettre à la méthode temps de la classe [**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fba44-104">Export setting data to be passed in to the ExportSnapshot method of [**Msvm\_CollectionSnapshotService**](msvm-collectionsnapshotservice.md) class.</span></span>

<span data-ttu-id="fba44-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fba44-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba44-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fba44-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a><span data-ttu-id="fba44-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fba44-107">Members</span></span>

<span data-ttu-id="fba44-108">La classe **MSVM \_ CollectionSnapshotExportSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fba44-108">The **Msvm\_CollectionSnapshotExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fba44-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fba44-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fba44-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fba44-110">Properties</span></span>

<span data-ttu-id="fba44-111">La classe **MSVM \_ CollectionSnapshotExportSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fba44-111">The **Msvm\_CollectionSnapshotExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fba44-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="fba44-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba44-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fba44-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fba44-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fba44-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fba44-115">Indique l’intention d’utiliser les jeux de sauvegarde exportés :</span><span class="sxs-lookup"><span data-stu-id="fba44-115">Indicates the intent how the exported backup sets would be used:</span></span>

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="fba44-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span><span class="sxs-lookup"><span data-stu-id="fba44-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fba44-117">Tous les jeux de sauvegardes complets et différentiels exportés sont conservés tels quels.</span><span class="sxs-lookup"><span data-stu-id="fba44-117">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="fba44-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span><span class="sxs-lookup"><span data-stu-id="fba44-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fba44-119">Les jeux de sauvegarde complète et différentielle exportés sont fusionnés pour synthétiser les jeux de sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="fba44-119">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fba44-120">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="fba44-120">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba44-121">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fba44-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fba44-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fba44-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fba44-123">Si la **valeur est true**, le stockage de la machine virtuelle est copié lorsque la machine virtuelle est exportée.</span><span class="sxs-lookup"><span data-stu-id="fba44-123">if **true**, the VM storage will be copied when the VM is exported.</span></span> <span data-ttu-id="fba44-124">Sinon, **false.**</span><span class="sxs-lookup"><span data-stu-id="fba44-124">Otherwise, **false.**</span></span>

</dd> <dt>

<span data-ttu-id="fba44-125">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="fba44-125">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba44-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fba44-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba44-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fba44-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fba44-128">Base pour l’exportation différentielle.</span><span class="sxs-lookup"><span data-stu-id="fba44-128">Base for differential export.</span></span> <span data-ttu-id="fba44-129">Il s’agit soit du chemin d’accès à une instance [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) qui représente le point de référence, soit du chemin d’accès à une instance [**\_ SnapshotCollection MSVM**](msvm-snapshotcollection.md) qui représente l’instantané à utiliser comme base pour l’exportation différentielle.</span><span class="sxs-lookup"><span data-stu-id="fba44-129">This is either path to an [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the reference point, or path to an [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) instance that represents the snapshot to be used as a base for differential export.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fba44-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fba44-130">Requirements</span></span>



| <span data-ttu-id="fba44-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fba44-131">Requirement</span></span> | <span data-ttu-id="fba44-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fba44-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba44-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fba44-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fba44-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fba44-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fba44-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fba44-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fba44-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fba44-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fba44-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fba44-137">Namespace</span></span><br/>                | <span data-ttu-id="fba44-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fba44-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fba44-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fba44-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fba44-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fba44-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fba44-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fba44-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba44-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fba44-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fba44-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fba44-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba44-144">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="fba44-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




