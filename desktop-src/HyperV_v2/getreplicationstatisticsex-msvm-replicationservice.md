---
description: Récupère les statistiques de réplication associées à la relation de réplication spécifiée de l’ordinateur virtuel.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: 'Msvm_ReplicationService :: GetReplicationStatisticsEx, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519328"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a>MSVM \_ ReplicationService :: GetReplicationStatisticsEx, méthode

Récupère les statistiques de réplication associées à la relation de réplication spécifiée de l’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel les statistiques de réplication doivent être récupérées.

</dd> <dt>

*ReplicationRelationship* \[ dans\]
</dt> <dd>

Représentation sous forme de chaîne d’une instance incorporée de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) qui définit la relation de réplication dont les statistiques de réplication doivent être récupérées.

</dd> <dt>

*ReplicationStatistics* \[ à\]
</dt> <dd>

En cas de réussite, reçoit une instance incorporée de la classe [**MSVM \_ ReplicationStatistics**](msvm-replicationstatistics.md) qui contient les statistiques de réplication pour la relation de réplication demandée.

</dd> <dt>

*ReplicationHealthIssues* \[ à\]
</dt> <dd>

En cas de réussite, reçoit un tableau d’instances incorporées de la classe d' [**\_ erreur MSVM**](msvm-error.md) qui indiquent les avertissements ou erreurs de réplication pour la machine virtuelle demandée.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)). Cette référence peut être **null** si la tâche est terminée.

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
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\\\\\Virtualisation racine \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> <dt>

[**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

