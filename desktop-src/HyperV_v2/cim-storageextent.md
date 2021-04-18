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
# <a name="cim_storageextent-class-hyper-v-management"></a>Classe CIM_StorageExtent (gestion Hyper-V)

Décrit les fonctionnalités et la gestion des médias qui stockent les données et permet la récupération des données. Cette super classe est utilisée pour représenter les composants RAID logiciels et matériels, ou une extension logique brute des supports physiques.

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe **CIM \_ StorageExtent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ StorageExtent** possède les propriétés suivantes.

<dl> <dt>

**y accéder**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de la prise en charge de la lecture/écriture du média.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**Lecture** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

**Accessible en écriture** (2)


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

**Lecture/écriture prise en charge** (3)


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

**Écriture unique** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stockage hôte DMTF \| 001,4 « , » MIB. IETF \| Host-Resources-MIB. hrStorageAllocationUnits "," MIF. \|Périphériques de stockage DMTF \| 001,5 ")
</dt> </dl>

Taille, en octets, des blocs qui forment l’extension de stockage. Si les tailles de bloc variables sont utilisées, cette propriété doit spécifier la taille de bloc maximale. Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour la **\_ AggregateExtent CIM**, la [**\_ mémoire CIM**](cim-memory.md) ou le [**\_ disque logique CIM**](cim-logicaldisk.md)), cette propriété doit être définie sur « 1 » (inconnu).

</dd> <dt>

**ConsumableBlocks**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre maximal de blocs pouvant être utilisés lors de la superposition des **\_ StorageExtent CIM** à l’aide de l’Association de classe [**CIM \_**](cim-basedon.md) . Cette propriété n’a de sens que lorsque l’extension de stockage est référencée dans la propriété **Antecedent** dans un objet **\_ basé sur CIM** .

</dd> <dt>

**DataOrganization**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type d’organisation de données utilisé par le média.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (1)


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

**Bloc fixe** (2)


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

**Bloc variable** (3)


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

**Nombre de données** de la clé (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataRedundancy**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**","**CIM \_ StorageSetting**.**DataRedundancyMax**","**CIM \_ StorageSetting**.**DataRedundancyMin**")
</dt> </dl>

Nombre total de copies de données qui sont actuellement conservées.

</dd> <dt>

**DeltaReservation**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**","**CIM \_ StorageSetting**.**DeltaReservationMax**","**CIM \_ StorageSetting**.**DeltaReservationMin**")
</dt> </dl>

Valeur actuelle pour la réservation Delta. Il s’agit d’un pourcentage qui spécifie la quantité d’espace qui doit être réservée dans un réplica pour la mise en cache des modifications.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de détection et de correction d’erreur pris en charge par l’extension de stockage.

</dd> <dt>

**ExtentStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Informations supplémentaires sur l’État.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (1)


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

**Aucun/non applicable** (2)


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

**Cassé** (3)


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

**Données perdues** (4)


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

**Reconfiguration dynamique** (5)


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

**Exposé** (6)


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

**Exposition fractionnaire** (7)


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

**Partiellement exposé** (8)


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

**Protection désactivée** (9)


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

**Prêt** (10)


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

**Régénération** (11)


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

**Recalculer** (12)


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

**Spare en cours d’utilisation** (13)


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

**Vérification en cours** (14)


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

**Accès intrabande accordé** (15)


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

**Importé** (16)


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

**Exporté** (17)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (18.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsBasedOnUnderlyingRedundancy**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**true** si les extensions de stockage sous-jacentes sont membres d’un [**\_ StorageRedundancyGroup CIM**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); sinon, **false**.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITSs-T10 \| VPD 83, identificateur d’association 0 \| ), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**","**CIM \_ StorageExtent**.**NameNamespace**")
</dt> </dl>

Identificateur unique de l’extension de stockage. La propriété **NameFormat** spécifie le format d’affectation de noms à utiliser dans la propriété **Name** .

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**","**CIM \_ StorageExtent**.**NameNamespace**","**CIM \_ StorageExtent**.**OtherNameFormat**")
</dt> </dl>

Format d’affectation de noms pour la propriété **Name** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

**VPD83NAA6** (2)


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

**VPD83NAA5** (3)


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (4)


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (5)


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

**VPD83Type0** (6)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**SNVM** (7)


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NodeWWN** (8)


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

**NAA** (9)


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

**EUI64** (10)


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

**T10VID** (11)


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**Nom du périphérique du système d’exploitation** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITSs-T10 \| VPD 83, identificateur d’association 0 \| ), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**","**CIM \_ StorageExtent**.**OtherNameNamespace**","**CIM \_ StorageExtent**.**NameFormat**»)
</dt> </dl>

Espace de noms de la propriété Name.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

**VPD83Type3** (2)


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (3)


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (4)


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

**VPD80** (5)


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NodeWWN** (6)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**SNVM** (7)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Espace de noms du périphérique du système d’exploitation** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**NoSinglePointOfFailure**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")
</dt> </dl>

**true** s’il n’existe aucun point de défaillance unique ; Sinon, **false**.

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stockage hôte DMTF \| 001,5 « , » MIB. \|Hôte IETF-ressources-MIB. hrStorageSize ")
</dt> </dl>

Nombre total de blocs contigus logiquement qui forment l’extension de stockage. La taille totale de l’extension de stockage est calculée en multipliant **BlockSize** par **NumberOfBlocks**. Si la propriété **BlockSize** a la valeur « 1 », cette propriété correspond à la taille totale de l’extension de stockage.

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**»)
</dt> </dl>

Format de la propriété **Name** lorsque la propriété **NameFormat** est définie sur « 1 » (other).

</dd> <dt>

**OtherNameNamespace**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameNamespace**")
</dt> </dl>

Description de l’espace de noms de la propriété **Name** lorsque la propriété **NameNamespace** est définie sur « 1 » (other).

</dd> <dt>

**PackageRedundancy**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**","**CIM \_ StorageSetting**.**PackageRedundancyMax**","**CIM \_ StorageSetting**.**PackageRedundancyMin**")
</dt> </dl>

Nombre actuel de packages physiques qui peuvent échouer sans perte de données. Par exemple, dans un domaine de stockage, il peut s’agir du nombre de piles de disques.

</dd> <dt>

**Primordial**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**true** si l’extension de stockage est primordiale ; Sinon, **false**.

</dd> <dt>

**Objectif**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Hôte IETF-ressources-MIB. hrStorageDescr ")
</dt> </dl>

Description de l’utilisation du support.

</dd> <dt>

**SequentialAccess**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**true** si le stockage est accessible de manière séquentielle par un objet [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) ; sinon, **false**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

