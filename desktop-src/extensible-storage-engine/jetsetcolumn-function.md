---
description: 'En savoir plus sur : fonction JetSetColumn'
title: Fonction JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538648"
---
# <a name="jetsetcolumn-function"></a>Fonction JetSetColumn


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetsetcolumn-function"></a>Fonction JetSetColumn

La fonction **JetSetColumn** modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou à mettre à jour l’enregistrement en cours. Elle peut remplacer une valeur existante, ajouter une nouvelle valeur à une séquence de valeurs dans une colonne à valeurs multiples, supprimer une valeur d’une séquence de valeurs dans une colonne à valeurs multiples, ou mettre à jour tout ou partie d’une valeur longue, une colonne de type [JET_coltypLongText](./jet-coltyp.md) ou [JET_coltypLongBinary](./jet-coltyp.md).

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*ColumnID*

[JET_COLUMNID](./jet-columnid.md) de la colonne à récupérer. Vous pouvez également donner une valeur *ColumnID* égale à 0 (zéro). Lorsque la valeur *ColumnID* 0 (zéro) est donnée, toutes les colonnes avec balises, les colonnes éparses et les colonnes à valeurs multiples, sont traitées comme une seule colonne. Cela facilite la récupération de toutes les colonnes éparses présentes dans un enregistrement.

*pvData*

Mémoire tampon d’entrée contenant les données à utiliser pour la valeur de colonne.

*cbData*

Taille en octets de la mémoire tampon d’entrée.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>Cette option est utilisée pour ajouter des données à une colonne de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>. Le même comportement peut être obtenu en déterminant la taille de la valeur longue existante et en spécifiant <em>ibLongValue</em> dans <em>psetinfo</em>. Toutefois, il est plus simple d’utiliser ce <em>Grbit</em> car le fait de connaître la taille de la valeur de colonne existante n’est pas nécessaire.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>Cette option est utilisée pour remplacer la valeur de type long existante par les données qui viennent d’être fournies. Lorsque cette option est utilisée, c’est comme si la valeur long existante ait été définie à 0 (zéro) avant de définir les nouvelles données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>Cette option s’applique uniquement aux colonnes avec balises, éparses ou à valeurs multiples. Elle fait en sorte que la colonne retourne la valeur de colonne par défaut lors des opérations de récupération de colonne suivantes. Toutes les valeurs de colonnes existantes sont supprimées.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>Cette option permet de forcer le stockage d’une valeur longue, de colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, séparément du reste des données d’enregistrement. Cela se produit normalement lorsque la taille de la valeur long l’empêche d’être stockée avec les données d’enregistrement restantes. Toutefois, cette option peut être utilisée pour forcer le stockage séparé de la valeur de type long. Notez que les valeurs longues de 4 octets de taille inférieure ne peuvent pas être forcées à être séparées. Dans ce cas, l’option est ignorée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>Cette option est utilisée pour interpréter la mémoire tampon d’entrée comme un nombre entier d’octets à définir comme longueur de la valeur longue décrite par le <em>ColumnID</em> donné et, le cas échéant, le numéro de séquence dans psetinfo- &gt; itagSequence. Si la taille donnée est supérieure à la valeur de colonne existante, la colonne est étendue avec 0. Si la taille est inférieure à la valeur de colonne existante, la valeur sera tronquée.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>Cette option permet d’imposer que toutes les valeurs d’une colonne à valeurs multiples soient distinctes. Cette option compare les données de la colonne source, sans aucune transformation, à d’autres valeurs de colonne existantes et une erreur est retournée si un doublon est trouvé. Si cette option est spécifiée, JET_bitSetAppendLV, JET_bitSetOverwriteLV et JET_bitSetSizeLV ne peuvent pas être spécifiés.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>Cette option permet d’imposer que toutes les valeurs d’une colonne à valeurs multiples soient distinctes. Cette option compare la transformation clé normalisée des données de colonne à d’autres valeurs de colonne existantes transformées de façon similaire, et une erreur est retournée si un doublon est trouvé. Si cette option est spécifiée, JET_bitSetAppendLV, JET_bitSetOverwriteLV et JET_bitSetSizeLV ne peuvent pas être spécifiés.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>Cette option est utilisée pour définir une valeur de longueur nulle. Normalement, une valeur de colonne est définie sur <strong>null</strong> en passant un cbMax de 0 (zéro). Toutefois, pour certains types, comme <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, une valeur de colonne peut avoir une longueur de 0 (zéro) au lieu de <strong>null</strong>, et cette option est utilisée pour différencier les <strong>valeurs NULL</strong> et 0 (zéro).</p>
<p><strong>Remarque</strong>  En général, si la colonne est une colonne de longueur fixe, ce bit est ignoré et la colonne est définie sur <strong>null</strong>. Toutefois, si la colonne est une colonne avec balises de longueur fixe, la longueur de la colonne est définie sur 0. Lorsque la colonne avec balises de longueur fixe a la valeur 0, les tentatives de récupération de la colonne avec <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ou <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> échouent, mais la longueur réelle qui est retournée dans le paramètre <em>cbActual</em> est 0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>Cette option permet de stocker la valeur longue entière dans l’enregistrement.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetCompressed</p></td>
<td><p>Cette option est utilisée pour tenter de compresser les données lors du stockage des données.</p>
<p><strong>Windows 7 :</strong>  JET_bitSetCompressed est introduite dans Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUncompressed</p></td>
<td><p>Cette option est utilisée pour ne pas tenter de compresser lors du stockage des données.</p>
<p><strong>Windows 7 :</strong>  JET_bitSetUnCompressed est introduite dans Windows 7.</p></td>
</tr>
</tbody>
</table>


*psetinfo*

Pointeur vers des paramètres d’entrée facultatifs qui peuvent être définis pour cette fonction à l’aide de la structure [JET_SETINFO](./jet-setinfo-structure.md) .

Si *psetinfo* est donné comme **null** , la fonction se comporte comme si un *ItagSequence* de 1 et un *ibLongValue* de 0 (zéro) ont été donnés. Cela amène le jeu de colonnes à définir la première valeur d’une colonne à valeurs multiples et à définir des données de type long en commençant à l’offset 0 (zéro).

Les options suivantes peuvent être définies pour ce paramètre :

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
<td><p>ibLongValue</p></td>
<td><p>Décalage binaire dans une valeur de colonne longue où les données de jeu doivent commencer.</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>Numéro de séquence de la valeur de colonne à valeurs multiples souhaitée à définir. Si <em>itagSequence</em> est défini sur 0 (zéro), la valeur fournie doit être ajoutée à la fin de la séquence de valeurs à valeurs multiples. Si le numéro de séquence fourni est supérieur à la dernière valeur à valeurs multiples existante, la valeur donnée est ajoutée à la fin de la séquence de valeurs. Si le numéro de séquence correspond à une valeur existante, cette valeur est remplacée par la valeur donnée.</p></td>
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
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadColumnId</p></td>
<td><p>L’ID de colonne indiqué est en dehors des limites autorisées d’un ID de colonne.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
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
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
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
<td><p>Une tentative non conforme a été effectuée pour définir une colonne non<strong>null</strong> à <strong>null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>Identique à JET_errNullInvalid.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>La valeur de la colonne n’a pas pu être définie sur la valeur dans la mémoire tampon d’entrée, car elle aurait provoqué un dépassement de la limite de taille liée à la taille de la page de l’enregistrement. Les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> peuvent être stockées séparément des données de l’enregistrement restant. Toutefois, les autres colonnes doivent être stockées avec l’enregistrement et peuvent entraîner le dépassement de la limite de taille des enregistrements. Même les colonnes longues nécessitent 5 octets d’espace dans l’enregistrement en tant que liaison, ce qui peut entraîner des JET_errRecordTooBig retournées.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Le curseur ne se trouve pas actuellement dans le processus d’insertion d’un nouvel enregistrement ou de mise à jour d’un enregistrement existant.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Cette erreur se produit lorsque la taille de la Banque des versions configurée est insuffisante pour contenir toutes les mises à jour en suspens.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>La valeur de colonne dans la mémoire tampon d’entrée a dépassé la longueur maximale configurée pour une colonne de longueur variable et a été tronquée.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, la partie souhaitée d’une valeur de colonne pour la colonne donnée est définie avec les données copiées à partir de la mémoire tampon d’entrée. Le jeu de données a peut-être été tronqué s’il dépasse la longueur maximale spécifiée pour une colonne de longueur variable.

En cas d’échec, l’emplacement du curseur reste inchangé et aucune donnée de valeur de colonne n’est mise à jour dans le tampon de copie.

#### <a name="remarks"></a>Notes

En définissant des valeurs longues, les valeurs des colonnes [JET_coltypLongBinary](./jet-coltyp.md) de type [JET_coltypLongText](./jet-coltyp.md) ou [JET_coltypLongBinary](./jet-coltyp.md)doivent être effectuées uniquement lorsque la session appelante est dans une transaction. Si la session appelante n’est pas dans une transaction, les modifications apportées aux valeurs longues qui sont stockées séparément peuvent être validées entièrement même lorsque l’opération de mise à jour est annulée ultérieurement. Si la session appelante est dans une transaction, les effets de la mise à jour peuvent être entièrement annulés en annulant la mise à jour et en restaurant la transaction de session.

Les mises à jour d’index ne sont pas effectuées suite à des opérations **JetSetColumn** . Au lieu de cela, les index sont mis à jour uniquement une fois que toutes les modifications de colonne sont terminées et [JetUpdate](./jetupdate-function.md) est appelé. Cela permet la mise à jour la plus efficace des index lorsque des index impliquent la modification de plusieurs colonnes.

La taille d’un enregistrement est limitée en fonction de la taille de la page de base de données. Toute valeur de type long de l’enregistrement supérieur à cinq octets est stockée séparément de l’enregistrement si les données de l’enregistrement dépassent la limite résultant d’une opération **JetSetColumn** . Le JET_errRecordTooBig d’erreur est renvoyé uniquement une fois que toutes les données de colonne d’enregistrement séparable ont été stockées séparément de l’enregistrement et que l’enregistrement dépasse la limite de taille d’enregistrement.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
