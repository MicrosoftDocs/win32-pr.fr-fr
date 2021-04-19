---
description: 'En savoir plus sur : fonction JetOpenTemporaryTable'
title: JetOpenTemporaryTable fonction)
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522122"
---
# <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable fonction)

La fonction **JetOpenTemporaryTable** crée une table volatile avec un index unique qui peut être utilisé pour stocker et récupérer des enregistrements, tout comme une table ordinaire créée via [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).

**Windows Vista :**  **JetOpenTemporaryTable** est introduit dans Windows Vista.

Les tables temporaires sont plus rapides que les tables ordinaires en raison de leur nature volatile. Ils peuvent rapidement trier et effectuer la suppression des doublons sur les jeux d’enregistrements lorsqu’ils sont accessibles de manière purement séquentielle.

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session qui sera utilisée pour cet appel.

*popentemporarytable*

Pointeur vers une structure [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md) qui contient la description de la table temporaire à créer en entrée. Après un appel réussi, la structure contient le handle vers les identifications de la table et de la colonne temporaires.

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>L’opération a échoué, car la mémoire peut être allouée pour être terminée.</p>
<p><strong>JetOpenTemporaryTable</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté. Le gestionnaire de tables temporaire alloue un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données stockées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a entraîné un résultat inattendu.</p>
<p>Cette erreur est retournée par <strong>JetOpenTemporaryTable</strong> dans les conditions suivantes :</p>
<ul>
<li><p>Le membre <strong>cbStruct</strong> de la structure <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> ne correspond pas à une version de cette structure qui est prise en charge par cette version du moteur de base de données.</p></li>
<li><p>Le membre <strong>cbKeyMost</strong> de la structure <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> est inférieur à JET_cbKeyMostMin.</p></li>
<li><p>Le membre <strong>cbKeyMost</strong> de la structure <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> est plus grand que la plus grande valeur prise en charge pour la taille de page de la base de données de l’instance (JET_paramDatabasePageSize). Pour plus d’informations, consultez le paramètre JET_paramKeyMost dans la liste des <a href="gg269241(v=exchg.10).md">paramètres d’information</a> .</p></li>
<li><p>Le membre cbVarSegMac de la structure <a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a> est plus grand que le membre <strong>cbKeyMost</strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance qui a été associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Le descripteur de session n’est pas valide ou fait référence à une session fermée.</p>
<p><strong>Remarque</strong>  Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur. Les ressources de curseur sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour créer une table temporaire. Les ressources de table temporaire sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>JetOpenTemporaryTable</strong> a échoué parce que JET_bitTTForwardOnly a été spécifié et que la table temporaire spécifiée n’a pas pu être créée à l’aide de l’optimisation avant uniquement.</p>
<p><strong>Windows Server 2003 :</strong>  Cette erreur est renvoyée uniquement par Windows Server 2003 et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée. Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache le schéma de la table. Pour configurer le nombre de tables qui ont des schémas pouvant être mis en cache, utilisez <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Le membre <strong>CP</strong> de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Le membre <strong>coltyp</strong> de l' <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur un type de colonne valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Impossible de créer l’index, car une tentative d’utilisation d’un ID de paramètres régionaux non valide a été effectuée. L’ID de paramètres régionaux peut être entièrement non valide ou le module linguistique associé n’est peut-être pas installé.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>Impossible de créer l’index, car une tentative d’utilisation d’un ensemble non valide d’indicateurs de normalisation a été effectuée.</p>
<p><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p>
<p><strong>Windows 2000 :</strong>  Sur Windows 2000, les indicateurs de normalisation non valides entraînent JET_errIndexInvalidDef.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Impossible de créer l’index, car une définition d’index non valide a été spécifiée. <strong>JetOpenTemporaryTable</strong> renvoie cette erreur dans les conditions suivantes :</p>
<ul>
<li><p>Les paramètres régionaux de langue neutre sont spécifiés.</p></li>
<li><p>Un ensemble non valide d’indicateurs de normalisation est spécifié.</p></li>
</ul>
<p><strong>Windows 2000 :</strong>  Cette erreur est renvoyée uniquement par Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache les index de la table. Pour configurer le nombre d’index qui ont des schémas pouvant être mis en cache, utilisez <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, un curseur ouvert sur la table temporaire nouvellement créée est retourné. L’état de la base de données temporaire sera préparé à contenir la nouvelle table temporaire. L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.

En cas d’échec, la table temporaire n’est pas créée et un curseur n’est pas renvoyé. L’état de la base de données temporaire peut être modifié. L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.

#### <a name="remarks"></a>Notes

Les tables temporaires ne prennent pas en charge le complément complet des options de définition de colonne généralement prises en charge par le moteur de base de données. En fait, seuls les JET_bitColumnFixed et les JET_bitColumnTagged sont pris en charge. Cela signifie qu’il n’est pas possible de créer une colonne à incrémentation automatique, une version ou une colonne à plusieurs valeurs dans une table temporaire. Enfin, les colonnes de mise à jour de tiers de confiance ne sont pas prises en charge, car elles ne peuvent être utilisées que par une seule session à la fois. Si l’une de ces options est demandée, elles seront ignorées.

Les tables temporaires ne prennent pas en charge les valeurs par défaut. Si une définition de colonne est fournie et contient une spécification de valeur par défaut, cette spécification sera ignorée.

Les tables temporaires sont retournées à l’appelant à la suite de nombreuses fonctions ESE différentes. Par exemple, [JetGetIndexInfo](./jetgetindexinfo-function.md) avec le groupe d’options JET_IdxInfo retourne une table temporaire contenant une liste de toutes les colonnes clés d’un index donné. Les tables temporaires suivent les mêmes règles de cycle de vie que les tables temporaires ordinaires, comme décrit ici.

Les tables temporaires sont également utilisées en interne par le moteur de base de données pour de nombreuses tâches. La plus importante de ces tâches est la création d’un index sur une table existante. Une table temporaire sera utilisée pour trier les clés d’index utilisées pour construire cet index.

Toutes les tables temporaires sont stockées dans la base de données temporaire. La base de données temporaire est un fichier de base de données spécial qui est conservé pendant la durée de vie d’une instance ESE et qui est supprimé lorsque cette instance est arrêtée ou redémarrée. L’emplacement de la base de données temporaire peut être configuré à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramTempPath](./temporary-database-parameters.md). Le placement de la base de données temporaire sur le disque par rapport à vos fichiers journaux de transactions et vos fichiers de base de données peut être important si votre application utilise intensivement des tables temporaires ou crée fréquemment des index.

Le cycle de vie d’une table temporaire est lié aux curseurs qui la référencent. Si tous les curseurs qui font référence à une table temporaire sont fermés, de manière implicite ou explicite, la table temporaire est supprimée. Si une table temporaire est créée à l’intérieur d’une transaction et que la transaction est ensuite restaurée, la table temporaire est supprimée, car tous les curseurs qui y font référence sont implicitement fermés. Les nouveaux curseurs peuvent référencer une table temporaire uniquement par le biais de l’utilisation de [JetDupCursor](./jetdupcursor-function.md). Dans ce cas, les nouveaux curseurs sont positionnés sur la première entrée d’index de la table temporaire. [JetDupCursor](./jetdupcursor-function.md) ne fonctionnera que pendant certaines phases d’utilisation de la table temporaire. Pour plus d’informations, consultez les notes relatives aux fonctionnalités de curseur de table temporaires. Il n’est pas possible de référencer une table temporaire à partir de plusieurs sessions à la fois.

**Attention**  Il existe un problème important dans [JetDupCursor](./jetdupcursor-function.md) qui affecte les tables temporaires. Si une tentative est faite pour dupliquer une table temporaire en mode avant uniquement, le curseur résultant ne sera pas créé correctement et fonctionnera correctement. Il est toujours possible de dupliquer un curseur sur une table temporaire matérialisée.

Le gestionnaire de tables temporaire peut implémenter une table temporaire de trois manières. La première méthode consiste à conserver une table en mémoire. Cette stratégie est la plus rapide, mais elle ne peut être utilisée que pour les tables temporaires, simples et de petite taille. La deuxième méthode consiste à créer un tri sur disque qui peut être piloté à l’aide d’un itérateur avant uniquement. Cette stratégie ne peut être utilisée que dans certaines circonstances et est le moyen le plus rapide pour trier et supprimer les doublons d’un jeu de données très volumineux. La troisième méthode consiste à créer une arborescence B + dans la base de données temporaire pour contenir la table temporaire. Cette stratégie est la plus lente, mais la plus polyvalente, appelée « table temporaire matérialisée ». Ces stratégies peuvent être utilisées en association pour obtenir les fonctionnalités demandées par la table temporaire.

Lorsque la table temporaire n’est pas matérialisée, elle est principalement utilisée en deux phases principales. La première phase correspond à la phase d’insertion où la table est remplie avec son jeu de données initial. Pendant cette phase, seule l’insertion de données est autorisée. Cette phase se termine lorsqu’une tentative est effectuée pour déplacer le curseur à l’aide de [JetMove](./jetmove-function.md) ou [JetSeek](./jetseek-function.md). La deuxième phase est la phase d’extraction des données. Au cours de cette phase, les données stockées dans la table temporaire peuvent être extraites en fonction des fonctionnalités qui ont été demandées lors de la création de la table temporaire.

**Fonctionnalités de curseur de table temporaires**

Lorsque la table temporaire est matérialisée, le curseur a les fonctionnalités suivantes, mais peut être limité par les options demandées :

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDelete](./jetdelete-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUpdate](./jetupdate-function.md)

Lorsque la table temporaire n’est pas matérialisée et qu’elle est dans la phase d’insertion, le curseur a les fonctionnalités suivantes, mais peut être limité par les options demandées :

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)
    
    **Remarque**  Provoque la transition vers la phase d’extraction.

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)
    
    **Remarque**  Provoque la transition vers la phase d’extraction.

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetUpdate](./jetupdate-function.md)

Lorsque la table temporaire n’est pas matérialisée et qu’elle est dans la phase d’extraction, le curseur a les fonctionnalités suivantes, mais peut être limité par les options demandées :

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)
    
    **Remarque**  Si une tentative est faite pour dupliquer une table temporaire en mode avant uniquement, le curseur résultant ne sera pas créé correctement et fonctionnera correctement. Il est toujours possible de dupliquer un curseur sur une table temporaire matérialisée.

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008.</p></td>
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
[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres d’information](./informational-parameters.md)  
[Paramètres de base de données temporaires](./temporary-database-parameters.md)
