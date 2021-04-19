---
description: 'En savoir plus sur : fonction JetSetCurrentIndex'
title: Fonction JetSetCurrentIndex
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514401"
---
# <a name="jetsetcurrentindex-function"></a>Fonction JetSetCurrentIndex


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetsetcurrentindex-function"></a>Fonction JetSetCurrentIndex

La fonction **JetSetCurrentIndex** peut être utilisée pour définir l’index actuel d’un curseur. L’index actuel d’un curseur définit les enregistrements d’une table qui sont visibles pour ce curseur et l’ordre dans lequel ils apparaissent en sélectionnant l’ensemble d’entrées d’index à utiliser pour exposer ces enregistrements.

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*szIndexName*

Nom de l’index à sélectionner pour le curseur.

Si ce paramètre a la valeur NULL ou est une chaîne vide, l’index cluster est sélectionné. Si un index primaire est défini pour la table, cet index est sélectionné, car il est identique à l’index cluster. Si aucun index primaire n’est défini pour la table, l’index séquentiel est sélectionné. L’index séquentiel n’a pas de définition d’index. Pour plus d’informations, consultez [JetCreateIndex](./jetcreateindex-function.md) .

Si *pIndexID* n’a pas la valeur null, le nom de l’index sera ignoré et l’index sera sélectionné par son ID d’index.

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
<td><p>JET_errBadItagSequence</p></td>
<td><p>Un index secondaire est sélectionné avec l’option JET_bitNoMove et il n’y a aucune valeur pour la première colonne clé à valeurs multiples dans la définition de la nouvelle index qui correspond au numéro de séquence spécifié.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidIndexId</p></td>
<td><p>Le contenu de l’ID d’index n’était pas valide ou a expiré et doit être actualisé. Cela peut se produire pour <strong>JetSetCurrentIndex</strong> dans les cas suivants :</p>
<ul>
<li><p>pIndexID- &gt; cbStruct n’est pas de la taille attendue (Windows Server 2003 et versions ultérieures).</p></li>
<li><p>Le moteur a été arrêté depuis que l’ID d’index a été extrait.</p></li>
<li><p>Tous les curseurs faisant référence à la table contenant l’index correspondant à l’ID d’index ont été fermés et le moteur a supprimé la définition de cet index du cache de schéma.</p></li>
<li><p>L’ID d’index est utilisé avec un curseur ouvert sur une table incorrecte.</p></li>
<li><p>L’index a été supprimé ou n’est pas encore visible dans la session.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p>Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>L’un des noms d’objets spécifiés n’est pas valide. Tous les noms d’objets doivent être conformes au même ensemble de règles. Ces règles sont les suivantes :</p>
<ul>
<li><p>Les noms d’objets doivent être composés de caractères ASCII.</p></li>
<li><p>Les noms d’objets doivent comporter au moins un caractère.</p></li>
<li><p>Les noms d’objets ne peuvent pas dépasser JET_cbNameMost (64) caractères.</p></li>
<li><p>Les noms d’objets ne peuvent pas commencer par un espace.</p></li>
<li><p>Les noms d’objets ne peuvent pas contenir de caractères de contrôle ASCII (0x00 à 0x1F).</p></li>
<li><p>Les noms d’objets ne peuvent pas contenir de point d’exclamation ( !), de point (.), de crochet gauche ([) ou de crochet droit (]).</p></li>
<li><p>Une fois validée, seule la partie de la chaîne jusqu’au premier espace (le cas échéant) sera utilisée pour le nom de l’objet. Cela signifie que les noms d’objets ne peuvent pas non plus contenir d’espace.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetSetCurrentIndex</strong> lorsque <em>pIndexID</em> n’a pas la valeur null et que pIndexID- &gt; cbStruct n’est pas de la taille attendue (Windows XP et versions antérieures).</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Un index secondaire est sélectionné avec l’option JET_bitNoMove et il n’existe aucune entrée d’index dans le nouvel index qui correspond à l’enregistrement associé à l’entrée d’index à la position actuelle du curseur sur l’ancien index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Le moteur a épuisé son pool de ressources utilisé pour ouvrir les curseurs. Le nombre maximal de curseurs pouvant être ouverts à un moment donné est contrôlé à l’aide de <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>. Pour plus d’informations, consultez <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> . Cela peut se produire pour <strong>JetSetCurrentIndex</strong> lorsqu’un index secondaire a été sélectionné et que le moteur ne peut pas ouvrir un curseur interne pour utiliser cet index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p>Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, l’index actuel du curseur est défini sur l’index demandé. Les entrées d’index peuvent désormais être recherchées à l’aide de [JetSeek](./jetseek-function.md) en fonction de la définition d’index de l’index demandé. Les entrées d’index peuvent également être énumérées à l’aide de [JetMove](./jetmove-function.md) dans l’ordre spécifié par cette définition d’index. La position actuelle du curseur est définie sur la première entrée d’index de l’index (JET_bitMoveFirst) ou sur une entrée d’index spécifique qui est associée à la position actuelle du curseur sur l’ancien index (JET_bitNoMove). Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, l’index actuel et la position actuelle du curseur sont dans un État indéfini. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Notes

Si l’indicateur d’ID d’index est obsolète, l’API échoue simplement. Il n’existe pas de secours pour le nom de texte de l’index dans ce cas, car il peut s’agir d’un exemple. Ce secours doit être effectué manuellement par l’appelant de l’API.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetSetCurrentIndexW</strong> (Unicode) et <strong>JetSetCurrentIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetCurrentIndex]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
