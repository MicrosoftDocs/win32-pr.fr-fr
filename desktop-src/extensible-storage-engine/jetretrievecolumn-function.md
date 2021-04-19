---
description: 'En savoir plus sur : fonction JetRetrieveColumn'
title: Fonction JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529427"
---
# <a name="jetretrievecolumn-function"></a>Fonction JetRetrieveColumn


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetretrievecolumn-function"></a>Fonction JetRetrieveColumn

La fonction **JetRetrieveColumn** récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur. Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur. Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif. En plus de récupérer la valeur réelle de la colonne, **JetRetrieveColumn** peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*ColumnID*

[JET_COLUMNID](./jet-columnid.md) de la colonne à récupérer.

Une valeur *ColumnID* égale à 0 (zéro) peut être fournie, qui ne fait pas référence à une colonne individuelle. Lorsque la valeur *ColumnID* 0 (zéro) est donnée, toutes les colonnes avec balises, éparses et les colonnes à valeurs multiples sont traitées comme une seule colonne. Cela facilite la récupération de toutes les colonnes éparses présentes dans un enregistrement.

*pvData*

Mémoire tampon de sortie qui reçoit la valeur de colonne.

*cbData*

Taille maximale, en octets, de la mémoire tampon de sortie.

*pcbActual*

Reçoit la taille réelle, en octets, de la valeur de colonne.

Si ce paramètre a la valeur **null**, la taille réelle de la valeur de colonne ne sera pas retournée.

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
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Cet indicateur force la récupération de la colonne à récupérer la valeur modifiée au lieu de la valeur d’origine. Si la valeur n’a pas été modifiée, la valeur d’origine est récupérée. De cette façon, une valeur qui n’a pas encore été insérée ou mise à jour peut être récupérée pendant l’opération d’insertion ou de mise à jour d’un enregistrement.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>Cette option permet de récupérer des valeurs de colonne à partir de l’index, si possible, sans accéder à l’enregistrement. De cette façon, le chargement inutile d’enregistrements peut être évité lorsque les données nécessaires sont disponibles à partir d’entrées d’index. Dans les cas où la valeur de colonne d’origine ne peut pas être récupérée à partir de l’index, en raison des transformations irréversibles ou de la troncation des données, l’enregistrement est accessible et les données sont récupérées comme normales. Il s’agit d’une option de performance qui doit être spécifiée uniquement lorsqu’il est probable que la valeur de colonne puisse être récupérée à partir de l’index. Cette option ne doit pas être spécifiée si l’index actuel est l’index cluster, étant donné que les entrées d’index de l’index cluster ou principal sont les enregistrements eux-mêmes. Ce bit ne peut pas être défini si JET_bitRetrieveFromPrimaryBookmark est également défini.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>Cette option est utilisée pour extraire des valeurs de colonne du signet d’index et peut différer de la valeur d’index lorsqu’une colonne apparaît à la fois dans l’index primaire et dans l’index actuel. Cette option ne doit pas être spécifiée si l’index actuel est l’index cluster ou principal. Ce bit ne peut pas être défini si JET_bitRetrieveFromIndex est également défini.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>Cette option permet de récupérer le numéro de séquence d’une valeur de colonne à valeurs multiples dans pretinfo- &gt; itagSequence. Le champ itagSequence est généralement une entrée permettant de récupérer des valeurs de colonnes à valeurs multiples à partir d’un enregistrement. Toutefois, lorsque vous récupérez des valeurs à partir d’un index, il est également possible d’associer l’entrée d’index à un numéro de séquence particulier et de récupérer également ce numéro de séquence. La récupération du numéro de séquence peut être une opération coûteuse et ne doit être effectuée que si nécessaire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveNull</p></td>
<td><p>Cette option permet de récupérer des valeurs <strong>null</strong> de colonne à valeurs multiples. Si cette option n’est pas spécifiée, les valeurs <strong>null</strong> de la colonne à valeurs multiples sont automatiquement ignorées.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>Cette option affecte uniquement les colonnes à valeurs multiples et entraîne le renvoi d’une valeur <strong>null</strong> lorsque le numéro de séquence demandé est 1 et qu’il n’existe aucune valeur définie pour la colonne dans l’enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>Cet indicateur est destiné à un usage interne uniquement et n’est pas destiné à être utilisé dans votre application.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>Cet indicateur est destiné à un usage interne uniquement et n’est pas destiné à être utilisé dans votre application.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveTuple</p></td>
<td><p>Cet indicateur permet la récupération d’un segment de tuple de l’index. Ce bit doit être spécifié avec JET_bitRetrieveFromIndex.</p></td>
</tr>
</tbody>
</table>


*pretinfo*

Si *pretinfo* a la **valeur null** , la fonction se comporte comme si un *ItagSequence* de 1 et un *ibLongValue* de 0 (zéro) ont été donnés. Ainsi, la récupération de colonne récupère la première valeur d’une colonne à valeurs multiples et récupère les données de type long à l’offset 0 (zéro).

Ce paramètre est utilisé pour fournir un ou plusieurs des éléments suivants :

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
<td><p>Donne un décalage binaire dans une valeur de colonne longue lors de l’extraction d’une partie d’une valeur de colonne.</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>Indique le numéro de séquence de la valeur de colonne à valeurs multiples souhaitée. Notez que ce champ est défini uniquement si le JET_bitRetrieveTag est spécifié. Dans le cas contraire, il n’est pas modifié.</p></td>
</tr>
<tr class="odd">
<td><p>columnidNextTagged</p></td>
<td><p>Retourne l’ID de colonne de la valeur de colonne retournée lors de l’extraction de toutes les colonnes balisées, éparses et à valeurs multiples à l’aide du passage de <em>ColumnID</em> égal à 0 (zéro).</p></td>
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
<td><p>JET_errBadItagSequence</p></td>
<td><p>Une valeur de numéro de séquence de colonne à valeurs multiples non valide a été transmise dans pretinfo- &gt; itagSequence. Les valeurs valides pour les numéros de séquence de valeur de colonne à valeurs multiples sont égales ou supérieures à 1. La valeur 0 (zéro) n’est pas valide pour cette fonction.</p></td>
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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Dans certains cas, la mémoire tampon donnée pour la colonne de récupération doit être suffisamment dimensionnée pour pouvoir retourner n’importe quel volume de la valeur de colonne. Par exemple, les colonnes pouvant être mises à jour par tiers de confiance sont ajustées pour être cohérentes pour le contexte transactionnel de la session appelante et cet ajustement requiert la mémoire tampon fournie par l’appelant. Si un espace de mémoire tampon insuffisant est fourni, JET_errInvalidBufferSize est retourné et aucune donnée de colonne n’est retournée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un ou plusieurs des paramètres spécifiés sont incorrects. Cela peut se produire si retinfo. cbStruct est plus petit que la taille de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Les options fournies sont inconnues ou une combinaison non conforme de paramètres de bits connus.</p></td>
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
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>La valeur de colonne Récupérée est <strong>null</strong>.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, la valeur de colonne pour la colonne donnée, est copiée dans la mémoire tampon donnée. Une valeur inférieure à toute la valeur de la colonne est copiée avec l’avertissement JET_wrnBufferTruncated est retourné. Si le *pcbActual* a été donné, la taille réelle de la valeur de colonne est retournée. Notez que les valeurs **null** ont une longueur de 0 (zéro) et, par conséquent, attribuez à la taille retournée la valeur 0 (zéro). Si la colonne Récupérée était une colonne à valeurs multiples et que la valeur de *pretinfo* a été spécifiée, et que JET_bitReturnTag a été défini en tant qu’option, le numéro de séquence de la valeur de colonne est retourné dans pretinfo- \> itagSequence.

En cas d’échec, l’emplacement du curseur reste inchangé et aucune donnée n’est copiée dans la mémoire tampon fournie.

#### <a name="remarks"></a>Notes

Cet appel est utilisé une seule fois pour récupérer des données de taille fixe ou connue pour des colonnes qui ne sont pas à valeurs multiples. Toutefois, lorsque les données de la colonne ont une taille inconnue, cet appel est généralement utilisé deux fois. Elle est appelée en premier pour déterminer la taille des données afin de pouvoir allouer l’espace de stockage nécessaire. Le même appel est ensuite refait pour récupérer les données de la colonne. Lorsque le nombre réel de valeurs est inconnu, car une colonne est à valeurs multiples, l’appel est généralement utilisé trois fois. Commencez par obtenir le nombre de valeurs, puis deux fois plus pour allouer le stockage et récupérer les données réelles.

La récupération de toutes les valeurs d’une colonne à valeurs multiples peut être effectuée en appelant à plusieurs reprises cette fonction avec une \> valeur pretinfo-itagSequence à partir de 1 et en accroissant à chaque appel suivant. La dernière valeur de colonne est connue pour être récupérée quand une JET_wrnColumnNull est retournée à partir de la fonction. Notez que cette méthode ne peut pas être effectuée si la colonne à valeurs multiples contient des valeurs **null** explicites définies dans sa séquence de valeurs, car ces valeurs sont ignorées. Si une application souhaite récupérer toutes les valeurs de colonne à valeurs multiples, y compris celles qui ont explicitement la valeur **null**, [JetRetrieveColumns](./jetretrievecolumns-function.md) doit être utilisé à la place de **JetRetrieveColumn**. Notez que cette fonction ne retourne pas le nombre de valeurs pour une fonction à valeurs multiples quand une valeur *itagSequence* égale à 0 (zéro) est donnée. Seul [JetRetrieveColumns](./jetretrievecolumns-function.md) retourne le nombre de valeurs d’une valeur de colonne lorsqu’une valeur *itagSequence* égale à 0 (zéro) est passée.

Si cette fonction est appelée au niveau de la transaction 0 (zéro), par exemple, la session appelante n’est pas elle-même dans une transaction, puis une transaction est ouverte et fermée dans la fonction. L’objectif est de retourner des résultats cohérents dans le cas où une valeur long s’étend sur des pages de base de données. Notez que la transaction est libérée entre les appels de fonction et une série d’appels à cette fonction lorsque la session n’est pas dans une transaction peut retourner des données mises à jour après le premier appel à cette fonction.

La valeur de colonne par défaut est récupérée lorsque la colonne n’a pas été définie explicitement sur une autre valeur, à moins que l’option JET_bitRetrieveIgnoreDefault soit définie.

La récupération de la valeur de colonne AutoIncrement à partir de la mémoire tampon de copie avant Insert est un moyen courant d’identifier un enregistrement de manière unique pour la liaison lors de l’insertion de données normalisées dans plusieurs tables. La valeur AUTOINCREMENT est allouée lorsque l’opération d’insertion commence et peut être récupérée à partir de la mémoire tampon de copie à tout moment jusqu’à ce que la mise à jour soit terminée.

Lors de la récupération de toutes les colonnes avec balises, à valeurs multiples et éparses, en affectant à *ColumnID* la valeur 0 (zéro), les colonnes sont récupérées dans l’ordre *ColumnID* , de la *plus petite à la plus ancienne* à *ColumnID*. Le même ordre des valeurs de colonne est retourné chaque fois que les valeurs de colonne sont récupérées. L’ordre est déterministe.

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
[JET_RETINFO](./jet-retinfo-structure.md)  
[JetSetColumn](./jetretrievekey-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
