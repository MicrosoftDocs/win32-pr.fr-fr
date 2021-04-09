---
description: 'En savoir plus sur : fonction JetUpdate'
title: Fonction JetUpdate
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38e17c5bc5ac32ab3b904456f2d97aa465fca670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862893"
---
# <a name="jetupdate-function"></a>Fonction JetUpdate


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetupdate-function"></a>Fonction JetUpdate

La fonction **JetUpdate** effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante. La suppression d’une ligne de table s’effectue en appelant [JetDelete](./jetdelete-function.md).

**JetUpdate** est la dernière étape de l’exécution d’une instruction INSERT ou Update. La mise à jour commence par appeler [JetPrepareUpdate](./jetprepareupdate-function.md) , puis en appelant [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md) une ou plusieurs fois pour définir l’état de l’enregistrement. Enfin, **JetUpdate** est appelé pour terminer l’opération de mise à jour. Les index sont mis à jour uniquement par **JetUpdate** ou [JetUpdate2](./jetupdate2-function.md), et non pendant [JetSetColumn](./jetsetcolumn-function.md) ou [JetSetColumns](./jetsetcolumns-function.md).

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pvBookmark*

Pointeur vers un signet retourné pour une ligne insérée.

*cbBookmark*

Taille de la mémoire tampon vers laquelle pointe *pvBookmark*.

*pcbActual*

Taille retournée du signet pour la ligne insérée retournée dans *pvBookmark*.

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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>La mémoire tampon donnée pour le signet d’enregistrement n’est pas suffisamment grande pour stocker le signet de l’enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identique à JET_errNullInvalid.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskFull</p></td>
<td><p>L’opération de mise à jour nécessite la croissance du fichier de base de données ou l’allocation des fichiers journaux, mais le lecteur de disque où se trouve le fichier de base de données ou la série de journaux est plein. Sinon, le fichier de base de données se trouve sur un volume au format FAT32 et le fichier de base de données est déjà 4GBytes, la limite par fichier pour FAT32.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Le paramètre <em>PREP</em> donné dans la fonction <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> n’est pas un indicateur valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyDuplicate</p></td>
<td><p>Une clé d’index pour cet enregistrement est un doublon d’une autre clé d’index pour un autre enregistrement déjà dans la table et l’index n’autorise pas les doublons.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyTruncated</p></td>
<td><p>L’enregistrement inséré ou mis à jour a un ou plusieurs index pour lesquels la clé générée aurait dépassé la taille maximale autorisée. Par conséquent, l’opération n’a pas pu empêcher la troncation de clé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedIndexViolation</p></td>
<td><p>L’enregistrement inséré ou mis à jour a une colonne à valeurs multiples indexée avec au moins deux valeurs qui sont identiques dans la taille de clé de longueur maximale définie pour l’index. Par conséquent, l’enregistrement a deux entrées identiques dans l’index, ce qui n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullInvalid</p></td>
<td><p>Une ou plusieurs colonnes de l’enregistrement à insérer ou à l’État mis à jour d’un enregistrement en cours de remplacement sont <strong>null</strong> , ce qui viole la contrainte définie pour ces colonnes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullKeyDisallowed</p></td>
<td><p>Un ou plusieurs index sont définis de façon à ne pas autoriser une clé <strong>null</strong> et l’état inséré ou mis à jour d’un enregistrement qui est remplacé viole cette contrainte définie.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordPrimaryChanged</p></td>
<td><p>Une opération de remplacement d’enregistrement a mis à jour la clé primaire. Les mises à jour des colonnes clés primaires doivent être effectuées par le biais de la suppression de l’enregistrement existant et de l’insertion d’un nouvel enregistrement avec les données souhaitées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Il n’est pas autorisé de tenter une mise à jour dans l’étendue d’une transaction en lecture seule. Une transaction en lecture seule est une transaction qui a été démarrée à l’aide d’un appel à <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> avec JET_bitTransactionReadOnly.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> a été appelé avec JET_prepCancel mais le curseur n’était pas dans l’état préparé.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>L’opération a échoué, car il n’y a pas assez de mémoire pour conserver les informations transactionnelles sur la mise à jour.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Une autre session a déjà verrouillé l’enregistrement pour la mise à jour. La mise à jour tentée par cette session échoue.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, l’opération d’ouverture de mise à jour sur le curseur est terminée. Si une colonne d’incrémentation automatique est définie pour la table, cette valeur est définie pour les enregistrements insérés. Si une colonne version est définie pour la table, sa valeur est initialisée pour les enregistrements nouvellement insérés, ou incrémentée chaque fois qu’un enregistrement est remplacé. Tous les index, y compris les index cluster et non cluster, sont mis à jour.

En cas d’échec, aucune modification de type n’est apportée à la base de données. Avant que les fonctions de rappel Insert et Before Replace aient été appelées, mais après l’appel d’insert et after Replace, les rappels n’auront pas été appelés, puisque ce dernier ne peut pas provoquer l’échec d’une mise à jour. Le tampon de copie de curseur reste dans son état préparé, afin que l’opportunité existe pour corriger de façon incrémentielle les problèmes qui ont provoqué des erreurs et retenter l’opération de mise à jour.

#### <a name="remarks"></a>Notes

Les fonctions de rappel peuvent être inscrites pour être appelées avant ou après l’insertion, et avant ou après la mise à jour.

Les limitations de taille d’enregistrement sont appliquées par [JetSetColumn](./jetsetcolumn-function.md), et non en général par **JetUpdate**.

Il est important de comprendre l’impact de l’exécution d’un grand nombre d’opérations de mise à jour au sein d’une même transaction. Chaque mise à jour de la base de données doit être suivie par le moteur de base de données dans la Banque des versions. La Banque des versions contient un enregistrement dynamique de toutes les différentes versions de chaque entrée d’enregistrement ou d’index dans la base de données qui peuvent être vues par toutes les transactions actives. Ces versions sont utilisées pour prendre en charge le contrôle d’accès concurrentiel multiversion utilisé par le moteur de base de données pour prendre en charge les transactions à l’aide de l’isolation d’instantané. Une fois que le moteur de base de données a épuisé les ressources utilisées pour stocker ces versions, il ne peut plus accepter de modifications tant que certaines transactions n’ont pas été terminées pour permettre la récupération de ces ressources. Lorsque le moteur est dans cet État, toutes les mises à jour échouent avec JET_errVersionStoreOutOfMemory. Les ressources disponibles pour le moteur de base de données pour stocker ces versions peuvent être contrôlées à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramMaxVerPages](./resource-parameters.md) et [JET_paramGlobalMinVerPages](./resource-parameters.md).

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
[JetDelete](./jetdelete-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[JetRegisterCallback](./jetregistercallback-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
