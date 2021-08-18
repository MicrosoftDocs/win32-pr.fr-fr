---
description: 'En savoir plus sur : fonction JetGotoBookmark'
title: JetGotoBookmark fonction)
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 56e94339a49cc80e8b7b416e89efc5c85079981e0430f325e29f1dd711eef63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978998"
---
# <a name="jetgotobookmark-function"></a>JetGotoBookmark fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgotobookmark-function"></a>JetGotoBookmark fonction)

La fonction **JetGotoBookmark** positionne un curseur sur une entrée d’index pour l’enregistrement associé au signet spécifié. Le signet peut être utilisé avec n’importe quel index défini sur une table. Le signet d’un enregistrement peut être récupéré à l’aide de [JetGetBookmark](./jetgetbookmark-function.md).

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pvBookmark*

Mémoire tampon qui contient le signet à utiliser pour positionner le curseur.

*cbBookmark*

Taille du signet dans la mémoire tampon.

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
<td><p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :</strong>   cette valeur de retour a été introduite dans Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>Le signet fourni n’est pas valide. Cela peut être dû au fait que la taille du signet est égale à zéro ou que le pointeur de la mémoire tampon du signet a la <strong>valeur null</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Le curseur se trouve sur un index secondaire et aucune entrée d’index n’a été trouvée pour l’enregistrement associé au signet.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>L’enregistrement associé au signet est introuvable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p><strong>Windows XP :</strong>   cette valeur de retour a été introduite dans Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


Si cette fonction est réussie, le curseur est positionné sur une entrée d’index pour l’enregistrement associé au signet spécifié. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur, cette plage d’index sera annulée. Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée. Aucune modification de l’état de la base de données ne se produit.

Si cette fonction échoue, la position du curseur reste inchangée. Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée. Si une plage d’index est en vigueur, cette plage d’index sera annulée. Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Il existe deux façons d’utiliser un signet pour positionner un curseur sur un index. La première consiste à utiliser le signet pour positionner directement sur l’enregistrement. Cela se produit lorsque l’index actuel du curseur est l’index primaire. Cette technique fonctionne, car un signet ESENT est le même que la clé primaire de l’enregistrement associé.

La deuxième façon d’utiliser un signet est de le positionner sur une entrée dans un index secondaire qui correspond à l’enregistrement associé à ce signet. Pendant ce processus, le moteur recherche l’enregistrement réel à l’aide du signet sur l’index primaire. Il utilise ensuite les données d’enregistrement et la définition d’index secondaire pour calculer une clé dans l’index secondaire qui pointe vers l’enregistrement. Il positionne ensuite le curseur sur l’entrée d’index pour cette clé. Si le curseur se trouve actuellement sur un index secondaire sur une ou plusieurs colonnes clés à valeurs multiples, le curseur est positionné sur l’entrée d’index correspondant à la première valeur multiple de chacune de ces colonnes clés.

#### <a name="requirements"></a>Configuration requise

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

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)
