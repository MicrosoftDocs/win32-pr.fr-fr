---
description: Représente le réseau sur lequel le service de migration de système virtuel écoute la migration du système virtuel entrant.
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Classe Msvm_VirtualSystemMigrationNetworkSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 176e7c46bcb2cf69149b6ce7524a841cf5e072e5d21f9d6f4247c795c839c0f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963549"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a>MSVM \_ VirtualSystemMigrationNetworkSettingData, classe

Représente le réseau sur lequel le service de migration de système virtuel écoute la migration du système virtuel entrant.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemMigrationNetworkSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemMigrationNetworkSettingData** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Mesure**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Mesure de priorité de ce réseau pour la migration. Les valeurs les plus basses sont prioritaires.

</dd> <dt>

**PrefixLength**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Longueur du préfixe du sous-réseau de la migration.

</dd> <dt>

**SubnetNumber**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de sous-réseau de la migration.

</dd> <dt>

**Balises**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de balises permettant de représenter le système de gestion qui a défini ce réseau pour le service de migration de système virtuel.

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

[**ModifyNetworkSettings**](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

