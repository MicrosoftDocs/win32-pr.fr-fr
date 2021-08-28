---
description: 'En savoir plus sur : fonction JetSetIndexRange'
title: Fonction JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 330adc9b4d18a7bfa66ced0c9cb5776f31162be5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988452"
---
# <a name="jetsetindexrange-function"></a>Fonction JetSetIndexRange


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetsetindexrange-function"></a>Fonction JetSetIndexRange

La fonction **JetSetIndexRange** limite temporairement l’ensemble des entrées d’index que le curseur peut parcourir à l’aide de [JetMove](./jetmove-function.md) à celles commençant à l’entrée d’index actuelle et se terminant à l’entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et les critères liés spécifiés. Une clé de recherche doit avoir été construite précédemment à l’aide de [JetMakeKey](./jetmakekey-function.md).

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*tableidSrc*

Curseur à utiliser pour cet appel.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitRangeInclusive</p> | <p>Cette option indique les critères de limite de la plage d’index. Lorsqu’elle est présente, cette option indique que la limite de la plage d’index est comprise. Lorsqu’elle est absente, cette option indique que la limite de la plage d’index est exclusive. Lorsque la limite de la plage d’index est inclusive, toutes les entrées d’index correspondant exactement aux critères de recherche sont incluses dans la plage.</p> | 
| <p>JET_bitRangeInstantDuration</p> | <p>Cette option demande que la plage d’index soit supprimée dès qu’elle a été établie. Tous les autres aspects de l’opération restent inchangés. Cela est utile pour tester l’existence d’entrées d’index qui correspondent aux critères de recherche.</p> | 
| <p>JET_bitRangeRemove</p> | <p>Cette option demande l’annulation d’une plage d’index existante sur le curseur. Une fois la plage d’index annulée, il est possible de se déplacer au-delà de la fin de la plage d’index à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>. Si une plage d’index n’est pas déjà en vigueur, <strong>JetSetIndexRange</strong> échoue avec JET_errInvalidOperation.</p><p>Quand cette option est spécifiée, toutes les autres options sont ignorées.</p> | 
| <p>JET_bitRangeUpperLimit</p> | <p>Si cette option est utilisée, la clé de recherche dans le curseur représente les critères de recherche de l’entrée d’index la plus proche de la fin de l’index qui correspond à la plage d’index. La plage d’index sera établie entre la position actuelle du curseur et cette entrée d’index afin que toutes les correspondances puissent être trouvées en progressant vers l’index à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a> avec JET_MoveNext ou un décalage positif.</p><p>Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches du début de l’index.</p><p>Si cette option est omise, la clé de recherche dans le curseur représente les critères de recherche de l’entrée d’index la plus proche du début de l’index qui correspond à la plage d’index. La plage d’index sera établie entre la position actuelle du curseur et cette entrée d’index afin que toutes les correspondances puissent être trouvées en parcourant l’index à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a> avec JET_MovePrevious ou un décalage négatif.</p><p>Il n’est pas judicieux d’omettre cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches de la fin de l’index.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p><p>Pour <strong>JetSetIndexRange</strong>, cela signifie qu’une plage d’index existante a été annulée ou qu’il existe au moins une entrée d’index à l’intérieur de la plage d’index.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidOperation</p> | <p>Cette erreur est retournée par <strong>JetSetIndexRange</strong> lorsque JET_bitRangeRemove a été spécifié et qu’aucune plage d’index n’était en vigueur.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Il n’existe pas de clé de recherche pour le curseur. <strong>JetSetIndexRange</strong> requiert que le curseur ait une clé de recherche valide, car il l’utilise pour les critères de recherche utilisés pour rechercher des entrées d’index.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Il n’y a pas d’index actuel pour le curseur. Cela se produit pour <strong>JetSetIndexRange</strong> si le curseur se trouve sur l’index cluster d’une table, un index primaire n’a pas été défini. La définition d’une plage d’index sur un tel index n’est pas prise en charge.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Cette erreur est retournée par <strong>JetSetIndexRange</strong> pour indiquer qu’il n’y a pas d’entrées d’index à l’intérieur de la plage d’index.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, si JET_bitRangeRemove est spécifié, la plage d’index actuellement en vigueur est annulée. Si JET_bitRangeRemove n’est pas spécifié et que JET_bitRangeInstantDuration est spécifié, aucune plage d’index n’est en vigueur. Si ni JET_bitRangeRemove ni JET_bitRangeInstantDuration n’est spécifié, une nouvelle plage d’index est en vigueur. Cette plage d’index limite temporairement l’ensemble d’entrées d’index que le curseur peut parcourir à l’aide de [JetMove](./jetmove-function.md) à celles qui commencent à l’entrée d’index actuelle et se termine à l’entrée d’index correspondant aux critères de recherche. La position du curseur reste inchangée. Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée. Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, si JET_errNoCurrentRecord n’est pas retourné, aucune plage d’index n’est en vigueur. Si JET_errNoCurrentRecord est retourné, une nouvelle plage d’index est en vigueur. Cette plage d’index limite temporairement l’ensemble d’entrées d’index que le curseur peut parcourir à l’aide de [JetMove](./jetmove-function.md) à celles qui commencent à l’entrée d’index actuelle et se termine à l’entrée d’index correspondant aux critères de recherche. La position du curseur reste inchangée. Si JET_errNoCurrentRecord a été retourné et qu’une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Une plage d’index est volatile et sera automatiquement annulée si une navigation autre que [JetMove](./jetmove-function.md) est effectuée sur le curseur.

Les plages d’index fonctionnent uniquement dans une seule direction. Si une limite supérieure est établie, seul le déplacement vers l’avant à l’aide de [JetMove](./jetmove-function.md) avec JET_MoveNext ou un décalage positif est évité une fois que la fin de la plage d’index a été atteinte. Dans ce cas, il est toujours possible de conserver la plage d’index à l’aide de [JetMove](./jetmove-function.md) avec JET_MovePrevious ou un décalage négatif. Une situation analogue se produit pour une limite inférieure.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetIndexRange]()  
[JetStopService](./jetstopservice-function.md)
