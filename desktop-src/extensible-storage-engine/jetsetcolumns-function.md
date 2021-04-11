---
description: 'En savoir plus sur : fonction JetSetColumns'
title: Fonction JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112043"
---
# <a name="jetsetcolumns-function"></a>Fonction JetSetColumns


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetsetcolumns-function"></a>Fonction JetSetColumns

Le comportement de la fonction **JetSetColumns** est similaire à celui de [JetSetColumn](./jetsetcolumn-function.md) , mais permet à une application de définir plusieurs valeurs de colonne en une seule opération. Un tableau de structures de [JET_SETCOLUMN](./jet-setcolumn-structure.md) est utilisé pour décrire l’ensemble des valeurs de colonne à définir, et pour décrire les mémoires tampons d’entrée pour chaque valeur de colonne à définir.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*psetcolumn*

Pointeur vers un tableau d’une ou plusieurs structures de [JET_SETCOLUMN](./jet-setcolumn-structure.md) . Chaque structure comprend des descriptions de la valeur de colonne à définir et de l’emplacement où les données de colonne doivent être définies.

*csetcolumn*

Nombre de structures de [JET_SETCOLUMN](./jet-setcolumn-structure.md) dans le tableau donné par *psetcolumn*.

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
<td><p>JET_errBadColumnId</p></td>
<td><p>L’ID de colonne indiqué est en dehors des limites autorisées d’un ID de colonne.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identique à JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonne décrite par le <em>ColumnID</em> donné n’existe pas dans la table.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable</p></td>
<td><p>Une tentative non conforme a été effectuée pour mettre à jour une valeur long pendant une opération de mise à jour d’origine de la suppression d’une copie Insert.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig</p></td>
<td><p>Les données de la valeur de colonne donnée dans la mémoire tampon d’entrée dépassent la limite de taille naturelle pour une colonne de longueur fixe ou configurée pour le texte de longueur fixe ou les colonnes binaires. Cette erreur est également retournée lors du passage de plus de 1024 octets de données pour une longue colonne et de la définition de l’indicateur de JET_bitSetIntrinsicLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>La taille de données de la valeur de colonne donnée ne correspond pas à ce qui est naturel pour le type de données de longueur fixe.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Une tentative non conforme a été effectuée pour mettre à jour une colonne à incrémentation automatique pendant une opération d’insertion ou de mise à jour, ou pour mettre à jour une colonne de version pendant une opération de remplacement.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Les options fournies sont inconnues ou une combinaison non conforme de paramètres de bits connus.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Le psetinfo- &gt; cbStruct donné n’est pas une taille valide pour la structure <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate</p></td>
<td><p>L’opération de définition de colonne a tenté de créer une valeur dupliquée et spécifiée soit JET_bitSetUniqueMultiValues, soit JET_bitSetUniqueNormalizedMultiValues.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Une tentative non conforme a été effectuée pour mettre à jour une valeur de colonne longue lorsque la session appelante n’était pas dans une transaction.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Une tentative non conforme a été effectuée pour définir une colonne non NULL à NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>La valeur de la colonne n’a pas pu être définie sur la valeur dans la mémoire tampon d’entrée, car elle aurait provoqué un dépassement de la limite de taille liée à la taille de la page de l’enregistrement. Les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> peuvent être stockées séparément des données de l’enregistrement restant. Toutefois, les autres colonnes doivent être stockées avec l’enregistrement et peuvent entraîner le dépassement de la limite de taille des enregistrements. Même les colonnes longues nécessitent 5 octets d’espace dans l’enregistrement en tant que liaison, ce qui peut entraîner des JET_errRecordTooBig retournées.</p></td>
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
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Le curseur ne se trouve pas actuellement dans le processus d’insertion d’un nouvel enregistrement ou de mise à jour d’un enregistrement existant.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>La valeur de colonne dans la mémoire tampon d’entrée a dépassé la longueur maximale configurée pour une colonne de longueur variable et a été tronquée.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, pour chaque colonne décrite dans psetcolumns, la partie souhaitée de la valeur de colonne est définie avec les données copiées à partir de la mémoire tampon d’entrée. Le jeu de données de la colonne a peut-être été tronqué s’il dépasse la longueur maximale spécifiée pour une colonne de longueur variable.

En cas d’échec, l’emplacement du curseur reste inchangé et aucune donnée de valeur de colonne n’est mise à jour dans le tampon de copie.

#### <a name="remarks"></a>Notes

Si une opération de définition de colonne individuelle retourne une erreur, la totalité de l’opération de **JetSetColumns** retourne une erreur. Des avertissements, en général, sont retournés dans l' \> erreur psetcolumns et non dans le code de retour de cette fonction. Toutefois, si le dernier jeu de colonnes a un avertissement, cet avertissement est retourné à partir de **JetSetColumns** lui-même.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
