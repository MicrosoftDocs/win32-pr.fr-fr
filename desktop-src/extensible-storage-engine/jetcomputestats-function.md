---
description: 'En savoir plus sur : fonction JetComputeStats'
title: JetComputeStats fonction)
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d990e4ded7dc2485bec6b5ecf92d9999aad57ce5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981972"
---
# <a name="jetcomputestats-function"></a>JetComputeStats fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetcomputestats-function"></a>JetComputeStats fonction)

La fonction **JetComputeStats** parcourt chaque index d’une table pour calculer exactement le nombre d’entrées dans un index et le nombre de clés distinctes dans un index. Ces informations, ainsi que le nombre de pages de base de données allouées pour un index et l’heure actuelle du calcul, sont stockées dans les métadonnées d’index dans la base de données. Ces données peuvent être récupérées par la suite avec les opérations d’informations.

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur qui sera utilisé pour cet appel. Décrit la table sur laquelle calculer les statistiques.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errRollbackError</p> | <p>Une erreur s’est produite lors de l’annulation de l’opération de restauration de toutes les modifications, mais la restauration de la transaction a échoué.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, les statistiques à jour sont stockées dans les catalogues de base de données pour la table décrite avec le curseur donné.

En cas d’échec, aucune mise à jour de n’importe quel type n’est effectuée dans la base de données.

#### <a name="remarks"></a>Remarques

Cette opération peut consommer des ressources puisque chaque index d’une table doit être parcouru dans son intégralité. [JetGetRecordPosition](./jetgetrecordposition-function.md) peut être utilisé pour obtenir une estimation approximative du nombre d’entrées dans un index, mais il ne peut pas estimer lui-même le nombre de valeurs distinctes dans un index.

Les données calculées par cette opération commencent à devenir obsolètes et la table est mise à jour par la suite.

Les mises à jour apportées à la base de données par **JetComputeStats** sont effectuées de manière différée. Cela signifie qu’aucun vidage du journal n’est accompagné de cette opération et qu’un incident système se produit suite à un retour de JET_errSuccess par **JetComputeStats** peut toujours entraîner la perte de ces mises à jour.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetStopService](./jetstopservice-function.md)
