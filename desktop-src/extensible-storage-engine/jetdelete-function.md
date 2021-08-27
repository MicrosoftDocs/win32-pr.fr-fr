---
description: 'En savoir plus sur : fonction JetDelete'
title: Fonction JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e5d8fe6cfc4e0521866a12383aa34f7858432d3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477605"
---
# <a name="jetdelete-function"></a>Fonction JetDelete


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetdelete-function"></a>Fonction JetDelete

La fonction **JetDelete** supprime l’enregistrement en cours dans une table de base de données.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de session de base de données qui sera utilisé pour l’appel d’API.

*TableID*

Curseur sur une table de base de données. La ligne actuelle sera supprimée.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errCallbackFailed</p> | <p>La fonction de rappel a échoué de quelque manière que ce soit. Par exemple, les violations d’accès dans les fonctions de rappel sont interceptées et converties en JET_errCallbackFailed. cette erreur est renvoyée uniquement par Windows XP et versions ultérieures.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIllegalOperation</p> | <p>Le curseur spécifié par <em>TableID</em> ne prend pas en charge la suppression. Consultez la section Notes.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur spécifié par <em>TableID</em> n’est pas sur un enregistrement.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errPermissionDenied</p> | <p>Le moteur de base de données ne dispose pas des autorisations suffisantes pour supprimer l’enregistrement. Cela peut se produire si le fichier de base de données a été ouvert avec un accès en lecture seule.</p> | 
| <p>JET_errRollbackError</p> | <p>Une mémoire tampon de mise à jour (consultez <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) existe, mais toutes les modifications apportées aux colonnes de type JET_coltypLongText et/ou les colonnes de type JET_coltypLongBinary peuvent être restaurées.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Il n’est pas conforme d’utiliser la même session à partir de plusieurs threads en même temps. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errTransReadOnly</p> | <p>La transaction est une transaction en lecture seule et ne prend pas en charge les suppressions.</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>L’opération a échoué, car il n’y a pas assez de mémoire pour conserver les informations transactionnelles sur la mise à jour.</p> | 
| <p>JET_errWriteConflict</p> | <p>Une autre session a déjà verrouillé l’enregistrement pour la mise à jour. La mise à jour tentée par cette session échoue.</p> | 



En cas de réussite, la devise est conservée juste avant l’enregistrement suivant. Si l’enregistrement supprimé était le dernier dans la table, la devise est laissée à la fin de la table (autrement dit, après le nouveau dernier enregistrement). Si l’enregistrement supprimé était le seul enregistrement dans la table, la devise est définie au début.

Les index appropriés sont automatiquement mis à jour.

Si une mise à jour est préparée (à l’aide de [JetPrepareUpdate](./jetprepareupdate-function.md)), elle sera annulée. La mémoire tampon de mise à jour sera réinitialisée.

En cas d’échec, la devise reste inchangée. Si une mise à jour est préparée (voir [JetPrepareUpdate](./jetprepareupdate-function.md)), la mémoire tampon de mise à jour peut être réinitialisée.

#### <a name="remarks"></a>Remarques

Toutes les tables ne prennent pas en charge la suppression de lignes. Une table temporaire ne prend normalement pas en charge la suppression de lignes. La suppression des enregistrements peut être activée sur les tables temporaires pour de nombreuses raisons, dont certaines sont :

  - JET_bitTTUpdatable a été spécifié lors de la création.

  - Les tables temporaires volumineuses peuvent prendre en charge la suppression si elles ont été créées avec JET_bitTTScrollable ou JET_bitTTIndexed. Le seuil auquel une table temporaire devient « grande » est actuellement de 64 kilo-octets, mais elle peut être modifiée dans les versions ultérieures.

Windows XP et versions ultérieures. Les fonctions de rappel peuvent être appelées par **JetDelete**, y compris JET_cbtypBeforeDelete et JET_cbtypAfterDelete.

Il est important de comprendre l’impact de l’exécution d’un grand nombre d’opérations de mise à jour au sein d’une même transaction. Chaque mise à jour de la base de données doit être suivie par le moteur de base de données dans la Banque des versions. La Banque des versions contient un enregistrement dynamique de toutes les différentes versions de chaque entrée d’enregistrement ou d’index dans la base de données qui peuvent être vues par toutes les transactions actives. Ces versions sont utilisées pour prendre en charge le contrôle d’accès concurrentiel multiversion utilisé par le moteur de base de données pour prendre en charge les transactions à l’aide de l’isolation d’instantané. Une fois que le moteur de base de données a épuisé les ressources utilisées pour stocker ces versions, il ne peut plus accepter de modifications tant que certaines transactions n’ont pas été terminées pour permettre la récupération de ces ressources. Lorsque le moteur est dans cet État, toutes les mises à jour échouent avec JET_errVersionStoreOutOfMemory. Les ressources disponibles pour le moteur de base de données pour stocker ces versions peuvent être contrôlées à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec *JET_paramMaxVerPages* et *JET_paramGlobalMinVerPages*.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
