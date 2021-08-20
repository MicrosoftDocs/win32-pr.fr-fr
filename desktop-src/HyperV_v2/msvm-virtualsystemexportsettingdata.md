---
description: Fournit des informations supplémentaires à utiliser avec la méthode ExportSystemDefinition de la \_ classe VirtualSystemManagementService MSVM.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Classe Msvm_VirtualSystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6760fb671e9e06ea603f86c944cf45a8637d1a811a8c8a0743946a88f25d5a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810494"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a>MSVM \_ VirtualSystemExportSettingData, classe

Fournit des informations supplémentaires à utiliser avec la méthode [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) de la [**classe \_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) .

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemExportSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemExportSettingData** possède les propriétés suivantes.

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique l’intention d’utiliser les jeux de sauvegarde exportés.

> [!Note]  
> cette propriété a été ajoutée dans Windows 10 et Windows Server 2016.

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)


</dt> <dd>

Tous les jeux de sauvegardes complets et différentiels exportés sont conservés tels quels.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)


</dt> <dd>

Les jeux de sauvegarde complète et différentielle exportés sont fusionnés pour synthétiser les jeux de sauvegarde complète.

</dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CaptureLiveState**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique l’État à capturer si la cible de l’exportation est une machine virtuelle en cours d’exécution.

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)


</dt> <dd>

Aucun fichier d’état enregistré ne sera exporté pour l’ordinateur virtuel en cours d’exécution, en le plaçant dans un état de cohérence en cas d’incident.

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)


</dt> <dd>

Les fichiers d’État enregistrés pour la machine virtuelle en cours d’exécution seront exportés en même temps que la configuration de la machine virtuelle.

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)


</dt> <dd>

L’état de cohérence des applications de la machine virtuelle en cours d’exécution sera exporté.

> [!Note]  
> ajouté dans Windows 10 et Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopySnapshotConfiguration**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique les captures instantanées à exporter avec la machine virtuelle.

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)


</dt> <dd>

Toutes les captures instantanées sont exportées avec la machine virtuelle.

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)


</dt> <dd>

Aucune capture instantanée n’est exportée avec la machine virtuelle.

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)


</dt> <dd>

Les instantanés identifiés par la propriété **SnapshotVirtualSystem** sont exportés avec l’ordinateur virtuel. Les propriétés **CopyVmStorage** et **CopyVmRuntimeInformation** sont ignorées, les informations de stockage et d’exécution sont exportées avec la machine virtuelle et tous les disques de différenciation VHD sont fusionnés dans un nouveau disque dur virtuel.

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)


</dt> <dd>

L’instantané identifié par la propriété **SnapshotVirtualSystem** sera exporté à des fins de sauvegarde de la machine virtuelle. La configuration exportée utilise l’ID de la machine virtuelle.

> [!Note]  
> ajouté dans Windows 10 et Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopyVmRuntimeInformation**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si les informations d’exécution de la machine virtuelle seront copiées lors de l’exportation de l’ordinateur virtuel.



| Valeur                                                                                | Signification                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Les informations d’exécution de la machine virtuelle seront copiées.<br/>     |
| <dl> <dt>**Faux**</dt> </dl> | Les informations d’exécution de l’ordinateur virtuel ne seront pas copiées.<br/> |



 

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si le stockage de l’ordinateur virtuel sera copié lors de l’exportation de l’ordinateur virtuel.



| Valeur                                                                                | Signification                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Le stockage de l’ordinateur virtuel sera copié.<br/>     |
| <dl> <dt>**Faux**</dt> </dl> | Le stockage de l’ordinateur virtuel ne sera pas copié.<br/> |



 

</dd> <dt>

**CreateVmExportSubdirectory**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si un sous-répertoire avec le nom de l’ordinateur virtuel sera créé lors de l’exportation de l’ordinateur virtuel.



| Valeur                                                                                | Signification                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**Vrai**</dt> </dl>  | Un sous-répertoire est créé.<br/>     |
| <dl> <dt>**Faux**</dt> </dl> | Un sous-répertoire ne sera pas créé.<br/> |



 

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Base pour l’exportation différentielle. Il s’agit de l’un des chemins d’accès à une instance [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) qui représente le point de référence ou le chemin d’accès à une instance [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) qui représente l’instantané à utiliser comme base pour l’exportation différentielle. Si la propriété **CopySnapshotConfiguration** n’a pas la valeur 3 (**ExportOneSnapshotForBackup**), cette propriété est ignorée.

> [!Note]  
> ajouté dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

**DisableDifferentialOfIgnoredStorage**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si les disques de différenciation seront créés ou non pour le stockage ignoré pendant l’exportation. Par défaut, cette valeur est définie sur false, ce qui signifie que les disques de différenciation sont créés pour le stockage qui ne va pas être copié vers la destination d’exportation.

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de cette instance. En outre, le nom complet peut être utilisé comme propriété d’index pour une recherche ou une requête. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**ExcludedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Tableau d’ID d’instance [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) (RASD) qui représentent les disques durs virtuels qui doivent être exclus de l’opération d’exportation. Si au moins un des ID fournis n’est pas un disque dur virtuel attaché valide, l’opération échoue.

Les disques durs virtuels référencés par cette propriété peuvent provenir de la machine virtuelle et/ou de l’un de ses instantanés. L’exclusion de disques durs virtuels n’est pas prise en charge lorsque la propriété **CopySnapshotConfiguration** est définie sur 0 (ExportAllSnapshots).

Notez que l’ID d’instance RASD pour les disques durs virtuels représente l’emplacement auquel ils sont attachés, et l’exclusion de cet ID exclut tous les disques durs virtuels attachés à cet emplacement dans l’arborescence des captures instantanées de la machine virtuelle, quelle que soit la chaîne de disque dur virtuel valide.

> [!Note]  
> ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**ExportForLiveMigration**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique si la machine virtuelle exportée est destinée à être utilisée dans la migration dynamique.

> [!Note]  
> ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Dans l’étendue de l’espace de noms d’instanciation, identifie de manière opaque et unique une instance de cette classe. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**SnapshotVirtualSystem**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Chemin d’accès à une instance [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représente l’instantané à exporter avec l’ordinateur virtuel. Si la propriété **CopySnapshotConfiguration** n’a pas la valeur 2 (ExportOneSnapshot), cette propriété est ignorée.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ VirtualSystemExportSettingData** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Conditions requises



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

[Classes de gestion du système virtuel](virtual-system-management-classes.md)
</dt> <dt>

[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

