---
description: Crée une relation de réplication pour un ordinateur virtuel. Lorsqu’un client appelle cette méthode pour un ordinateur virtuel de réplication, il étend la relation de réplication au fournisseur spécifié.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Méthode CreateReplicationRelationship de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d9b61c2339a426314d5c62fe5481b51ba3960c2650ccbdc40b9b9ebd4761cfc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150082"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a>Méthode CreateReplicationRelationship de la \_ classe ReplicationService MSVM

Crée une relation de réplication pour un ordinateur virtuel. Lorsqu’un client appelle cette méthode pour un ordinateur virtuel de réplication, il étend la relation de réplication au fournisseur spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel la réplication doit être activée.

</dd> <dt>

*ReplicationSettingData* \[ dans\]
</dt> <dd>

Représentation sous forme de chaîne d’une instance de la classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) qui définit les paramètres de réplication pour la nouvelle relation de réplication à créer pour l’ordinateur virtuel.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> <dt>

**Fichier introuvable** (32779)
</dt> </dl>

## <a name="remarks"></a>Remarques

**CreateReplicationRelationship** prend une instance [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) comme entrée. Le FRSD associé à l’ordinateur virtuel en tant que fournisseur hôte à hôte est le choix par défaut. L’entrée FRSD est validée pour les paramètres valides pour chaque propriété du fournisseur par défaut. Ce tableau résume les différences de validation par rapport au fournisseur externe.



| Propriété                                             | Fournisseurs externes                                 |
|------------------------------------------------------|----------------------------------------------------|
| ReplicationProvider                                  | Identique au fournisseur par défaut                           |
| AuthenticationType                                   | Ignoré                                            |
| CertificateThumbPrint                                | Ignoré                                            |
| RootCertificateThumbPrint (RO)                       | Ignoré                                            |
| CompressionEnabled                                   | Identique au fournisseur par défaut                           |
| BypassProxyServer                                    | Identique au fournisseur par défaut                           |
| RecoveryConnectionPoint                              | Ignoré \* (peut changer si le fournisseur a besoin) |
| RecoveryHostSystem (RO)                              | Ignoré                                            |
| PrimaryConnectionPoint (RO)                          | Identique au fournisseur par défaut                           |
| PrimaryHostSystem (RO)                               | Identique au fournisseur par défaut                           |
| RecoveryServerPortNumber                             | Ignoré \* (peut changer si le fournisseur a besoin) |
| ReplicateHostKvpItems                                | Ignoré                                            |
| ApplicationConsistentSnapshotInterval                | Identique au fournisseur par défaut                           |
| RecoveryHistory                                      | Identique au fournisseur par défaut                           |
| IncludedDisks\[\]                                    | Identique au fournisseur par défaut                           |
| AutoResynchronizeEnabled                             | Identique au fournisseur par défaut                           |
| AutoResynchronizeIntervalStart                       | Identique au fournisseur par défaut                           |
| AutoResynchronizeIntervalEnd                         | Identique au fournisseur par défaut                           |
| EnableWriteOrderPreservationAcrossDisks (déconseillée) | Identique au fournisseur par défaut                           |
| ReplicationInterval                                  | Identique au fournisseur par défaut                           |



 

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

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

