---
description: 'En savoir plus sur : fonction JetMove'
title: Fonction JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 020018ede6be6ff13d65667deee5c189d98e1e53
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474055"
---
# <a name="jetmove-function"></a>Fonction JetMove


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetmove-function"></a>Fonction JetMove

La fonction **JetMove** positionne un curseur au début ou à la fin d’un index et parcourt les entrées de cet index vers l’avant ou vers l’arrière. Il est également possible de déplacer le curseur vers l’avant ou vers l’arrière sur l’index actuel en fonction d’un nombre spécifié d’entrées d’index. Une autre approche consiste à limiter artificiellement les entrées d’index qui peuvent être énumérées à l’aide de **JetMove** en définissant une plage d’index sur le curseur à l’aide de [JetSetIndexRange](./jetsetindexrange-function.md).

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*Vol*

Décalage arbitraire qui indique le déplacement souhaité du curseur sur l’index actuel.

En plus des décalages standard, ce paramètre peut également être défini avec l’une des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_MoveFirst</p> | <p>Déplace le curseur vers la première entrée d’index dans l’index (s’il en existe un).</p><p><strong>Remarque</strong>   La valeur littérale de-2147483648 est utilisée pour désigner cette option. N’utilisez pas cette valeur comme un décalage ordinaire ou un comportement inattendu peut se produire.</p> | 
| <p>JET_MoveLast</p> | <p>Déplace le curseur vers la dernière entrée d’index de l’index (s’il en existe un).</p><p><strong>Remarque</strong>   La valeur littérale de 2147483647 est utilisée pour désigner cette option. N’utilisez pas cette valeur comme un décalage ordinaire ou un comportement inattendu peut se produire.</p> | 
| <p>JET_MoveNext</p> | <p>Déplace le curseur à l’entrée d’index suivante dans l’index (s’il en existe un). Cette valeur est exactement égale à un décalage ordinaire de + 1.</p> | 
| <p>JET_MovePrevious</p> | <p>Déplace le curseur à l’entrée d’index précédente dans l’index (s’il en existe un).</p><p>Cette valeur est exactement égale à un décalage ordinaire de-1, ou 0 (zéro).</p><p>Le curseur reste à la position logique actuelle et l’existence de l’entrée d’index correspondant à cette position logique sera testée.</p> | 



*grbit*

Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitMoveKeyNE</p> | <p>Déplace le curseur vers l’avant ou vers l’arrière selon le nombre d’entrées d’index requises pour ignorer le nombre demandé de valeurs de clé d’index rencontrées dans l’index. Cela a pour effet de réduire les entrées d’index avec des valeurs de clé en double dans une entrée d’index unique. En règle générale, un décalage déplace le curseur en fonction du nombre d’entrées d’index spécifié, indépendamment de leurs valeurs de clés.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès. Pour <strong>JetMove</strong>, cela signifie qu’une entrée d’index a été trouvée à l’emplacement ou au décalage demandé sur l’index actuel.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur n’est pas positionné sur une entrée d’index. Pour <strong>JetMove</strong>, cela signifie qu’une entrée d’index est introuvable à l’emplacement ou au décalage demandé sur l’index actuel.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Le curseur est actuellement positionné logiquement sur une entrée d’index qui correspond à un enregistrement qui a été supprimé.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 



Si cette fonction est réussie, le curseur est positionné sur une entrée d’index qui correspond à l’emplacement ou au décalage demandé. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur et JET_MoveFirst ou JET_MoveLast a été spécifié, cette plage d’index sera annulée. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, la position du curseur reste inchangée, à moins que JET_errNoCurrentRecord ne soit retourné. Dans ce cas, le curseur est positionné à l’emplacement où l’entrée d’index qui correspond à l’emplacement ou au décalage demandé aurait été. Le curseur peut être déplacé par rapport à cette position, mais il n’est pas toujours sur une entrée d’index valide. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur et JET_MoveFirst ou JET_MoveLast a été spécifié, cette plage d’index sera annulée. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Un curseur peut être déplacé vers deux positions spéciales à l’aide de **JetMove**, avant le premier et après le dernier. Si le curseur se trouve sur la première entrée d’index de la table et que **JetMove** est appelé avec JET_MovePrevious, l’appel échoue avec JET_errNoCurrentRecord et le curseur est positionné logiquement avant la première entrée de l’index. Cette position logique est conservée même si une autre entrée d’index est insérée avant la première entrée de l’index. Une situation analogue se produit pour la dernière fois par rapport à la fin de l’index. Avant le premier et après dernier sont particulièrement utiles lors de la configuration d’une plage d’entrées d’index à itérer à l’aide de **JetMove**, à l’aide d’un modèle d’itérateur qui s’attend à toujours passer à l’élément suivant (ou précédent) avant d’utiliser cet élément.

L’ensemble d’entrées d’index qui peut être visité par **JetMove** peut être limité en définissant une plage d’index sur le curseur. Cela est utile pour les applications qui énumèrent un ensemble d’entrées d’index qui correspondent à des critères simples qui peuvent être exprimés à l’aide d’une paire de clés de recherche générées pour cet index. Pour plus d’informations, consultez [JetSetIndexRange](./jetsetindexrange-function.md).

dans les versions antérieures à Windows Server 2003 SP1, un problème survient dans **JetMove** dans certains cas spécifiques, ce qui affecte la mise en œuvre correcte d’une plage d’index telle qu’elle est définie par la fonction [JetSetIndexRange](./jetsetindexrange-function.md) . Si le curseur se trouve actuellement avant la première entrée d’index et qu’une plage d’index est définie avec une limite supérieure inférieure à la première entrée d’index, l’appel suivant à **JetMove** passera par erreur à cette entrée d’index au lieu d’échouer avec JET_errNoCurrentRecord, comme prévu. La même erreur se produit pour la situation analogue à partir de la fin de l’index. Cette situation peut se produire dans une application qui configure une plage d’index et la parcourt à l’aide d’un itérateur qui s’attend à démarrer avant la première entrée d’index qui est membre du jeu d’entrées à énumérer, au lieu de démarrer sur la première entrée d’index de ce jeu. Cette situation se produit également dans le cas analogue à partir de la fin de l’index. La solution de contournement consiste à ce que l’application vérifie manuellement que l’entrée d’index acquise se trouve à l’intérieur de la plage d’index en comparant la clé de l’entrée d’index actuelle (Récupérée à l’aide de [JetRetrieveKey](./jetretrievekey-function.md)) avec la clé représentant la fin de la plage d’index actuelle (Récupérée à l’aide de [JetRetrieveKey](./jetretrievekey-function.md) à l’aide de JET_bitRetrieveCopy).

Il est important d’être prudent lors du passage de décalages calculés à **JetMove**. Si le décalage calculé est inférieur ou égal à JET_MoveFirst, cet offset doit être divisé en plusieurs parties, chacune d’elles étant passée à **JetMove** séparément, mais dans une transaction unique pour obtenir l’effet souhaité. Il en va de même pour les décalages supérieurs ou égaux à JET_MoveNext. Il est peu probable qu’une application subisse cette situation dans le monde réel, mais il est judicieux d’avoir une protection contre ce cas en raison de la sémantique très différente de JET_MoveFirst et de JET_MoveLast à partir d’un décalage ordinaire.

Quand **JetMove** est appelé avec un décalage très important, par exemple lorsque le paramètre cRow a la valeur 1000, **JetMove** parcourt toutes les entrées d’index de 1000 pour atteindre la position finale. Actuellement, l’API ESE ne fournit pas de méthode efficace pour passer directement à une entrée d’index donnée par décalage sans traverser chaque entrée d’index.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
