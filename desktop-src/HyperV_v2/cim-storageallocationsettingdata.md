---
description: Représente les paramètres pour l’allocation de stockage virtuel.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: CIM_StorageAllocationSettingData, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe380b03daced6ca98a44c189c52b5842862aa2e033bf66a04f8dd1466968449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899669"
---
# <a name="cim_storageallocationsettingdata-class"></a>\_Classe CIM StorageAllocationSettingData

Représente les paramètres pour l’allocation de stockage virtuel.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ StorageAllocationSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ StorageAllocationSettingData** possède les propriétés suivantes.

<dl> <dt>

**y accéder**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Accès**»)
</dt> </dl>

Prise en charge en lecture/écriture de l’allocation de stockage.

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

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Name**»)
</dt> </dl>

Identificateur unique de l’étendue de stockage hôte.

</dd> <dt>

**HostExtentNameFormat**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**»)
</dt> </dl>

Format de la valeur de la propriété **HostExtentName** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)


</dt> <dd>

Numéro de série/fournisseur/modèle (SNVM) SNVM est 3 chaînes représentant le nom du fournisseur, le nom du produit dans l’espace de noms du fournisseur et le numéro de série dans l’espace de noms du modèle. Les chaînes sont délimitées par un' + '. Les espaces peuvent être inclus et significatifs. Le numéro de série est la représentation textuelle du numéro de série en majuscules hexadécimales. Cela représente le fournisseur et l’ID de modèle des données de recherche SCSI ; le champ Vendor doit avoir une largeur de 8 caractères et le champ Product doit avoir une largeur de 16 caractères. Par exemple,

« Acme \_ \_ \_ \_ + Super Disk \_ \_ \_ \_ \_ \_ + 124437458 » ( \_ est un espace)

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span id="NAA"></span><span id="naa"></span>**NAA** (9)


</dt> <dd>

9 = NAA comme format générique. Consultez

https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html. Mise en forme en tant que 16 ou 32 caractères hexadécimaux non séparés (2 par octet binaire).

Par exemple, ' 21000020372D3C73 '

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)


</dt> <dd>

EUI comme format générique (EUI64) consultez

https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)


</dt> <dd>

Format d’identificateur de fournisseur T10 tel qu’il est retourné par la page d’interrogation SCSI 83, type d’identificateur 1. Consultez la spécification de T10 SPC-3. Il s’agit de l’ID de fournisseur ASCII de 8 octets du registre de T10 suivi d’un identificateur ASCII spécifique au fournisseur ; les espaces sont autorisés. Pour les volumes non-SCSI, « SNVM » peut être le choix le plus approprié.

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nom du périphérique du système d’exploitation** (12)


</dt> <dd>

Nom du périphérique du système d’exploitation (pour LogicalDisks). Pour plus d’informations, consultez Description du nom de disque logique.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Espace de noms**»)
</dt> </dl>

Format d’affectation de noms pour la propriété **Name** .

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


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentStartingAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**","[**CIM \_ BasedOn**](cim-basedon.md).**** De l’un des»)
</dt> </dl>

Adresse de départ sur l’étendue de stockage de l’hôte. Valeur NULL ; UE indique qu’il n’existe pas de mappage direct entre l’extension de stockage virtuel et l’extension de stockage hôte.

</dd> <dt>

**HostResourceBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Blocksize**"), **punitif** (" Byte ")
</dt> </dl>

Taille, en octets, des blocs alloués sur l’hôte pour l’allocation de stockage. Si la taille de bloc est variable, la taille de bloc maximale en octets doit être spécifiée. Si la taille de bloc est inconnue ou si aucun concept de bloc ne s’applique, la valeur « 1 » (inconnu) doit être utilisée.

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

Nombre maximal de blocs qui seront accordés pour l’allocation des ressources de stockage sur l’ordinateur hôte. La taille de bloc est spécifiée par la propriété **HostResourceBlockSize** .

</dd> <dt>

**OtherHostExtentNameFormat**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**")
</dt> </dl>

Format de la propriété **HostExtentName** si la propriété a la valeur « 1 » (autre).

</dd> <dt>

**OtherHostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**")
</dt> </dl>

Chaîne qui décrit l’espace de noms de la propriété **HostExtentName** si la valeur de la propriété **HostExtentNameNamespace** est « 1 » (other).

</dd> <dt>

**Réservation**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

Quantité de blocs dont la disponibilité est garantie pour l’allocation des ressources de stockage sur l’ordinateur hôte. La taille de bloc est spécifiée par la propriété **HostResourceBlockSize** .

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**NumberOfBlocks**","**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**")
</dt> </dl>

Nombre de blocs que l’allocation de stockage présente au consommateur.

> [!Note]  
> La propriété **VirtualQuantity** peut spécifier une taille de bloc de « 1 », même si **VirtualResourceBlockSize** est inconnu.

 

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**
</dt> </dl>

Unités utilisées par la propriété **VirtualQuantity** . Cette valeur doit être définie sur « nombre (bloc de taille fixe) » ou « octet ». La valeur par défaut, « nombre (bloc de taille fixe) » doit être utilisée pour une taille de bloc fixe, et « octet » doit être utilisé pour une taille de bloc inconnue ou variable.

</dd> <dt>

**VirtualResourceBlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Blocksize**"), **punitif** (" Byte ")
</dt> </dl>

Taille, en octets, des blocs qui forment la demande d’allocation de stockage. Si la taille de bloc est variable, la taille de bloc maximale doit être spécifiée. Si la taille de bloc est inconnue ou si aucun concept de bloc ne s’applique, la taille de bloc doit être « 1 » (inconnu).

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

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

