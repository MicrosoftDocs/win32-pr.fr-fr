---
description: Représente une collection de systèmes virtuels.
ms.assetid: acf51beb-1103-43a4-8dc5-1a7f2a0482be
title: Classe Msvm_VirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemCollection
- Msvm_VirtualSystemCollection.CollectionID
- Msvm_VirtualSystemCollection.ElementName
- Msvm_VirtualSystemCollection.LastApplyConsistencyLevel
- Msvm_VirtualSystemCollection.LastApplyVirtualMachineIds
- Msvm_VirtualSystemCollection.LastApplyTime
- Msvm_VirtualSystemCollection.FailedOverReplicationType
- Msvm_VirtualSystemCollection.ReplicationMode
- Msvm_VirtualSystemCollection.ReplicationState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04bb39e0c3ecb73facf09e962d2d189bd6ac59449908c0ed9e0214aa5551595e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644816"
---
# <a name="msvm_virtualsystemcollection-class"></a>MSVM \_ VirtualSystemCollection, classe

Représente une collection de systèmes virtuels.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemCollection : CIM_CollectionOfMSEs
{
  string   CollectionID;
  string   ElementName;
  uint16   LastApplyConsistencyLevel;
  String   LastApplyVirtualMachineIds[];
  DateTime LastApplyTime;
  uint16   FailedOverReplicationType;
  uint16   ReplicationMode;
  uint16   ReplicationState;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemCollection** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemCollection** possède les propriétés suivantes.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« porte »), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identification unique de l’objet de collection.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nom défini par l’utilisateur pour la collection. Notez qu’il n’est pas garanti qu’il soit unique.

</dd> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de basculement effectué pour la collection de systèmes virtuels.

> [!Note]  
> ajouté dans Windows 10, version 1703.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normal** (1)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planifié** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastApplyConsistencyLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Niveau de cohérence du dernier Delta appliqué.

> [!Note]  
> ajouté dans Windows 10, version 1703.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Cohérence des applications** (1)


</dt> <dd>

Le dernier Delta appliqué indique un point dans le temps où le système virtuel était dans un état de cohérence des applications.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Cohérence des incidents** (2)


</dt> <dd>

Le dernier Delta appliqué indique un point dans le temps où le système virtuel était en état de cohérence en cas d’incident.

</dd> <dt>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>

<span id="Group_Crash_Consistent"></span><span id="group_crash_consistent"></span><span id="GROUP_CRASH_CONSISTENT"></span>**Cohérence des pannes de groupe** (3)


</dt> <dd>

Le dernier Delta appliqué indique un point dans le temps où le groupe était dans un état de cohérence en cas d’incident.

</dd> </dl>

</dd> <dt>

**LastApplyTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure à laquelle la dernière réplication est appliquée lors de la récupération de la collection de systèmes virtuels.

> [!Note]  
> ajouté dans Windows 10, version 1703.

 

</dd> <dt>

**LastApplyVirtualMachineIds**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau d’ID d’ordinateur virtuel qui ont été correctement appliqués lors du dernier cycle d’application.

> [!Note]  
> ajouté dans Windows 10, version 1703.

 

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de réplication pour la collection de systèmes virtuels.

> [!Note]  
> ajouté dans Windows 10, version 1703.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Aucun** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

**Principal** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

**Réplica** (2)


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

**Réplica de test** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

État de réplication pour la collection de systèmes virtuels.

> [!Note]  
> ajouté dans Windows 10, version 1703.

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Désactivé** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Prêt pour la réplication** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**En attente de l’exécution de la réplication initiale** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Réplication** (3)


</dt> <dd></dd> <dt>

<span id="Failover_initiated"></span><span id="failover_initiated"></span><span id="FAILOVER_INITIATED"></span>

**Basculement initié** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Récupéré** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Validé** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Suspendu** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critique** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**En attente de démarrage de la resynchronisation** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Resynchronisation** (10)


</dt> <dd></dd> <dt>

<span id="Planned_failover_initiatedRepurpose_initiatedTest_failover_initiatedPartially_enabled"></span><span id="planned_failover_initiatedrepurpose_initiatedtest_failover_initiatedpartially_enabled"></span><span id="PLANNED_FAILOVER_INITIATEDREPURPOSE_INITIATEDTEST_FAILOVER_INITIATEDPARTIALLY_ENABLED"></span>

**Basculement planifié InitiatedRepurpose initiatedTest basculement initiatedPartially activé** (11)


</dt> <dd></dd> <dt>

<span id="Partially_disabled"></span><span id="partially_disabled"></span><span id="PARTIALLY_DISABLED"></span>

**Partiellement désactivé** (12)


</dt> <dd></dd> <dt>

<span id="Partially_recovered"></span><span id="partially_recovered"></span><span id="PARTIALLY_RECOVERED"></span>

**Partiellement récupéré** (13)


</dt> <dd></dd> <dt>



 (14)


</dt> <dd></dd> <dt>



 (15)


</dt> <dd></dd> <dt>



 (16)


</dt> <dd></dd> </dl>

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

[**\_COLLECTIONOFMSES CIM**](cim-collectionofmses.md)
</dt> </dl>

 

