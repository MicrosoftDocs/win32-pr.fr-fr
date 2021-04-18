---
description: Demande que l’état de réplication de la relation de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée.
ms.assetid: 8EC78CCC-2997-4239-A20C-BA56F848ECB6
title: 'Msvm_ComputerSystem :: RequestReplicationStateChangeEx, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChangeEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d77db9dff90f985991c8e9013ea4f239cb6479f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526128"
---
# <a name="msvm_computersystemrequestreplicationstatechangeex-method"></a>MSVM \_ ComputerSystem :: RequestReplicationStateChangeEx, méthode

Demande que l’état de réplication de la relation de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée. Pendant que le changement d’État est en cours, la propriété **ReplicationState** est remplacée par la valeur du paramètre *RequestedState* . Cette méthode est prise en charge uniquement pour les instances de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représentent un ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
uint32 RequestReplicationStateChangeEx(
  [in]  string              ReplicationRelationship,
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ReplicationRelationship* \[ dans\]
</dt> <dd>

Représentation sous forme de chaîne d’une instance incorporée de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui définit la relation de réplication pour la demande de modification d’État. Ce paramètre est facultatif. Lorsqu’elle n’est pas spécifiée, la demande s’exécute sur la relation de réplication principale.

</dd> <dt>

*RequestedState* \[ dans\]
</dt> <dd>

Nouvel état de réplication. Doit avoir l’une des valeurs suivantes.

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Prêt à démarrer la réplication initiale** (1)


</dt> <dd>

Prêt à démarrer la réplication initiale.

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**En attente de l’exécution de la réplication initiale** (2)


</dt> <dd>

En attente de l’exécution de la réplication initiale.

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Réplication** (3)


</dt> <dd>

Réplication.

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Réplication synchronisée terminée** (4)


</dt> <dd>

Réplication synchronisée terminée.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspendre** (7)


</dt> <dd>

Suspend la réplication.

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Annuler la resynchronisation** (9)


</dt> <dd>

Annulez la resynchronisation.

</dd> </dl> </dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Référence facultative à un objet [**\_ ConcreteJob MSVM**](msvm-concretejob.md) qui est retourné si l’opération est exécutée de façon asynchrone. Si elle est présente, la référence retournée peut être utilisée pour surveiller la progression et obtenir le résultat de la méthode.

</dd> <dt>

*TimeoutPeriod* \[ dans\]
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                                                | Description                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Terminé sans erreur**</dt> <dt>0</dt> </dl>                    | Succès<br/>                                                                                                          |
| <dl> <dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt> </dl> | La transition est asynchrone.<br/>                                                                                  |
| <dl> <dt>**Échec**</dt> <dt>32768</dt> </dl>                                 |                                                                                                                             |
| <dl> <dt>**Accès refusé**</dt> <dt>32769</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Non pris en charge**</dt> <dt>32770</dt> </dl>                          |                                                                                                                             |
| <dl> L' <dt>**État est inconnu**</dt> <dt>32771</dt> </dl>                      |                                                                                                                             |
| <dl> <dt>**Délai d’expiration**</dt> <dt>32772</dt> </dl>                                |                                                                                                                             |
| <dl> <dt>**Paramètre non valide**</dt> <dt>32773</dt> </dl>                      | La valeur spécifiée dans l’un des paramètres n’est pas prise en charge.<br/>                                                   |
| <dl> Le <dt>**système est en cours d’utilisation**</dt> <dt>32774</dt> </dl>                       |                                                                                                                             |
| <dl> <dt>**État non valide pour cette opération**</dt> <dt>32775</dt> </dl>       | La valeur spécifiée dans le paramètre *RequestedState* n’est pas prise en charge dans le mode de réplication ou l’état actuel.<br/> |
| <dl> <dt>**Type de données incorrect**</dt> <dt>32776</dt> </dl>                    |                                                                                                                             |
| <dl> Le <dt>**système n’est pas disponible**</dt> <dt>32777</dt> </dl>                |                                                                                                                             |
| <dl> <dt>**Mémoire Insuffisante**</dt> <dt>32778</dt> </dl>                          |                                                                                                                             |
| <dl> <dt>**Fichier introuvable**</dt> <dt>32779</dt> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\\\\\Virtualisation racine \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ComputerSystem**](msvm-computersystem.md)
</dt> </dl>

 

 




