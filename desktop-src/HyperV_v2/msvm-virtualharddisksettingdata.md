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
ms.openlocfilehash: b7f87ba072aaff03ab415ccabe803546a89192ecb1e28d85b628dd0655d47421
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068419"
---
# <a name="msvm_virtualharddisksettingdata-class"></a>MSVM \_ VirtualHardDiskSettingData, classe

Fournit des données de définition pour un disque dur virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualHardDiskSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualHardDiskSettingData** possède les propriétés suivantes.

<dl> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Taille de bloc utilisée par le disque dur virtuel, en octets.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « données de paramètre de disque dur virtuel ».

</dd> <dt>

**DataAlignment**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie l’alignement souhaité, en octets, pour la charge utile de données du disque virtuel

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « définition des données pour un disque dur virtuel ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Format**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Format du disque dur virtuel. Il s’agit de l’une des valeurs suivantes.

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span id="VHD"></span><span id="vhd"></span>**Disque dur virtuel** (2)


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)


</dt> <dd>

> [!Note]  
> ajouté dans Windows 10 et Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**IsPmemCompatible**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Spécifie si le disque virtuel peut être utilisé comme magasin de stockage pour un périphérique de mémoire persistante.

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**LogicalSectorSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Taille de secteur logique utilisée par le disque dur virtuel, en octets.

</dd> <dt>

**MaxInternalSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Taille maximale, en octets, du disque dur virtuel, tel qu’il est visible par l’ordinateur virtuel. Cette taille sera arrondie au plus grand multiple de la taille de secteur suivante.

</dd> <dt>

**ParentIdentifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

GUID utilisé pour identifier de manière unique le parent du disque dur virtuel. Si le disque dur virtuel n’a pas de parent, ce champ est vide.

> [!Note]  
> ajouté dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

**ParentPath**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Parent du disque dur virtuel. Si le disque dur virtuel n’a pas de parent, cette propriété est vide.

</dd> <dt>

**ParentTimestamp**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Horodateur du parent du disque dur virtuel. Si le disque dur virtuel n’a pas de parent, ce champ est vide.

> [!Note]  
> ajouté dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

**Chemin d’accès**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Le chemin d’accès complet du disque dur virtuel.

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Taille de secteur physique utilisée par le disque dur virtuel, en octets.

</dd> <dt>

**PmemAddressAbstractionType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Méthode d’abstraction d’adresse mémoire persistante à utiliser avec ce disque virtuel.

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (0)


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

**BTT** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Type de disque dur virtuel. Il s’agit de l’une des valeurs suivantes.

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Résolu** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

**Dynamique** (3)


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

**Différenciation** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualDiskId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

GUID utilisé pour identifier le disque virtuel de façon unique.

Lorsque la méthode [**MSVM \_ ImageManagementService. GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) retourne une instance de **MSVM \_ VirtualHardDiskSettingData**, le client peut utiliser cette propriété pour récupérer l’ID de disque unique du disque dur virtuel.

Lors de la détection de conflit ou dans le cas contraire, un client peut définir la valeur **VirtualDiskId** sur un nouveau GUID et passer cette instance **MSVM \_ VirtualHardDiskSettingData** à la méthode [**MSVM \_ ImageManagementService. SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) pour modifier l’ID de disque du disque dur virtuel. Si le disque dur virtuel n’est pas un disque dur virtuel VHDX, ou si le disque dur virtuel est attaché, l’opération échoue. L’opération échoue également si la valeur transmise est incorrecte, autrement dit, qu’il ne s’agit pas d’un GUID ou qu’il ne contient que des 0. L’opération réussit silencieusement si la valeur passée est identique à l’ID de disque actuel.

Les erreurs générées par la fonction [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) sont propagées par le biais de cette propriété. Un client peut également utiliser le même mécanisme pour fournir la valeur **VirtualDiskId** lors de la création d’un disque dur virtuel via la méthode [**MSVM \_ ImageManagementService. CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) dans le même espace de noms. Cela peut être utilisé pour créer des disques durs virtuels VHD1 ou VHD2.

**Windows 8.1 :** cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

