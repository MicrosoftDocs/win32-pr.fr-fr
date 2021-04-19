---
description: 'En savoir plus sur : fonction JetGetCursorInfo'
title: JetGetCursorInfo fonction)
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523068"
---
# <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgetcursorinfo-function"></a>JetGetCursorInfo fonction)

La fonction **JetGetCursorInfo** est utilisée pour déterminer si une mise à jour de l’enregistrement en cours d’un curseur entraîne un conflit d’écriture, en fonction de l’état de mise à jour actuel de l’enregistrement. Il est possible qu’un conflit d’écriture soit retourné, même si **JetGetCursorInfo** retourne JET_errSuccess, car une autre session peut mettre à jour l’enregistrement avant que la session actuelle puisse mettre à jour le même enregistrement.

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session qui sera utilisée pour cet appel.

*TableID*

Curseur qui sera utilisé pour cet appel.

*pvResult*

Réservé pour un usage futur.

*cbMax*

Doit être défini sur 0 (zéro), sinon inutilisé. Il est présent pour les fonctionnalités futures.

*InfoLevel*

Doit être défini sur 0 (zéro), sinon inutilisé. Il est présent pour les fonctionnalités futures.

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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p><em>CbMax</em> n’est pas égal à 0 (zéro) ou <em>InfoLevel</em> n’est pas égal à 0 (zéro).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Le curseur ne se trouve pas actuellement sur un enregistrement et les informations sur un enregistrement logique ne peuvent pas être retournées en conséquence.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflict</p></td>
<td><p>L’enregistrement actuel du curseur a été mis à jour par une autre session et une mise à jour de cet enregistrement par cette session entraîne un conflit d’écriture.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, cette opération n’a aucun effet sur l’emplacement du curseur, mais indique uniquement qu’aucune autre session n’a actuellement mis à jour cet enregistrement.

En cas d’échec, si un code d’erreur négatif est retourné, il n’y a aucun effet sur le curseur ou la base de données.

#### <a name="remarks"></a>Notes

Cette opération n’affecte pas l’état du curseur ou des données. Elle retourne uniquement un code d’erreur qui décrit si une mise à jour de l’enregistrement en cours par la session appelante est connue pour générer un JET_errWriteConflict ou est inconnue pour retourner JET_errWriteConflict. Si une autre session a déjà mis à jour cet enregistrement pour l’utiliser, il est certain qu’une mise à jour de cet enregistrement par cette session entraîne un conflit d’écriture. La valeur est true jusqu’à ce que cette session valide ou restaure ses transactions au niveau de la transaction 0 (zéro). Toutefois, si **JetGetCursorInfo** retourne JET_errSuccess, il est toujours possible pour une autre session de mettre à jour cet enregistrement avant la session active. il est donc toujours possible qu’une mise à jour de l’enregistrement actif par cette session dans sa transaction actuelle entraîne un conflit d’écriture.

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetLock](./jetgetlock-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetStopService](./jetstopservice-function.md)  
[JetUpdate](./jetupdate-function.md)
