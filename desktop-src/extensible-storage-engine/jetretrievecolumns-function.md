---
description: 'En savoir plus sur : fonction JetRetrieveColumns'
title: Fonction JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210377"
---
# <a name="jetretrievecolumns-function"></a>Fonction JetRetrieveColumns


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetretrievecolumns-function"></a>Fonction JetRetrieveColumns

La fonction **JetRetrieveColumns** Récupère plusieurs valeurs de colonne de l’enregistrement actuel en une seule opération. Un tableau de structures de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) est utilisé pour décrire l’ensemble des valeurs de colonne à récupérer et pour décrire les mémoires tampons de sortie pour chaque valeur de colonne à récupérer.

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*pretrievecolumn*

Pointeur vers un tableau d’une ou plusieurs structures de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Chaque structure comprend des descriptions de la valeur de colonne à récupérer et de l’emplacement de stockage des données retournées.

*cretrievecolumn*

Nombre de structures de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) dans le tableau donné par *pretrievecolumn*.

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
<td><p>Une valeur de numéro de séquence de colonne à valeurs multiples non valide a été transmise dans pretinfo- &gt; itagSequence. Les valeurs valides pour les numéros de séquence de valeur de colonne à valeurs multiples sont égales ou supérieures à 1. La valeur 0 (zéro) est valide pour cette fonction, mais n’est pas valide pour <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>L’ID de colonne indiqué est en dehors des limites autorisées d’un ID de colonne.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonne décrite par le <em>ColumnID</em> donné n’existe pas dans la table.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex</p></td>
<td><p>Les colonnes indexées en tant que sous-chaînes ne peuvent pas être récupérées à partir de l’index, car seule une petite partie de la colonne est généralement présente dans chaque entrée d’index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Dans certains cas, la mémoire tampon donnée pour la colonne de récupération doit être suffisamment dimensionnée pour pouvoir retourner n’importe quel volume de la valeur de colonne. Par exemple, les colonnes pouvant être mises à jour par tiers de confiance sont ajustées pour être cohérentes pour le contexte transactionnel de la session appelante et cet ajustement requiert la mémoire tampon fournie par l’appelant. Si un espace de mémoire tampon insuffisant est fourni, JET_errInvalidBufferSize est retourné et aucune donnée de colonne n’est retournée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Les options fournies sont inconnues ou une combinaison non conforme de paramètres de bits connus.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un ou plusieurs des paramètres spécifiés sont incorrects. Cela peut se produire si retinfo. cbStruct est plus petit que la taille de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Le curseur n’est pas positionné sur un enregistrement. Cela peut se produire pour de nombreuses raisons différentes. Par exemple, cela se produit si le curseur est actuellement positionné après le dernier enregistrement de l’index actuel.</p></td>
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
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>Impossible de récupérer la valeur de colonne entière, car la taille de la mémoire tampon donnée est inférieure à celle de la colonne.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, les données de colonnes et la taille de colonne sont retournées dans les mémoires tampons fournies décrites dans tableau de structures de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) . Si un *itagSequence* a été défini sur 0 (zéro) pour indiquer que le nombre d’instances d’un champ à valeurs multiples était souhaité à la place des données de colonne, le nombre d’instances d’une colonne à valeurs multiples est retourné dans le champ *itagSequence* lui-même. Chaque structure de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) a un champ d’erreur qui contient des avertissements pour la colonne récupérée. Si la colonne a une valeur **null** , le code d’erreur est défini sur JET_wrnColumnNull.

En cas d’échec, l’emplacement du curseur reste inchangé et aucune donnée n’est copiée dans la mémoire tampon fournie.

#### <a name="remarks"></a>Notes

**JetRetrieveColumns** prend en charge une fonctionnalité que [JetRetrieveColumn](./jetretrievecolumn-function.md) ne fait pas. Il s’agit de la possibilité de récupérer le nombre d’instances d’une colonne à valeurs multiples. L’objectif de cette fonctionnalité est de permettre à une application de récupérer toutes les valeurs d’une colonne. Pour ce faire, vous devez d’abord déterminer le nombre de valeurs d’une colonne. Ensuite, leur longueur peut être déterminée en appelant à nouveau **JetRetrieveColumns** avec une structure [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) allouée pour chaque valeur afin de déterminer la longueur des données de la colonne. Pour ce faire, vous pouvez passer des pointeurs _PvData_ **null** avec *cbMax* de 0 (zéro) et récupérer la longueur de colonne dans *cbActual*. Le troisième et le dernier appel peuvent être effectués avec la mémoire allouée pour les données de valeur de colonne.

Si une colonne Récupérée est tronquée en raison d’une mémoire tampon de longueur insuffisante, l’API retourne JET_wrnBufferTruncated. Toutefois, d’autres erreurs, JET_wrnColumnNull sont retournées uniquement dans le champ d’erreur de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). Cela est dû au fait que les applications veulent souvent s’assurer que toutes les données ont été récupérées et que le retour de cette erreur à partir de **JetRetrieveColumns** facilite cette compréhension.

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
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
