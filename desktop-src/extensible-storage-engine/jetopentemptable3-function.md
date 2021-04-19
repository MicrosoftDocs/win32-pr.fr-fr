---
description: 'En savoir plus sur : fonction JetOpenTempTable3'
title: Fonction JetOpenTempTable3
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7820f90ef0192c1f700759835bf1572b187cf3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514570"
---
# <a name="jetopentemptable3-function"></a>Fonction JetOpenTempTable3


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetopentemptable3-function"></a>Fonction JetOpenTempTable3

La fonction **JetOpenTempTable3** crée une table temporaire avec un index unique qui peut être utilisé pour stocker et récupérer des enregistrements comme une table ordinaire créée à l’aide de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile. Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*prgcolumndef*

Identifie les définitions de colonne des colonnes à créer dans la table temporaire.

Il existe des limitations importantes pour les options de définition de colonne qui peuvent être utilisées avec une table temporaire. Pour plus d'informations, consultez la section Notes.

Outre les options de définition de colonne habituelles, aucune ou plusieurs des options suivantes peuvent également être spécifiées qui ne sont pertinentes que dans le contexte d’une table temporaire.

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
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Cette option indique que l’ordre de tri de la colonne clé pour la table temporaire doit être décroissant plutôt que croissant. Si cette option est spécifiée sans JET_bitColumnTTKey, cette option est ignorée.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Cette option indique que la colonne sera une colonne clé pour la table temporaire.</p>
<p>L’ordre des définitions de colonne avec cette option spécifiée dans le tableau d’entrée détermine la précédence de chaque colonne clé pour la table temporaire. La première définition de colonne dans le tableau avec cette option est définie sur la colonne clé la plus significative, et ainsi de suite. Si le moteur de base de données demande plus de colonnes clés que ce qui peut être pris en charge par le moteur de base de données, cette option est ignorée pour les colonnes clés non prises en charge.</p></td>
</tr>
</tbody>
</table>


*ccolumn*

Consultez *prgcolumndef*.

*pidxunicode*

ID de paramètres régionaux et indicateurs de normalisation qui seront utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire.

Lorsque ce paramètre n’est pas présent, le LCID par défaut est utilisé pour comparer les colonnes clés Unicode de la table temporaire. Le LCID par défaut est le paramètre régional anglais (États-Unis).

Lorsque ce paramètre n’est pas présent, les indicateurs de normalisation par défaut sont utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire. Les indicateurs de normalisation par défaut sont les suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.

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
<td><p>JET_bitTTErrorOnDuplicateInsertion</p></td>
<td><p>Cette option demande que toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échoue avec JET_errKeyDuplicate. Si cette option n’est pas demandée, un doublon peut être détecté immédiatement et échouer ou peut être supprimé en mode silencieux ultérieurement selon la stratégie choisie par le moteur de base de données pour implémenter la table temporaire en fonction de la fonctionnalité demandée.</p>
<p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTForceMaterialization</p></td>
<td><p>Cette option force le gestionnaire de tables temporaires à abandonner toute tentative de choix d’une stratégie astucieuse pour la gestion de la table temporaire qui entraîne des performances améliorées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTForwardOnly</p></td>
<td><p>Cette option demande que la table temporaire soit créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation optimisée pour les résultats de requête intermédiaires. Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</p>
<p>L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées. Pour plus d’informations, consultez JET_bitTTUnique.</p>
<p>Cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTIndexed</p></td>
<td><p>Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de <a href="gg294103(v=exchg.10).md">JetSeek</a> pour rechercher des enregistrements par clé d’index.</p>
<p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTUnique</p></td>
<td><p>Cette option demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire.</p>
<p>Avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques. À compter de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons lorsque l’option JET_bitTTForwardOnly est également spécifiée.</p>
<p>Il n’est pas possible de savoir quels doublons seront remportés et quels doublons seront ignorés en général. Toutefois, lorsque l’option JET_bitTTErrorOnDuplicateInsertion est demandée, alors le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire est toujours gagnant.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTUpdatable</p></td>
<td><p>Cette option demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment. Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</p>
<p>Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTScrollable</p></td>
<td><p>Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>.</p>
<p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTTSortNullsHigh</p></td>
<td><p>Cette option demande que les valeurs de colonne clé NULL soient triées plus près de la fin de l’index que les valeurs de colonne clé non NULL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTTIntrinsicLVsOnly</p></td>
<td><p>Demande d’autoriser uniquement les valeurs longues intrinsèques.</p>
<p><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> est introduite dans Windows 7.</p></td>
</tr>
</tbody>
</table>


*pTableID*

Mémoire tampon de sortie qui recevra le nouveau curseur ouvert sur la table temporaire nouvellement créée.

*prgcolumnid*

Mémoire tampon de sortie qui recevra le tableau d’ID de colonne générés au cours de la création de la table temporaire.

Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne. Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.

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
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>JetOpenTempTable3</strong> a échoué parce que JET_bitTTForwardOnly a été spécifié et que la table temporaire spécifiée n’a pas pu être créée à l’aide de l’optimisation avant uniquement. Cette erreur est renvoyée uniquement par Windows Server 2003 et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Impossible de créer l’index, car une définition d’index non valide a été spécifiée. <strong>JetOpenTempTable3</strong> renvoie cette erreur dans les cas suivants :</p>
<ul>
<li><p>Les paramètres régionaux de langue neutre sont spécifiés.</p></li>
<li><p>Un ensemble non valide d’indicateurs de normalisation est spécifié.</p></li>
</ul>
<p>Cette erreur est renvoyée uniquement par Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Le membre <strong>CP</strong> de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Le membre <strong>coltyp</strong> de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur un type de colonne valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Impossible de créer l’index, car une tentative d’utilisation d’un ID de paramètres régionaux non valide a été effectuée. L’ID de paramètres régionaux peut être entièrement non valide ou le module linguistique associé n’est peut-être pas installé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Impossible de créer l’index, car une tentative d’utilisation d’un ensemble non valide d’indicateurs de normalisation a été effectuée. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures. Sur Windows 2000, les indicateurs de normalisation non valides génèrent JET_errIndexInvalidDef à la place.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Le descripteur de session n’est pas valide ou fait référence à une session fermée. Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur. Les ressources de curseur sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>L’opération a échoué, car la mémoire peut être allouée pour être terminée.</p>
<p><strong>JetOpenTempTable3</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté. Le gestionnaire de tables temporaire allouera toujours un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données à stocker.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
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
<td><p>JET_errTooManyColumns</p></td>
<td><p>Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée. Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache les index de la table. Le nombre d’index dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache le schéma de la table. Le nombre de tables dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour créer une table temporaire. Les ressources de table temporaire sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, un curseur ouvert sur la table temporaire nouvellement créée est retourné. L’état de la base de données temporaire sera préparé à contenir la nouvelle table temporaire. L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.

En cas d’échec, la table temporaire n’est pas créée et un curseur n’est pas renvoyé. L’état de la base de données temporaire peut être modifié. L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.

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

[Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md)  
[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
