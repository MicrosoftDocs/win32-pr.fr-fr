---
description: Décrit les fonctionnalités et la gestion des médias qui stockent les données et permet la récupération des données. Cette super classe est utilisée pour représenter les composants RAID logiciels et matériels, ou une extension logique brute des supports physiques.
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: Classe CIM_StorageExtent (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.DataOrganization
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Access
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.ConsumableBlocks
- CIM_StorageExtent.IsBasedOnUnderlyingRedundancy
- CIM_StorageExtent.SequentialAccess
- CIM_StorageExtent.ExtentStatus
- CIM_StorageExtent.NoSinglePointOfFailure
- CIM_StorageExtent.DataRedundancy
- CIM_StorageExtent.PackageRedundancy
- CIM_StorageExtent.DeltaReservation
- CIM_StorageExtent.Primordial
- CIM_StorageExtent.Name
- CIM_StorageExtent.NameFormat
- CIM_StorageExtent.NameNamespace
- CIM_StorageExtent.OtherNameNamespace
- CIM_StorageExtent.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a3dc1b58dd97582e229497e754d10c3f307eab76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543116"
---
# <a name="cim_storageextent-class-hyper-v-management"></a><span data-ttu-id="8bae0-104">Classe CIM_StorageExtent (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="8bae0-104">CIM_StorageExtent class (Hyper-V management)</span></span>

<span data-ttu-id="8bae0-105">Décrit les fonctionnalités et la gestion des médias qui stockent les données et permet la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="8bae0-105">Describes the capabilities and management of media that stores data and allows retrieval of the data.</span></span> <span data-ttu-id="8bae0-106">Cette super classe est utilisée pour représenter les composants RAID logiciels et matériels, ou une extension logique brute des supports physiques.</span><span class="sxs-lookup"><span data-stu-id="8bae0-106">This super class is used to represent software and hardware RAID components, or a raw logical extent of physical media.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bae0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bae0-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.13.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
{
  uint16  DataOrganization;
  string  Purpose;
  uint16  Access;
  string  ErrorMethodology;
  uint64  BlockSize;
  uint64  NumberOfBlocks;
  uint64  ConsumableBlocks;
  boolean IsBasedOnUnderlyingRedundancy;
  boolean SequentialAccess;
  uint16  ExtentStatus[];
  boolean NoSinglePointOfFailure;
  uint16  DataRedundancy;
  uint16  PackageRedundancy;
  uint8   DeltaReservation;
  boolean Primordial = FALSE;
  string  Name;
  uint16  NameFormat;
  uint16  NameNamespace;
  string  OtherNameNamespace;
  string  OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="8bae0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8bae0-108">Members</span></span>

<span data-ttu-id="8bae0-109">La classe **CIM \_ StorageExtent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8bae0-109">The **CIM\_StorageExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="8bae0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8bae0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bae0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8bae0-111">Properties</span></span>

<span data-ttu-id="8bae0-112">La classe **CIM \_ StorageExtent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bae0-112">The **CIM\_StorageExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bae0-113">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="8bae0-113">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bae0-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-116">Description de la prise en charge de la lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="8bae0-116">A description of the read/write support of the media.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8bae0-117">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8bae0-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="8bae0-118">**Lecture** (1)</span><span class="sxs-lookup"><span data-stu-id="8bae0-118">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="8bae0-119">**Accessible en écriture** (2)</span><span class="sxs-lookup"><span data-stu-id="8bae0-119">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="8bae0-120">**Lecture/écriture prise en charge** (3)</span><span class="sxs-lookup"><span data-stu-id="8bae0-120">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="8bae0-121">**Écriture unique** (4)</span><span class="sxs-lookup"><span data-stu-id="8bae0-121">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8bae0-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="8bae0-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-123">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8bae0-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-125">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stockage hôte DMTF \| 001,4 « , » MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "," MIF. \|Périphériques de stockage DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="8bae0-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.4", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits", "MIF.DMTF\|Storage Devices\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-126">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="8bae0-126">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="8bae0-127">Si les tailles de bloc variables sont utilisées, cette propriété doit spécifier la taille de bloc maximale.</span><span class="sxs-lookup"><span data-stu-id="8bae0-127">If variable block sizes are used, then this property should specify the maximum block size.</span></span> <span data-ttu-id="8bae0-128">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour la **\_ AggregateExtent CIM**, la [**\_ mémoire CIM**](cim-memory.md) ou le [**\_ disque logique CIM**](cim-logicaldisk.md)), cette propriété doit être définie sur « 1 » (inconnu).</span><span class="sxs-lookup"><span data-stu-id="8bae0-128">If the block size is unknown or if a block concept is not valid (for example, for **CIM\_AggregateExtent**, [**CIM\_Memory**](cim-memory.md) or [**CIM\_LogicalDisk**](cim-logicaldisk.md)), then this property should be set to "1" (unknow).</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-129">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="8bae0-129">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-130">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8bae0-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-132">Nombre maximal de blocs pouvant être utilisés lors de la superposition des **\_ StorageExtent CIM** à l’aide de l’Association de classe [**CIM \_**](cim-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="8bae0-132">The maximum number of blocks, that are available for use when layering **CIM\_StorageExtent** using the [**CIM\_BasedOn**](cim-basedon.md) class association.</span></span> <span data-ttu-id="8bae0-133">Cette propriété n’a de sens que lorsque l’extension de stockage est référencée dans la propriété **Antecedent** dans un objet **\_ basé sur CIM** .</span><span class="sxs-lookup"><span data-stu-id="8bae0-133">This property only has meaning when the storage extent is referenced in the **Antecedent** property in a **CIM\_BasedOn** object.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-134">**DataOrganization**</span><span class="sxs-lookup"><span data-stu-id="8bae0-134">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bae0-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-137">Type d’organisation de données utilisé par le média.</span><span class="sxs-lookup"><span data-stu-id="8bae0-137">The type of data organization used by the media.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8bae0-138">**Autre** (0)</span><span class="sxs-lookup"><span data-stu-id="8bae0-138">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8bae0-139">**Inconnu** (1)</span><span class="sxs-lookup"><span data-stu-id="8bae0-139">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

<span data-ttu-id="8bae0-140">**Bloc fixe** (2)</span><span class="sxs-lookup"><span data-stu-id="8bae0-140">**Fixed Block** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

<span data-ttu-id="8bae0-141">**Bloc variable** (3)</span><span class="sxs-lookup"><span data-stu-id="8bae0-141">**Variable Block** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

<span data-ttu-id="8bae0-142">**Nombre de données** de la clé (4)</span><span class="sxs-lookup"><span data-stu-id="8bae0-142">**Count Key Data** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8bae0-143">**DataRedundancy**</span><span class="sxs-lookup"><span data-stu-id="8bae0-143">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bae0-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-146">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**","**CIM \_ StorageSetting**.**DataRedundancyMax**","**CIM \_ StorageSetting**.**DataRedundancyMin**")</span><span class="sxs-lookup"><span data-stu-id="8bae0-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**", "**CIM\_StorageSetting**.**DataRedundancyMax**", "**CIM\_StorageSetting**.**DataRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-147">Nombre total de copies de données qui sont actuellement conservées.</span><span class="sxs-lookup"><span data-stu-id="8bae0-147">The number of complete copies of data that are currently maintained.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-148">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="8bae0-148">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-149">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="8bae0-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-151">Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**","**CIM \_ StorageSetting**.**DeltaReservationMax**","**CIM \_ StorageSetting**.**DeltaReservationMin**")</span><span class="sxs-lookup"><span data-stu-id="8bae0-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**", "**CIM\_StorageSetting**.**DeltaReservationMax**", "**CIM\_StorageSetting**.**DeltaReservationMin**")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-152">Valeur actuelle pour la réservation Delta.</span><span class="sxs-lookup"><span data-stu-id="8bae0-152">The current value for delta reservation.</span></span> <span data-ttu-id="8bae0-153">Il s’agit d’un pourcentage qui spécifie la quantité d’espace qui doit être réservée dans un réplica pour la mise en cache des modifications.</span><span class="sxs-lookup"><span data-stu-id="8bae0-153">This is a percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="8bae0-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bae0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-157">Type de détection et de correction d’erreur pris en charge par l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="8bae0-157">The type of error detection and correction supported by the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-158">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="8bae0-158">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-159">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bae0-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-161">Informations supplémentaires sur l’État.</span><span class="sxs-lookup"><span data-stu-id="8bae0-161">Additional status information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8bae0-162">**Autre** (0)</span><span class="sxs-lookup"><span data-stu-id="8bae0-162">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8bae0-163">**Inconnu** (1)</span><span class="sxs-lookup"><span data-stu-id="8bae0-163">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

<span data-ttu-id="8bae0-164">**Aucun/non applicable** (2)</span><span class="sxs-lookup"><span data-stu-id="8bae0-164">**None/Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

<span data-ttu-id="8bae0-165">**Cassé** (3)</span><span class="sxs-lookup"><span data-stu-id="8bae0-165">**Broken** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

<span data-ttu-id="8bae0-166">**Données perdues** (4)</span><span class="sxs-lookup"><span data-stu-id="8bae0-166">**Data Lost** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

<span data-ttu-id="8bae0-167">**Reconfiguration dynamique** (5)</span><span class="sxs-lookup"><span data-stu-id="8bae0-167">**Dynamic Reconfig** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

<span data-ttu-id="8bae0-168">**Exposé** (6)</span><span class="sxs-lookup"><span data-stu-id="8bae0-168">**Exposed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

<span data-ttu-id="8bae0-169">**Exposition fractionnaire** (7)</span><span class="sxs-lookup"><span data-stu-id="8bae0-169">**Fractionally Exposed** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

<span data-ttu-id="8bae0-170">**Partiellement exposé** (8)</span><span class="sxs-lookup"><span data-stu-id="8bae0-170">**Partially Exposed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

<span data-ttu-id="8bae0-171">**Protection désactivée** (9)</span><span class="sxs-lookup"><span data-stu-id="8bae0-171">**Protection Disabled** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

<span data-ttu-id="8bae0-172">**Prêt** (10)</span><span class="sxs-lookup"><span data-stu-id="8bae0-172">**Readying** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

<span data-ttu-id="8bae0-173">**Régénération** (11)</span><span class="sxs-lookup"><span data-stu-id="8bae0-173">**Rebuild** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

<span data-ttu-id="8bae0-174">**Recalculer** (12)</span><span class="sxs-lookup"><span data-stu-id="8bae0-174">**Recalculate** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

<span data-ttu-id="8bae0-175">**Spare en cours d’utilisation** (13)</span><span class="sxs-lookup"><span data-stu-id="8bae0-175">**Spare in Use** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

<span data-ttu-id="8bae0-176">**Vérification en cours** (14)</span><span class="sxs-lookup"><span data-stu-id="8bae0-176">**Verify In Progress** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

<span data-ttu-id="8bae0-177">**Accès intrabande accordé** (15)</span><span class="sxs-lookup"><span data-stu-id="8bae0-177">**In-Band Access Granted** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

<span data-ttu-id="8bae0-178">**Importé** (16)</span><span class="sxs-lookup"><span data-stu-id="8bae0-178">**Imported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

<span data-ttu-id="8bae0-179">**Exporté** (17)</span><span class="sxs-lookup"><span data-stu-id="8bae0-179">**Exported** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8bae0-180">**DMTF réservé** (18.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8bae0-180">**DMTF Reserved** (18..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8bae0-181">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8bae0-181">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8bae0-182">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="8bae0-182">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-183">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8bae0-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-185">**true** si les extensions de stockage sous-jacentes sont membres d’un [**\_ StorageRedundancyGroup CIM**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8bae0-185">**true** if the underlying storage extents are members of a [**CIM\_StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-186">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8bae0-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bae0-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-189">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITSs-T10 \| VPD 83, identificateur d’association 0 \| ), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**","**CIM \_ StorageExtent**.**NameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="8bae0-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**", "**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-190">Identificateur unique de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="8bae0-190">A unique identifier for the storage extent.</span></span> <span data-ttu-id="8bae0-191">La propriété **NameFormat** spécifie le format d’affectation de noms à utiliser dans la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="8bae0-191">The **NameFormat** property specifies the naming format to use in the **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-192">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="8bae0-192">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-193">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bae0-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-195">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**","**CIM \_ StorageExtent**.**NameNamespace**","**CIM \_ StorageExtent**.**OtherNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="8bae0-195">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**NameNamespace**", "**CIM\_StorageExtent**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-196">Format d’affectation de noms pour la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="8bae0-196">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8bae0-197">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8bae0-197">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8bae0-198">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8bae0-198">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

<span data-ttu-id="8bae0-199">**VPD83NAA6** (2)</span><span class="sxs-lookup"><span data-stu-id="8bae0-199">**VPD83NAA6** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

<span data-ttu-id="8bae0-200">**VPD83NAA5** (3)</span><span class="sxs-lookup"><span data-stu-id="8bae0-200">**VPD83NAA5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="8bae0-201">**VPD83Type2** (4)</span><span class="sxs-lookup"><span data-stu-id="8bae0-201">**VPD83Type2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="8bae0-202">**VPD83Type1** (5)</span><span class="sxs-lookup"><span data-stu-id="8bae0-202">**VPD83Type1** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

<span data-ttu-id="8bae0-203">**VPD83Type0** (6)</span><span class="sxs-lookup"><span data-stu-id="8bae0-203">**VPD83Type0** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="8bae0-204">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="8bae0-204">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="8bae0-205">**NodeWWN** (8)</span><span class="sxs-lookup"><span data-stu-id="8bae0-205">**NodeWWN** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="8bae0-206">**NAA** (9)</span><span class="sxs-lookup"><span data-stu-id="8bae0-206">**NAA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="8bae0-207">**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="8bae0-207">**EUI64** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="8bae0-208">**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="8bae0-208">**T10VID** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="8bae0-209">**Nom du périphérique du système d’exploitation** (12)</span><span class="sxs-lookup"><span data-stu-id="8bae0-209">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8bae0-210">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="8bae0-210">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-211">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bae0-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-213">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITSs-T10 \| VPD 83, identificateur d’association 0 \| ), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**","**CIM \_ StorageExtent**.**OtherNameNamespace**","**CIM \_ StorageExtent**.**NameFormat**»)</span><span class="sxs-lookup"><span data-stu-id="8bae0-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**OtherNameNamespace**", "**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-214">Espace de noms de la propriété Name.</span><span class="sxs-lookup"><span data-stu-id="8bae0-214">The namespace of the name property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8bae0-215">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8bae0-215">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8bae0-216">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8bae0-216">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="8bae0-217">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="8bae0-217">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="8bae0-218">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="8bae0-218">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="8bae0-219">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="8bae0-219">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="8bae0-220">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="8bae0-220">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="8bae0-221">**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="8bae0-221">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="8bae0-222">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="8bae0-222">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="8bae0-223">**Espace de noms du périphérique du système d’exploitation** (8)</span><span class="sxs-lookup"><span data-stu-id="8bae0-223">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8bae0-224">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="8bae0-224">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-225">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8bae0-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-227">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span><span class="sxs-lookup"><span data-stu-id="8bae0-227">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-228">**true** s’il n’existe aucun point de défaillance unique ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8bae0-228">**true** if there are not any single points of failure; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-229">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="8bae0-229">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-230">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8bae0-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-232">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stockage hôte DMTF \| 001,5 « , » MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="8bae0-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-233">Nombre total de blocs contigus logiquement qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="8bae0-233">The total number of logically contiguous blocks that form the storage extent.</span></span> <span data-ttu-id="8bae0-234">La taille totale de l’extension de stockage est calculée en multipliant **BlockSize** par **NumberOfBlocks**.</span><span class="sxs-lookup"><span data-stu-id="8bae0-234">The total size of the storage extent is calculated by multiplying **BlockSize** by **NumberOfBlocks**.</span></span> <span data-ttu-id="8bae0-235">Si la propriété **BlockSize** a la valeur « 1 », cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="8bae0-235">If the **BlockSize** is "1", this property is the total size of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-236">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="8bae0-236">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bae0-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-239">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**»)</span><span class="sxs-lookup"><span data-stu-id="8bae0-239">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-240">Format de la propriété **Name** lorsque la propriété **NameFormat** est définie sur « 1 » (other).</span><span class="sxs-lookup"><span data-stu-id="8bae0-240">The format of the **Name** property when the **NameFormat** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-241">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="8bae0-241">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bae0-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-244">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="8bae0-244">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-245">Description de l’espace de noms de la propriété **Name** lorsque la propriété **NameNamespace** est définie sur « 1 » (other).</span><span class="sxs-lookup"><span data-stu-id="8bae0-245">A description of the namespace of the **Name** property when the **NameNamespace** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-246">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="8bae0-246">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-247">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8bae0-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-249">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**","**CIM \_ StorageSetting**.**PackageRedundancyMax**","**CIM \_ StorageSetting**.**PackageRedundancyMin**")</span><span class="sxs-lookup"><span data-stu-id="8bae0-249">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**", "**CIM\_StorageSetting**.**PackageRedundancyMax**", "**CIM\_StorageSetting**.**PackageRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-250">Nombre actuel de packages physiques qui peuvent échouer sans perte de données.</span><span class="sxs-lookup"><span data-stu-id="8bae0-250">The current number of physical packages that can fail without data loss.</span></span> <span data-ttu-id="8bae0-251">Par exemple, dans un domaine de stockage, il peut s’agir du nombre de piles de disques.</span><span class="sxs-lookup"><span data-stu-id="8bae0-251">For example, in a storage domain, this might be the number of disk spindles.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-252">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="8bae0-252">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-253">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8bae0-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-255">**true** si l’extension de stockage est primordiale ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8bae0-255">**true** if the storage extent is primordial; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-256">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="8bae0-256">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8bae0-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-259">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageDescr ")</span><span class="sxs-lookup"><span data-stu-id="8bae0-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageDescr")</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-260">Description de l’utilisation du support.</span><span class="sxs-lookup"><span data-stu-id="8bae0-260">A description of the media usage.</span></span>

</dd> <dt>

<span data-ttu-id="8bae0-261">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="8bae0-261">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bae0-262">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8bae0-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8bae0-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8bae0-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bae0-264">**true** si le stockage est accessible de manière séquentielle par un objet [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) ; sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8bae0-264">**true** if storage is sequentially accessed by a [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) object; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bae0-265">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bae0-265">Requirements</span></span>



| <span data-ttu-id="8bae0-266">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bae0-266">Requirement</span></span> | <span data-ttu-id="8bae0-267">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bae0-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bae0-268">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bae0-268">Minimum supported client</span></span><br/> | <span data-ttu-id="8bae0-269">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8bae0-269">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8bae0-270">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8bae0-270">Minimum supported server</span></span><br/> | <span data-ttu-id="8bae0-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8bae0-271">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8bae0-272">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8bae0-272">Namespace</span></span><br/>                | <span data-ttu-id="8bae0-273">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8bae0-273">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8bae0-274">MOF</span><span class="sxs-lookup"><span data-stu-id="8bae0-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bae0-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bae0-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bae0-276">DLL</span><span class="sxs-lookup"><span data-stu-id="8bae0-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bae0-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8bae0-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8bae0-278">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bae0-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bae0-279">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8bae0-279">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

