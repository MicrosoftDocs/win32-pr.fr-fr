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
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201221"
---
# <a name="jetmove-function"></a>Fonction JetMove


_**S’applique à :** Windows | Serveur Windows_

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
<td><p>JET_MoveFirst</p></td>
<td><p>Déplace le curseur vers la première entrée d’index dans l’index (s’il en existe un).</p>
<p><strong>Remarque</strong>   La valeur littérale de-2147483648 est utilisée pour désigner cette option. N’utilisez pas cette valeur comme un décalage ordinaire ou un comportement inattendu peut se produire.</p></td>
</tr>
<tr class="even">
<td><p>JET_MoveLast</p></td>
<td><p>Déplace le curseur vers la dernière entrée d’index de l’index (s’il en existe un).</p>
<p><strong>Remarque</strong>   La valeur littérale de 2147483647 est utilisée pour désigner cette option. N’utilisez pas cette valeur comme un décalage ordinaire ou un comportement inattendu peut se produire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_MoveNext</p></td>
<td><p>Déplace le curseur à l’entrée d’index suivante dans l’index (s’il en existe un). Cette valeur est exactement égale à un décalage ordinaire de + 1.</p></td>
</tr>
<tr class="even">
<td><p>JET_MovePrevious</p></td>
<td><p>Déplace le curseur à l’entrée d’index précédente dans l’index (s’il en existe un).</p>
<p>Cette valeur est exactement égale à un décalage ordinaire de-1, ou 0 (zéro).</p>
<p>Le curseur reste à la position logique actuelle et l’existence de l’entrée d’index correspondant à cette position logique sera testée.</p></td>
</tr>
</tbody>
</table>


*grbit*

Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.

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
<td><p>JET_bitMoveKeyNE</p></td>
<td><p>Déplace le curseur vers l’avant ou vers l’arrière selon le nombre d’entrées d’index requises pour ignorer le nombre demandé de valeurs de clé d’index rencontrées dans l’index. Cela a pour effet de réduire les entrées d’index avec des valeurs de clé en double dans une entrée d’index unique. En règle générale, un décalage déplace le curseur en fonction du nombre d’entrées d’index spécifié, indépendamment de leurs valeurs de clés.</p></td>
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
<td><p>L’opération s’est terminée avec succès. Pour <strong>JetMove</strong>, cela signifie qu’une entrée d’index a été trouvée à l’emplacement ou au décalage demandé sur l’index actuel.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Le curseur n’est pas positionné sur une entrée d’index. Pour <strong>JetMove</strong>, cela signifie qu’une entrée d’index est introuvable à l’emplacement ou au décalage demandé sur l’index actuel.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Le curseur est actuellement positionné logiquement sur une entrée d’index qui correspond à un enregistrement qui a été supprimé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


Si cette fonction est réussie, le curseur est positionné sur une entrée d’index qui correspond à l’emplacement ou au décalage demandé. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur et JET_MoveFirst ou JET_MoveLast a été spécifié, cette plage d’index sera annulée. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, la position du curseur reste inchangée, à moins que JET_errNoCurrentRecord ne soit retourné. Dans ce cas, le curseur est positionné à l’emplacement où l’entrée d’index qui correspond à l’emplacement ou au décalage demandé aurait été. Le curseur peut être déplacé par rapport à cette position, mais il n’est pas toujours sur une entrée d’index valide. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur et JET_MoveFirst ou JET_MoveLast a été spécifié, cette plage d’index sera annulée. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Notes

Un curseur peut être déplacé vers deux positions spéciales à l’aide de **JetMove**, avant le premier et après le dernier. Si le curseur se trouve sur la première entrée d’index de la table et que **JetMove** est appelé avec JET_MovePrevious, l’appel échoue avec JET_errNoCurrentRecord et le curseur est positionné logiquement avant la première entrée de l’index. Cette position logique est conservée même si une autre entrée d’index est insérée avant la première entrée de l’index. Une situation analogue se produit pour la dernière fois par rapport à la fin de l’index. Avant le premier et après dernier sont particulièrement utiles lors de la configuration d’une plage d’entrées d’index à itérer à l’aide de **JetMove**, à l’aide d’un modèle d’itérateur qui s’attend à toujours passer à l’élément suivant (ou précédent) avant d’utiliser cet élément.

L’ensemble d’entrées d’index qui peut être visité par **JetMove** peut être limité en définissant une plage d’index sur le curseur. Cela est utile pour les applications qui énumèrent un ensemble d’entrées d’index qui correspondent à des critères simples qui peuvent être exprimés à l’aide d’une paire de clés de recherche générées pour cet index. Pour plus d’informations, consultez [JetSetIndexRange](./jetsetindexrange-function.md).

Dans les versions antérieures à Windows Server 2003 SP1, un problème survient dans **JetMove** dans certains cas spécifiques, ce qui affecte la mise en œuvre correcte d’une plage d’index telle qu’elle est définie par la fonction [JetSetIndexRange](./jetsetindexrange-function.md) . Si le curseur se trouve actuellement avant la première entrée d’index et qu’une plage d’index est définie avec une limite supérieure inférieure à la première entrée d’index, l’appel suivant à **JetMove** passera par erreur à cette entrée d’index au lieu d’échouer avec JET_errNoCurrentRecord, comme prévu. La même erreur se produit pour la situation analogue à partir de la fin de l’index. Cette situation peut se produire dans une application qui configure une plage d’index et la parcourt à l’aide d’un itérateur qui s’attend à démarrer avant la première entrée d’index qui est membre du jeu d’entrées à énumérer, au lieu de démarrer sur la première entrée d’index de ce jeu. Cette situation se produit également dans le cas analogue à partir de la fin de l’index. La solution de contournement consiste à ce que l’application vérifie manuellement que l’entrée d’index acquise se trouve à l’intérieur de la plage d’index en comparant la clé de l’entrée d’index actuelle (Récupérée à l’aide de [JetRetrieveKey](./jetretrievekey-function.md)) avec la clé représentant la fin de la plage d’index actuelle (Récupérée à l’aide de [JetRetrieveKey](./jetretrievekey-function.md) à l’aide de JET_bitRetrieveCopy).

Il est important d’être prudent lors du passage de décalages calculés à **JetMove**. Si le décalage calculé est inférieur ou égal à JET_MoveFirst, cet offset doit être divisé en plusieurs parties, chacune d’elles étant passée à **JetMove** séparément, mais dans une transaction unique pour obtenir l’effet souhaité. Il en va de même pour les décalages supérieurs ou égaux à JET_MoveNext. Il est peu probable qu’une application subisse cette situation dans le monde réel, mais il est judicieux d’avoir une protection contre ce cas en raison de la sémantique très différente de JET_MoveFirst et de JET_MoveLast à partir d’un décalage ordinaire.

Quand **JetMove** est appelé avec un décalage très important, par exemple lorsque le paramètre cRow a la valeur 1000, **JetMove** parcourt toutes les entrées d’index de 1000 pour atteindre la position finale. Actuellement, l’API ESE ne fournit pas de méthode efficace pour passer directement à une entrée d’index donnée par décalage sans traverser chaque entrée d’index.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
