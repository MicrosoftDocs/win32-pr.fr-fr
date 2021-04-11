---
description: Représente les paramètres spécifiques à la réplication pour un ordinateur virtuel.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Classe Msvm_ReplicationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35bb97e531f8aca5f74801d55a71e5b3f2850c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203414"
---
# <a name="msvm_replicationsettingdata-class"></a>MSVM \_ ReplicationSettingData, classe

Représente les paramètres spécifiques à la réplication pour un ordinateur virtuel. Le client passe une instance de cette classe à [**MSVM \_ ReplicationService. CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) pour créer une relation de réplication. Le client ne peut pas modifier directement les valeurs des propriétés de cette classe ; il doit appeler la méthode [**MSVM \_ ReplicationService. ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) pour modifier les valeurs. Chaque relation de réplication possède une seule instance de paramètres.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ReplicationSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ReplicationSettingData** possède les propriétés suivantes.

<dl> <dt>

**AdditionalSettings**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Paramètres de réplication supplémentaires que le fournisseur de point de terminaison peut utiliser.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**ApplicationConsistentSnapshotInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de temps entre les captures instantanées cohérentes de l’application, spécifié en heures. Les valeurs valides sont comprises entre 1 heure et 12 heures.

</dd> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Définit le mode d’authentification utilisé pour se connecter au serveur de récupération.

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Authentification Kerberos** (1)


</dt> <dd>

Authentification Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Authentification basée sur les certificats** (2)


</dt> <dd>

Authentification basée sur les certificats.

</dd> </dl>

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Non utilisé.

Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Non utilisé.

Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Non utilisé.

Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Délai avant le démarrage automatique de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre qui indique la séquence relative d’activation d’ordinateur virtuel lors du démarrage du système hôte. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**AutoResynchronizeEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les opérations de resynchronisation sont déclenchées automatiquement lorsqu’une erreur de réplication se produit en raison de défaillances de l’alimentation et du matériel. Les opérations de resynchronisation ne sont déclenchées que lorsque l’échec se produit entre les heures spécifiées par les propriétés **AutoResynchronizeIntervalStart** et **AutoResynchronizeIntervalEnd** .

La valeur par défaut est **False**.

</dd> <dt>

**AutoResynchronizeIntervalEnd**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’heure de fin des opérations de resynchronisation automatique à déclencher. Cette valeur est en heure locale. La valeur par défaut est 06:00 (6:00 A.M.).

Les opérations de resynchronisation ne sont déclenchées que lorsque l’échec se produit entre les heures spécifiées par les propriétés **AutoResynchronizeIntervalStart** et **AutoResynchronizeIntervalEnd** .

Les opérations de resynchronisation peuvent également être planifiées pour être déclenchées au cours de l’intervalle suivant.

</dd> <dt>

**AutoResynchronizeIntervalStart**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie l’heure de début des opérations de resynchronisation automatique à déclencher. Cette valeur est en heure locale. La valeur par défaut est 18:30 (6:30 P.M.).

Les opérations de resynchronisation ne sont déclenchées que lorsque l’échec se produit entre les heures spécifiées par les propriétés **AutoResynchronizeIntervalStart** et **AutoResynchronizeIntervalEnd** .

Les opérations de resynchronisation peuvent également être planifiées pour être déclenchées au cours de l’intervalle suivant.

</dd> <dt>

**BypassProxyServer**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si le serveur proxy doit être contourné lors de la connexion à un serveur de récupération.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de réplication ».

</dd> <dt>

**Empreinte**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Empreinte numérique du certificat à utiliser lorsque la propriété **AuthenticationType** est l’authentification basée sur les certificats.

</dd> <dt>

**CompressionEnabled**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les données de réplication sont compressées lors de leur envoi au serveur de récupération.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Non utilisé.

Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Fichier ConfigurationFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès relatif et nom de fichier d’un fichier dans lequel sont stockées les informations relatives à la configuration de l’ordinateur virtuel. Ce chemin d’accès est relatif à la propriété **ConfigurationDataRoot** . Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identificateur unique de la configuration de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure de création des paramètres de l’ordinateur virtuel. Si cet objet représente les paramètres actuels de l’ordinateur virtuel, cette valeur correspond à l’heure à laquelle le système a été créé. Si cet objet représente les paramètres d’instantané de la machine virtuelle, cette valeur correspond à l’heure à laquelle l’instantané a été pris. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « données des paramètres de réplication de l’ordinateur virtuel ».

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))et est définie sur le nom complet de la machine virtuelle.

</dd> <dt>

**EnableWriteOrderPreservationAcrossDisks**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)
</dt> </dl>

Spécifie si tous les disques durs virtuels de réplication de la machine virtuelle sont répliqués au même point dans le temps. Cela garantit que la réplication honore l’ordre d’écriture des applications dans la machine virtuelle.

**Windows 8.1 :** À partir de Windows 8.1 et de Windows Server 2012 R2, cette propriété est déconseillée et a toujours la valeur **true**.

</dd> <dt>

**IncludedDisks**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **HyperVEmbeddedInstance** ("CIM \_ StorageAllocationSettingData"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")
</dt> </dl>

Liste des disques durs virtuels (VHD) attachés au système qui seront répliqués par le moteur de réplication. Il s’agit d’un tableau de chaînes, chacune contenant l' **InstanceID** du [**\_ StorageAllocationSettingData MSVM**](msvm-storageallocationsettingdata.md) qui représente le disque dur virtuel.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)). Pour Windows 8, elle est toujours définie sur « Microsoft :*GUID d’ordinateur virtuel* \\ HVR ». Par Windows 8.1, elle est définie sur « Microsoft :*GUID d’ordinateur virtuel* \\ HVR \\<0/1> ». Dans la valeur Windows 8.1, 0 indique primaire et 1 indique la réplication étendue. Pour plus d’informations sur la réplication étendue, consultez [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire dans lequel sont stockées les informations de journalisation de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**Remarques**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Non utilisé et ne peut pas être défini.

Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**PrimaryConnectionPoint**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom du point de connexion principal. Dans le cas d’un cluster principal, il s’agit du nom de l’extrémité de service Broker. Dans le cas d’un serveur principal autonome, il s’agit du nom du système hôte.

</dd> <dt>

**PrimaryHostSystem**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom de domaine complet du système hôte principal qui héberge l’ordinateur virtuel.

</dd> <dt>

**RecoveryConnectionPoint**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom du point de connexion de récupération. Dans le cas d’un cluster de récupération, il s’agit du nom de l’extrémité de service Broker. Dans le cas d’un serveur de récupération autonome, il s’agit du nom du système hôte.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès complet d’un fichier dans lequel sont stockées les informations relatives à la récupération de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**RecoveryHistory**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre maximal d’instantanés de récupération qui seront stockés sur le serveur de récupération. Les valeurs valides sont comprises entre 0 et 24.

</dd> <dt>

**RecoveryHostSystem**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nom de domaine complet du système hôte de récupération qui héberge la machine virtuelle.

</dd> <dt>

**RecoveryServerPortNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de port du serveur de récupération à utiliser pour établir une connexion sécurisée pour la réplication.

</dd> <dt>

**ReplicateHostKvpItems**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie si les [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s de l’ordinateur hôte doivent être répliqués à partir de l’ordinateur virtuel principal vers l’ordinateur virtuel de récupération.

</dd> <dt>

**ReplicationInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de réplication d’une relation de réplication, en secondes. Les valeurs autorisées sont :

30

300

900

La valeur par défaut est 300 secondes.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**ReplicationProvider**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès à l’instance de la classe [**MSVM \_ ReplicationProvider**](msvm-replicationprovider.md) qui identifie le point de terminaison du fournisseur de réplication.

**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.

</dd> <dt>

**RootCertificateThumbPrint**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Empreinte numérique de certificat racine du certificat en cours d’utilisation lorsque **AuthenticationType** est 2 (autorisation basée sur un certificat).

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations sur les captures instantanées d’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockées les informations relatives aux informations relatives à la suspension de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès d’un répertoire où sont stockés les fichiers d’échange de l’ordinateur virtuel. Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.

</dd> <dt>

**Attribut virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de l’objet [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) auquel appartiennent les données de ce paramètre. Cette propriété est une substitution de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Spécifie le type de machine virtuelle que les données de paramètre représentent. Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))et est toujours définie sur « Microsoft : Hyper-V : réplica ».

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

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

