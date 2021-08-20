---
description: 'En savoir plus sur : fonction JetDupCursor'
title: Fonction JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 011c8ba50ea708df93a0bb9b7f781e19391317676034434de67c61134ddff603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117891506"
---
# <a name="jetdupcursor-function"></a>Fonction JetDupCursor


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetdupcursor-function"></a>Fonction JetDupCursor

La fonction **JetDupCursor** duplique un curseur ouvert et retourne un descripteur au curseur dupliqué. Si le curseur qui était dupliqué était un curseur en lecture seule, le curseur dupliqué est également un curseur en lecture seule. Tout État lié à la construction d’une clé de recherche ou à la mise à jour d’un enregistrement n’est pas copié dans le curseur dupliqué. En outre, l’emplacement du curseur d’origine n’est pas dupliqué dans le curseur dupliqué. Le curseur dupliqué est toujours ouvert sur l’index cluster et son emplacement est toujours sur la première ligne de la table.

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pTableID*

Pointeur vers *TableID*.

*grbit*

Réservé pour un usage futur.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Il n’existe aucune ressource de curseur disponible.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, *pTableID* est défini sur un curseur dupliqué.

En cas d’échec, aucune modification n’est apportée. L’état de *TableID* est inchangé.

#### <a name="remarks"></a>Remarques

Le curseur dupliqué n’a pas l’état de curseur entier copié. L’emplacement du curseur dupliqué, y compris l’index actuel, est généralement différent du curseur donné. Le curseur dupliqué est toujours retourné sur l’index cluster et sur la première ligne de la table. Si la table est vide, le curseur dupliqué ne figure pas sur une ligne.

Les tables ouvertes avec **JetDupCursor** doivent généralement être fermées avec [JetCloseTable](./jetclosetable-function.md). L’exception à cette règle se produit lorsque **JetDupCursor** est appelé dans une transaction et que la transaction est restaurée (avec [JetRollback](./jetrollback-function.md)). Lors de la restauration d’une transaction, le curseur est automatiquement fermé. Dans ce cas, il s’agit d’une erreur de fermeture de la table avec [JetCloseTable](./jetclosetable-function.md).

Le nombre de tables pouvant être ouvertes simultanément est directement affecté par [JET_paramMaxOpenTables](./resource-parameters.md). Pour plus d’informations, consultez [paramètres système](./extensible-storage-engine-system-parameters.md) .

#### <a name="requirements"></a>Conditions requises

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p></td>
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

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
