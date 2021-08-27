---
description: Démarre la réplication d’un ordinateur virtuel.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Méthode StartReplication de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f774192cf5c65f6fff0d9a1a17df51483984b49efd6be437f0348547eed5082c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050489"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a>Méthode StartReplication de la \_ classe ReplicationService MSVM

Démarre la réplication d’un ordinateur virtuel. Lorsqu’un client appelle cette méthode pour un ordinateur virtuel de réplication, il démarre la réplication avec le réplica étendu.

## <a name="syntax"></a>Syntaxe


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel la réplication doit être démarrée.

</dd> <dt>

*InitialReplicationType* \[ dans\]
</dt> <dd>

Type de transfert à utiliser pour effectuer la réplication initiale.

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Transfert réseau** (1)


</dt> <dd>

Transfert réseau.

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Exporter** (2)


</dt> <dd>

exportation.

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Transfert réseau amorcé** (3)


</dt> <dd>

Transfert réseau amorcé.

</dd> </dl> </dd> <dt>

*InitialReplicationExportLocation* \[ dans\]
</dt> <dd>

Si *InitialReplicationType* a la valeur 2 (exporter), ce paramètre contient le chemin d’accès complet du répertoire dans lequel la réplication initiale doit être exportée. Ce paramètre n’est pas utilisé pour d’autres valeurs de *InitialReplicationType* et peut avoir la **valeur null**. Ce répertoire peut être réutilisé pour l’exportation de plusieurs réplications de machines virtuelles. Cette méthode place chaque réplication de machine virtuelle dans un sous-répertoire distinct sous ce chemin d’accès.

</dd> <dt>

*StartTime* \[ dans\]
</dt> <dd>

Heure de début planifiée pour la réplication initiale sur la connexion réseau au serveur de récupération. Ce paramètre est ignoré lorsque *InitialReplicationType* est 2 (exportation). Si ce paramètre a la **valeur null**, la réplication initiale démarre immédiatement.

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
</dt> </dl>

 

