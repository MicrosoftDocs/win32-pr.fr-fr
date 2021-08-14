---
description: Récupère les statistiques de réplication d’un ordinateur virtuel et agit sur la relation de réplication principale de la machine virtuelle.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Méthode GetReplicationStatistics de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 767ea873b725523e3d430708dc5485d3d24c62e07e5cebac001b020ee996bd63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392913"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a>Méthode GetReplicationStatistics de la \_ classe ReplicationService MSVM

Récupère les statistiques de réplication d’un ordinateur virtuel et agit sur la relation de réplication principale de la machine virtuelle.

> [!Note]  
> à partir de Windows 8.1, nous vous recommandons de ne pas utiliser **GetReplicationStatistics** pour récupérer les statistiques de réplication. Utilisez plutôt [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel les statistiques de réplication doivent être récupérées.

</dd> <dt>

*ReplicationStatistics* \[ à\]
</dt> <dd>

En cas de réussite, reçoit une instance incorporée de la classe [**MSVM \_ ReplicationStatistics**](msvm-replicationstatistics.md) qui contient les statistiques de réplication pour la machine virtuelle demandée.

</dd> <dt>

*ReplicationHealthIssues* \[ à\]
</dt> <dd>

En cas de réussite, reçoit un tableau d’instances incorporées de la classe d' [**\_ erreur MSVM**](msvm-error.md) qui indiquent les avertissements ou erreurs de réplication pour la machine virtuelle demandée.

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

[**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[**MSVM \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

