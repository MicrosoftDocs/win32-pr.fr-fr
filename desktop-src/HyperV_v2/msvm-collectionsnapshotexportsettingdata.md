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
ms.openlocfilehash: bd148b7ea73bf7c2eaff7f648c7084c37a8669779515749611c675e7f5564d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130629"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a>MSVM \_ CollectionSnapshotExportSettingData, classe

Exportez les données de paramètre à transmettre à la méthode temps de la classe [**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md) .

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CollectionSnapshotExportSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ CollectionSnapshotExportSettingData** possède les propriétés suivantes.

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique l’intention d’utiliser les jeux de sauvegarde exportés :

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)


</dt> <dd>

Tous les jeux de sauvegardes complets et différentiels exportés sont conservés tels quels.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)


</dt> <dd>

Les jeux de sauvegarde complète et différentielle exportés sont fusionnés pour synthétiser les jeux de sauvegarde complète.

</dd> </dl>

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, le stockage de la machine virtuelle est copié lorsque la machine virtuelle est exportée. Sinon, **false.**

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Base pour l’exportation différentielle. Il s’agit soit du chemin d’accès à une instance [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) qui représente le point de référence, soit du chemin d’accès à une instance [**\_ SnapshotCollection MSVM**](msvm-snapshotcollection.md) qui représente l’instantané à utiliser comme base pour l’exportation différentielle.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




