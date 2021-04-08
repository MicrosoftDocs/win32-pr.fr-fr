---
description: Représente les paramètres de migration pour la migration d’un système virtuel et du stockage attaché à un système virtuel.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Classe Msvm_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862054"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a>MSVM \_ VirtualSystemMigrationSettingData, classe

Représente les paramètres de migration pour la migration d’un système virtuel et du stockage attaché à un système virtuel.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemMigrationSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemMigrationSettingData** possède les propriétés suivantes.

<dl> <dt>

**AllowOverwriteExistingFile**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Autoriser l’opération de migration du stockage à remplacer les fichiers. vhdx existants.

> [!Note]  
> Cette propriété a été ajoutée dans Windows 10, version 1703.

 

</dd> <dt>

**AvoidRemovingVHDs**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Ne supprimez pas les disques durs virtuels pendant la migration, c’est-à-dire les VHD sur la source dans successand VHD sur la destination en cas d’échec.

> [!Note]  
> Ajouté dans Windows 10, version 1703 et Windows Server 2016.

 

</dd> <dt>

**Bande passante**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie la bande passante affectée ou demandée pour une opération de migration de système virtuel. Les unités de bande passante sont spécifiées par la propriété **BandwidthUnit** . Dans une migration, la valeur 0 indique la bande passante par défaut. Dans le cas contraire, la valeur 0 indique que les bandes passantes ne sont pas prises en charge.

**La bande passante et la** **priorité** peuvent être utilisées conjointement. Les processus de migration ayant la valeur de priorité la plus élevée partagent la bande passante disponible en fonction de la bande passante demandée. Si la bande passante n’est pas consommée par cet ensemble de processus, les processus de migration avec la priorité la plus basse égale partagent la bande passante restante. Si la bande passante est toujours supérieure, les processus de migration avec la priorité égale inférieure suivante sont considérés, et ainsi de suite.

Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie les unités utilisées par la propriété de **bande passante** . La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation, tel que défini dans l’annexe C. 1 de DSP0004 V 2.4 ou version ultérieure.

Si la valeur de cette propriété est « percent », la valeur de la propriété de **bande passante** doit être comprise entre 0 et 100, avec des valeurs plus élevées indiquant une bande passante plus élevée. La valeur 100 indique la bande passante totale disponible pour l’exécution des opérations de migration du système virtuel. Les valeurs comprises entre 1 et 100 doivent correspondre de manière linéaire à la plage de bande passante disponible. Par exemple, une valeur de 50 doit demander la moitié de la bande passante disponible.

Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.

</dd> <dt>

**CancelIfBlackoutThresholdExceeded**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Annule la migration si le temps de dépassement du seuil d’indisponibilité est dépassé.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CPUCappingMagnitude**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")
</dt> </dl>

Degré de limitation de l’UC pendant la migration.

> [!Note]  
> Ajouté dans Windows 10, version 1709.

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

**Normal** (0)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Faible** (1)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Élevé** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DestinationIPAddressList**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Il s’agit d’une **valeur null** pour la migration du stockage. Pour la migration du système virtuel, il peut contenir une liste d’adresses IP de l’hôte de destination.

</dd> <dt>

**DestinationPlannedVirtualSystemId**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si une machine virtuelle planifiée existe à la destination de la migration, cette propriété est définie sur le GUID de la machine virtuelle planifiée de destination dans laquelle la machine virtuelle doit être migrée. Cela est utile dans les cas où un utilisateur a créé un ordinateur virtuel planifié à la destination, ainsi que la configuration des ressources, et qu’il souhaite qu’un ordinateur virtuel de la source migre vers cet ordinateur virtuel planifié.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Indique s’il faut compresser le trafic de migration dynamique. **True** indique la compression ; Sinon, **false**.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

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

**MigrationType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")
</dt> </dl>

Spécifie le type d’opération de migration à effectuer. Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)


</dt> <dd>

Migre le système virtuel vers l’ordinateur hôte de destination.

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Stockage** (32769)


</dt> <dd>

Migre uniquement les ressources de stockage du système virtuel.

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Intermédiaire** (32770)


</dt> <dd>

À l’aide de la configuration du système virtuel, crée un système virtuel planifié sur l’ordinateur hôte de destination.

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)


</dt> <dd>

Migre le système virtuel et son stockage vers l’ordinateur hôte de destination.

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)


</dt> <dd>

Effectue une vérification de la capacité de migration des ressources de stockage du système virtuel sur l’ordinateur hôte de destination.

</dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de transport à appliquer si la valeur de **TransportType** est 1 (autre). Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’importance de la migration relative que le système de migration peut utiliser pour commander ou accorder des préférences entre plusieurs demandes de migration en attente. Plus la valeur est faible, plus la priorité est élevée. Dans une migration, la valeur 0 indique la priorité par défaut. Dans le cas contraire, la valeur 0 indique que les priorités ne sont pas prises en charge.

Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.

</dd> <dt>

**RemoveSourceUnmanagedVhds**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Supprimez les disques durs virtuels non gérés source.

> [!Note]  
> Ajouté dans Windows 10 et Windows Server 2016.

 

</dd> <dt>

**RetainVhdCopiesOnSource**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Pour une migration de stockage, cette valeur spécifie si les disques durs virtuels en lecture seule sur l’hôte source doivent être supprimés une fois la migration terminée.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")
</dt> </dl>

Spécifie le type de transport à appliquer pour une opération de migration de système virtuel. Cette propriété est héritée de la **\_ VirtualSystemMigrationSettingData CIM**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Autre** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS strict** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (32768...)


</dt> <dd></dd> </dl>

Pour la migration en direct, cette propriété spécifie le type de transport à utiliser pour transférer l’état du système virtuel vers l’ordinateur hôte de destination. Les valeurs prises en charge sont les suivantes :

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span id="TCP"></span><span id="tcp"></span>**TCP** (5)


</dt> <dd>

Indique le type de transport TCP.

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span id="SMB"></span><span id="smb"></span>**SMB** (32768)


</dt> <dd>

Indique que le type de transport pour le transfert de l’état de l’ordinateur virtuel est SMB.

</dd> </dl>

</dd> <dt>

**UnmanagedVhds**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("MSVM \_ MoveUnmanagedVhd")
</dt> </dl>

Tableau d’instances [**MSVM \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) incorporées qui contiennent des informations sur les disques durs virtuels non managés.

> [!Note]  
> Ajouté dans Windows 10 et Windows Server 2016.

 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VIRTUALSYSTEMMIGRATIONSETTINGDATA CIM**](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

