---
description: 'En savoir plus sur : fonction JetDelete'
title: Fonction JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541902"
---
# <a name="jetdelete-function"></a>Fonction JetDelete


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetdelete-function"></a>Fonction JetDelete

La fonction **JetDelete** supprime l’enregistrement en cours dans une table de base de données.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de session de base de données qui sera utilisé pour l’appel d’API.

*TableID*

Curseur sur une table de base de données. La ligne actuelle sera supprimée.

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
<td><p>JET_errCallbackFailed</p></td>
<td><p>La fonction de rappel a échoué de quelque manière que ce soit. Par exemple, les violations d’accès dans les fonctions de rappel sont interceptées et converties en JET_errCallbackFailed. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation</p></td>
<td><p>Le curseur spécifié par <em>TableID</em> ne prend pas en charge la suppression. Consultez la section Notes.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Le curseur spécifié par <em>TableID</em> n’est pas sur un enregistrement.</p></td>
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
<td><p>JET_errPermissionDenied</p></td>
<td><p>Le moteur de base de données ne dispose pas des autorisations suffisantes pour supprimer l’enregistrement. Cela peut se produire si le fichier de base de données a été ouvert avec un accès en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackError</p></td>
<td><p>Une mémoire tampon de mise à jour (consultez <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) existe, mais toutes les modifications apportées aux colonnes de type JET_coltypLongText et/ou les colonnes de type JET_coltypLongBinary peuvent être restaurées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Il n’est pas conforme d’utiliser la même session à partir de plusieurs threads en même temps. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>La transaction est une transaction en lecture seule et ne prend pas en charge les suppressions.</p></td>
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


En cas de réussite, la devise est conservée juste avant l’enregistrement suivant. Si l’enregistrement supprimé était le dernier dans la table, la devise est laissée à la fin de la table (autrement dit, après le nouveau dernier enregistrement). Si l’enregistrement supprimé était le seul enregistrement dans la table, la devise est définie au début.

Les index appropriés sont automatiquement mis à jour.

Si une mise à jour est préparée (à l’aide de [JetPrepareUpdate](./jetprepareupdate-function.md)), elle sera annulée. La mémoire tampon de mise à jour sera réinitialisée.

En cas d’échec, la devise reste inchangée. Si une mise à jour est préparée (voir [JetPrepareUpdate](./jetprepareupdate-function.md)), la mémoire tampon de mise à jour peut être réinitialisée.

#### <a name="remarks"></a>Notes

Toutes les tables ne prennent pas en charge la suppression de lignes. Une table temporaire ne prend normalement pas en charge la suppression de lignes. La suppression des enregistrements peut être activée sur les tables temporaires pour de nombreuses raisons, dont certaines sont :

  - JET_bitTTUpdatable a été spécifié lors de la création.

  - Les tables temporaires volumineuses peuvent prendre en charge la suppression si elles ont été créées avec JET_bitTTScrollable ou JET_bitTTIndexed. Le seuil auquel une table temporaire devient « grande » est actuellement de 64 kilo-octets, mais elle peut être modifiée dans les versions ultérieures.

Windows XP et versions ultérieures. Les fonctions de rappel peuvent être appelées par **JetDelete**, y compris JET_cbtypBeforeDelete et JET_cbtypAfterDelete.

Il est important de comprendre l’impact de l’exécution d’un grand nombre d’opérations de mise à jour au sein d’une même transaction. Chaque mise à jour de la base de données doit être suivie par le moteur de base de données dans la Banque des versions. La Banque des versions contient un enregistrement dynamique de toutes les différentes versions de chaque entrée d’enregistrement ou d’index dans la base de données qui peuvent être vues par toutes les transactions actives. Ces versions sont utilisées pour prendre en charge le contrôle d’accès concurrentiel multiversion utilisé par le moteur de base de données pour prendre en charge les transactions à l’aide de l’isolation d’instantané. Une fois que le moteur de base de données a épuisé les ressources utilisées pour stocker ces versions, il ne peut plus accepter de modifications tant que certaines transactions n’ont pas été terminées pour permettre la récupération de ces ressources. Lorsque le moteur est dans cet État, toutes les mises à jour échouent avec JET_errVersionStoreOutOfMemory. Les ressources disponibles pour le moteur de base de données pour stocker ces versions peuvent être contrôlées à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec *JET_paramMaxVerPages* et *JET_paramGlobalMinVerPages*.

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
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetPrepareUpdate](./jetprepareupdate-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
