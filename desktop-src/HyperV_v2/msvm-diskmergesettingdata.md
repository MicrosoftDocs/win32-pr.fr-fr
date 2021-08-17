---
description: Représente l’état de configuration des paramètres de fusion de disque pour un ordinateur virtuel.
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Classe Msvm_DiskMergeSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 825653d643a3f9eb4cf08354edc12e825ae856fc64fb6181f01d04172b393a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431009"
---
# <a name="msvm_diskmergesettingdata-class"></a>MSVM \_ DiskMergeSettingData, classe

Représente l’état de configuration des paramètres de fusion de disque pour un ordinateur virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ DiskMergeSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ DiskMergeSettingData** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) et a toujours la valeur « données de paramètre de fusion sur disque ».

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « données de paramètre de fusion de disque Microsoft ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))et est toujours définie sur « données de paramètre de fusion sur disque ». La modification de cette propriété entraînera la modification de la propriété **ElementName** de la dérivée [**CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) associée.

Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’état activé de la fonctionnalité de fusion de disque.

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

**Désactivé temporairement** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Activé** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) et est toujours définie sur « Microsoft :*GUID* \\ *DeviceSpecificData*».

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

