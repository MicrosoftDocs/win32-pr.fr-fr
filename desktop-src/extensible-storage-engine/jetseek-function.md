---
description: 'En savoir plus sur : fonction JetSeek'
title: JetSeek fonction)
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520165"
---
# <a name="jetseek-function"></a>JetSeek fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetseek-function"></a>JetSeek fonction)

La fonction **JetSeek** positionne efficacement un curseur sur une entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et l’inégalité spécifiée. Une clé de recherche doit avoir été construite précédemment à l’aide de [JetMakeKey](./jetmakekey-function.md).

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*grbit*

Groupe de bits qui contient les options à utiliser pour cet appel. *Grbit* doit être différent de zéro et doit inclure une ou plusieurs des valeurs énumérées dans le tableau suivant.

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
<td><p>JET_bitCheckUniqueness</p></td>
<td><p>Un code d’erreur spécial, JET_wrnUniqueKey, est retourné s’il peut être déterminé de manière économique qu’il existe une seule entrée d’index correspondant à la clé de recherche.</p>
<p>Cette option est ignorée sauf si JET_bitSeekEQ est également spécifié.</p>
<p>Cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekEQ</p></td>
<td><p>Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui correspond exactement à la clé de recherche. Le début de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le premier enregistrement de cet index. Le début de l’index n’est pas le même que le bas de l’index, ce qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p>
<p>Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekGE</p></td>
<td><p>Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui est supérieure ou égale à une entrée d’index qui correspond exactement aux critères de recherche. Le début de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le premier enregistrement de cet index. Le début de l’index n’est pas le même que le bas de l’index, ce qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p>
<p>Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches de la fin de l’index.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekGT</p></td>
<td><p>Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui est supérieure à une entrée d’index qui correspond exactement aux critères de recherche. Le début de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le premier enregistrement de cet index. Le début de l’index n’est pas le même que le bas de l’index, ce qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p>
<p>Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches du début de l’index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekLE</p></td>
<td><p>Le curseur est positionné à l’entrée d’index la plus proche de la fin de l’index qui est inférieure ou égale à une entrée d’index qui correspond exactement aux critères de recherche. La fin de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le dernier enregistrement de cet index. La fin de l’index n’est pas identique à la fin de l’index, qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p>
<p>Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches du début de l’index.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekLT</p></td>
<td><p>Le curseur est positionné à l’entrée d’index la plus proche de la fin de l’index qui est inférieure à une entrée d’index qui correspond exactement aux critères de recherche. La fin de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le dernier enregistrement de cet index. La fin de l’index n’est pas identique à la fin de l’index, qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</p>
<p>Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches de la fin de l’index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIndexRange</p></td>
<td><p>Une plage d’index sera automatiquement configurée pour toutes les clés qui correspondent exactement à la clé de recherche. La plage d’index résultante est identique à celle qui aurait été créée par un appel à <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> avec les options JET_bitRangeInclusive et JET_bitRangeUpperLimit. Pour plus d’informations, consultez <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> .</p>
<p>Il s’agit d’une méthode pratique pour découvrir toutes les entrées d’index qui correspondent aux mêmes critères de recherche.</p>
<p>Cette option est ignorée sauf si JET_bitSeekEQ est également spécifié.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Cette fonction permet le retour de tout [JET_ERRs](./jet-err.md) défini dans cette API. Pour plus d’informations sur les erreurs jet, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
<td><p>L’opération s’est terminée avec succès.</p>
<p>Pour <strong>JetSeek</strong>, cela signifie qu’une entrée d’index correspondant exactement aux critères de recherche a été trouvée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p>Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyNotMade</p></td>
<td><p>Il n’existe pas de clé de recherche pour le curseur. <strong>JetSeek</strong> requiert que le curseur ait une clé de recherche valide, car il l’utilise pour les critères de recherche utilisés pour rechercher des entrées d’index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNotFound</p></td>
<td><p>Aucune entrée d’index correspondant aux critères de recherche n’a été trouvée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSeekNotEqual</p></td>
<td><p>Une entrée d’index correspondant aux critères de recherche a été trouvée. Toutefois, cette entrée d’index n’était pas une correspondance exacte.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p>Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnUniqueKey</p></td>
<td><p>Une seule entrée d’index a été trouvée et correspond exactement aux critères de recherche. Cette erreur est renvoyée uniquement si JET_bitSeekCheckUniqueness a été spécifiée et qu’elle était économique pour déterminer que l’entrée d’index correspondante était la seule entrée d’index qui correspond exactement aux critères de recherche.</p>
<p>Cette erreur est renvoyée uniquement par Windows Server 2003 et les versions ultérieures.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, le curseur est positionné au niveau d’une entrée d’index qui correspond aux critères de recherche. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur, cette plage d’index sera annulée. Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée. Aucune modification de l’état de la base de données ne se produit. Lorsque plusieurs entrées d’index ont la même valeur, l’entrée la plus proche du début de l’index est toujours sélectionnée.

En cas d’échec, la position du curseur reste inchangée, à moins que JET_errRecordNotFound ne soit retourné. Dans ce cas, le curseur est positionné à l’emplacement où l’entrée d’index qui correspondait aux critères de recherche spécifiés par la clé de recherche dans ce curseur et l’inégalité spécifiée aurait été. Le curseur peut être déplacé par rapport à cette position, mais il n’est pas toujours sur une entrée d’index valide. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur, cette plage d’index sera annulée. Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée. Aucune modification de l’état de la base de données ne se produit.

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
[JetMakeKey](./jetmakekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
