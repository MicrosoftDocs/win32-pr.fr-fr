---
description: 'En savoir plus sur : fonction JetDefragment2'
title: JetDefragment2 fonction)
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bcde8d55032d2e07466668b5a4d96b9a447d843
ms.sourcegitcommit: 35baf9ba19918a38c4ca8714f88c004af0c6f518
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107838803"
---
# <a name="jetdefragment2-function"></a>JetDefragment2 fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetdefragment2-function"></a>JetDefragment2 fonction)

La fonction **JetDefragment2** démarre et arrête les tâches de défragmentation de base de données qui améliorent l’Organisation des données dans une base de données, avec un paramètre de rappel disponible pour signaler la progression de la défragmentation. Cela permet de limiter la croissance de la base de données en utilisant l’allocation de disque existante plus efficacement dans la base de données. Elle peut également réduire la plage de travail en garantissant un compactage plus étroit des données. Enfin, il peut améliorer les performances des applications en accélérant les opérations courantes via une meilleure organisation des données.

**Windows XP :**  **JetDefragment2** est introduit dans Windows XP.

**JetDefragment2** contient également un paramètre de fonction de rappel utilisé pour signaler la progression du processus de défragmentation.

La défragmentation de base de données est une opération en ligne et n’interrompt pas l’activité normale de la base de données, comme les opérations de requête ou les mises à jour des données. **JetDefragment2** ne fait pas non plus de copie de toutes les données existantes. Au lieu de cela, elle défragmente une base de données sur place. Enfin, **JetDefragment2** récupère l’espace de la base de données interne en vue de sa réutilisation, mais ne libère pas d’espace supplémentaire dans le système de fichiers du système d’exploitation.

Le format des données résultant peut être bien plus efficace, mais n’est généralement pas optimal. La défragmentation est limitée à la libération des pages de base de données à réutiliser qui contiennent des données qui ont déjà été logiquement supprimées. La défragmentation rend également les pages de base de données disponibles pour une réutilisation dans certains cas en combinant les données de deux pages quand elles peuvent tenir sur une seule page.

Cette opération est différente de [JetCompact](./jetcompact-function.md) qui fait une copie d’une base de données en lecture seule dans un format très optimal.

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*dbid*

Base de données à défragmenter.

*szTableName*

Parfois, *szTableName* est requis, et il est parfois interdit :

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Doit être `NULL`. |
| `JET_bitDefragmentBTree` | Spécifie le nom de la table/BTree à défragmenter. |
| *autres* | Doit être `NULL`. |
 
La défragmentation est effectuée pour l’ensemble de la base de données décrite par l’ID de base de données spécifié.

*pcPasses*

Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre d’entrée facultatif définit le nombre maximal de passes de défragmentation. Lors de l’arrêt d’une tâche de défragmentation en ligne, cette mémoire tampon de sortie facultative est définie sur le nombre de passes effectuées.

Lorsque ce paramètre a la valeur NULL, le nombre de passes de défragmentation en ligne est illimité.

*pcSeconds*

Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre d’entrée facultatif définit la durée maximale de la défragmentation. Lors de l’arrêt d’une tâche de défragmentation en ligne, cette mémoire tampon de sortie facultative est définie sur la durée utilisée pour la défragmentation.

Lorsque ce paramètre est défini sur NULL ou si *pcSeconds* pointe vers une valeur négative, la durée maximale de la défragmentation est illimitée.

*rappel*

Fonction de rappel que la défragmentation appelle régulièrement pour signaler la progression.

| *grbit* | *szTableName* |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | Doit être `NULL`. |
| `JET_bitDefragmentBTree` | Doit être `NULL`. |
| *autres* | facultatif.


*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDefragmentAvailSpaceTreesOnly</p></td>
<td><p>Cette option est utilisée pour défragmenter la partie espace disponible de l’allocation de l’espace de la base de données ESE. L’espace de la base de données est divisé en deux types, l’espace détenu et l’espace disponible. L’espace détenu est alloué à une table ou à un index, alors que l’espace disponible est prêt à être utilisé dans la table ou l’index, respectivement. L’espace disponible est bien plus dynamique dans le comportement et nécessite une défragmentation en ligne plus qu’un espace détenu ou des données de table ou d’index.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBatchStart</p></td>
<td><p>Cette option permet de démarrer une nouvelle tâche de défragmentation.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBatchStop</p></td>
<td><p>Cette option est utilisée pour arrêter une tâche de défragmentation démarrée existante.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDefragmentBTree</p></td>
<td><p>Cette option est utilisée pour défragmenter une arborescence binaire (B-Tree), spécifiée par szTableName.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDefragmentBTreeBatch</p></td>
<td><p>Cette option est utilisée pour appeler OLD2 sur l’ensemble de la base de données.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Code de retour</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseFileReadOnly</p></td>
<td><p>La base de données choisie pour la défragmentation est en lecture seule et ne peut pas être mise à jour de quelque façon que ce soit, y compris la défragmentation.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDistributedTransactionAlreadyPreparedToCommit</p></td>
<td><p>La session donnée est dans l’état préparé pour valider et ne peut pas commencer les nouvelles mises à jour tant que la transaction en cours n’est pas validée ou annulée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>L’ID de base de données spécifié ne correspond pas à une base de données connue dans l’instance.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La session donnée a uniquement des privilèges en lecture seule et ne peut pas démarrer une tâche qui peut effectuer une mise à jour, y compris une défragmentation.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Cette erreur se produit lorsque la taille de la Banque des versions configurée est insuffisante pour contenir toutes les mises à jour en suspens.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnDefragAlreadyRunning</p></td>
<td><p>L’option JET_bitDefragmentBatchStart a été passée, mais une tâche de défragmentation exécute déjà la défragmentation sur la base de données spécifiée.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDefragNotRunning</p></td>
<td><p>L’option JET_bitDefragmentBatchStop a été passée, mais aucune tâche de défragmentation n’est en cours d’exécution.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, l’action demandée de démarrage d’une tâche de défragmentation pour des données données avec les options spécifiées est effectuée, ou l’action d’arrêt d’une tâche de défragmentation existante est effectuée.

En cas d’échec, l’action demandée de démarrage ou d’arrêt d’un travail de défragmentation en ligne n’est pas effectuée. Aucun autre effet secondaire ne se produit.

#### <a name="remarks"></a>Remarques

La défragmentation en ligne est contrôlée à la fois par un paramètre, ainsi que par cette API. La valeur par défaut du paramètre système est JET_OnlineDefragAll, ce qui signifie que la défragmentation est activée pour toutes les structures de données prises en charge. Toutefois, à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md), il est possible de désactiver la défragmentation en ligne ou de l’activer de manière sélective pour les arborescences d’espace de base de données uniquement, les bases de données uniquement, les fichiers de streaming uniquement ou une combinaison de ces options. Si le paramètre système pour la défragmentation en ligne est un paramètre obsolète, **JetDefragment2** traite le paramètre comme JET_OnlineDefragAll.

Il peut y avoir au plus une tâche en cours d’exécution pour chaque base de données. La tâche s’exécute en tant que thread dans le processus hébergeant le moteur ESE.

La session utilisée pour démarrer la tâche de défragmentation en ligne peut être utilisée par la suite pour les opérations de base de données pendant que la tâche de défragmentation se poursuit, car la tâche de défragmentation alloue sa propre session. La session donnée est utilisée uniquement pour vérifier les autorisations associées à la session de démarrage de la tâche et n’est pas réellement utilisée pour les opérations de défragmentation elles-mêmes.

#### <a name="requirements"></a>Spécifications

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetDefragment2W</strong> (Unicode) et <strong>JetDefragment2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetCompact](./jetcompact-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
