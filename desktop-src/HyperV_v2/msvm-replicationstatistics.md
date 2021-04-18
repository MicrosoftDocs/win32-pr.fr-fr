---
description: Fournit des statistiques de réplication pour un ordinateur virtuel.
ms.assetid: 52d944a7-9309-4b56-97b7-e050a9501c57
title: Classe Msvm_ReplicationStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationStatistics
- Msvm_ReplicationStatistics.InstanceID
- Msvm_ReplicationStatistics.Caption
- Msvm_ReplicationStatistics.Description
- Msvm_ReplicationStatistics.ElementName
- Msvm_ReplicationStatistics.StartStatisticTime
- Msvm_ReplicationStatistics.EndStatisticTime
- Msvm_ReplicationStatistics.ReplicationSuccessCount
- Msvm_ReplicationStatistics.ReplicationSize
- Msvm_ReplicationStatistics.MaxReplicationSize
- Msvm_ReplicationStatistics.ReplicationLatency
- Msvm_ReplicationStatistics.ReplicationMissCount
- Msvm_ReplicationStatistics.MaxReplicationLatency
- Msvm_ReplicationStatistics.NetworkFailureCount
- Msvm_ReplicationStatistics.ReplicationFailureCount
- Msvm_ReplicationStatistics.PendingReplicationSize
- Msvm_ReplicationStatistics.ApplicationConsistentSnapshotFailureCount
- Msvm_ReplicationStatistics.ReplicationHealth
- Msvm_ReplicationStatistics.LastTestFailoverTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3f18501c2da875a9c3514549271fbc91620abef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519997"
---
# <a name="msvm_replicationstatistics-class"></a>MSVM \_ ReplicationStatistics, classe

Fournit des statistiques de réplication pour un ordinateur virtuel. Ces statistiques couvrent la durée spécifiée par les propriétés **MonitoringStartTime** et **MonitoringInterval** de la [**classe \_ ReplicationServiceSettingData MSVM**](msvm-replicationservicesettingdata.md) .

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationStatistics : CIM_ManagedElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime StartStatisticTime;
  datetime EndStatisticTime;
  uint32   ReplicationSuccessCount;
  uint64   ReplicationSize;
  uint64   MaxReplicationSize;
  uint32   ReplicationLatency;
  uint32   ReplicationMissCount;
  uint32   MaxReplicationLatency;
  uint32   NetworkFailureCount;
  uint32   ReplicationFailureCount;
  uint64   PendingReplicationSize;
  uint32   ApplicationConsistentSnapshotFailureCount;
  uint32   ReplicationHealth;
  datetime LastTestFailoverTime;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ReplicationStatistics** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ReplicationStatistics** possède les propriétés suivantes.

<dl> <dt>

**ApplicationConsistentSnapshotFailureCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total d’échecs d’instantanés VSS.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet de l’objet. Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.

</dd> <dt>

**EndStatisticTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure, en UTC, à laquelle le service de réplication Hyper-V a arrêté la collecte des données des statistiques de réplication. À ce stade, un nouveau cycle des statistiques de réplication démarre.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Identifie de façon unique une instance de cette classe. Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.

</dd> <dt>

**LastTestFailoverTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique la dernière fois qu’un système de réplication de test a été créé pour un ordinateur virtuel de réplication activé sur le serveur de récupération.

</dd> <dt>

**MaxReplicationLatency**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée maximale d’exécution d’un cycle de réplication unique, en secondes.

</dd> <dt>

**MaxReplicationSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre maximal de données de réplication transférées au système hôte de récupération, en octets. Il s’agit de la taille maximale des données de réplication envoyées sur un cycle unique pour cet intervalle.

</dd> <dt>

**NetworkFailureCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total d’erreurs réseau rencontrées pour le canal de réplication avec le système hôte de récupération.

</dd> <dt>

**PendingReplicationSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille des données pour une réplication en attente, en octets.

</dd> <dt>

**ReplicationFailureCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total d’échecs de réplication. Cela comprend les erreurs de l’opération de réplication.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intégrité de la réplication pour la machine virtuelle. Il s’agit de l’une des valeurs suivantes.

<dl> <dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (0)
</dt> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**OK** (1)
</dt> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (2)
</dt> <dt>

<span id="Critical_________________"></span><span id="critical_________________"></span><span id="CRITICAL_________________"></span>**Critique** (3)
</dt> </dl>

</dd> <dt>

**ReplicationLatency**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Latence totale de réplication lors du transfert des données vers le système hôte de récupération, en secondes.

</dd> <dt>

**ReplicationMissCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de cycles de réplication manqués. Cela peut être dû à de lourdes charges de travail, problèmes réseau ou erreurs de réplication.

</dd> <dt>

**ReplicationSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité totale de données de réplication transférées au système hôte de récupération, en octets.

</dd> <dt>

**ReplicationSuccessCount**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre total de réplications réussies pour la machine virtuelle.

</dd> <dt>

**StartStatisticTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure, en UTC, à laquelle le service de réplication Hyper-V a démarré la collecte des données des statistiques de réplication.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

