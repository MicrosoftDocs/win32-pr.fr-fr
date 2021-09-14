---
description: 'En savoir plus sur : fonction JetOpenTempTable'
title: Fonction JetOpenTempTable
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a94af3f142fb7449a95ddf67ad9a0d16f2e37c43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917180"
---
# <a name="jetopentemptable-function"></a>Fonction JetOpenTempTable


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetopentemptable-function"></a>Fonction JetOpenTempTable

La fonction **JetOpenTempTable** crée une table temporaire avec un index unique. Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile. Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser.

*prgcolumndef*

Définitions de colonne pour les colonnes créées dans la table temporaire.

Il existe des limitations **importantes** pour les options de définition de colonne utilisées avec une table temporaire. Pour plus d'informations, consultez la section Notes.

Outre les options de définition de colonne habituelles, aucune ou plusieurs des options suivantes peuvent également être spécifiées qui ne sont pertinentes que dans le contexte d’une table temporaire.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>L’ordre de tri de la colonne clé pour la table temporaire doit être décroissant plutôt que croissant. Si cette option est spécifiée sans JET_bitColumnTTKey, cette option est ignorée.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>La colonne est une colonne clé pour la table temporaire.</p><p>L’ordre des définitions de colonne avec cette option spécifiée dans le tableau d’entrée détermine la précédence de chaque colonne clé pour la table temporaire. La première définition de colonne dans le tableau qui a cette option est définie sur la colonne clé la plus significative, et ainsi de suite. Si le moteur de base de données demande plus de colonnes clés que ce qui peut être pris en charge par le moteur de base de données, cette option est ignorée pour les colonnes clés non prises en charge.</p> | 



*ccolumn*

Consultez *prgcolumndef*.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échouera immédiatement avec JET_errKeyDuplicate. Si cette option n’est pas demandée, un doublon est détecté immédiatement et échoue, ou est supprimé en mode silencieux ultérieurement, en fonction de la stratégie choisie par le moteur de base de données pour implémenter la table temporaire, en fonction de la fonctionnalité demandée.</p><p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Force le gestionnaire de tables temporaires à abandonner la recherche de la meilleure stratégie pour utiliser la gestion de la table temporaire qui entraîne des performances améliorées.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>La table temporaire est créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation qui est optimisée pour les résultats de requête intermédiaires. Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</p><p>L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées. Pour plus d’informations, consultez JET_bitTTUnique.</p><p>cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</p> | 
| <p>JET_bitTTIndexed</p> | <p>Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de <a href="gg294103(v=exchg.10).md">JetSeek</a> pour rechercher des enregistrements par clé d’index.</p><p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTUnique</p> | <p>Demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire.</p><p>avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques. à partir de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons lorsque l’option JET_bitTTForwardOnly est également spécifiée.</p><p>Il n’est pas possible de savoir quel doublon va être effectué et quels doublons seront ignorés, en général. Toutefois, lorsque l’option JET_bitTTErrorOnDuplicateInsertion est demandée, le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire sera toujours correctement effectué.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment. Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</p><p>Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>.</p><p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Demande que les valeurs de colonne clé NULL soient plus proches de la fin de l’index que les valeurs de colonne clé non NULL.</p><p></p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>Demande d’autoriser uniquement les valeurs longues intrinsèques.</p><p><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> est introduite dans Windows 7.</p> | 



*pTableID*

Mémoire tampon de sortie qui reçoit le nouveau curseur ouvert sur la table temporaire nouvellement créée.

*prgcolumnid*

Mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés au cours de la création de la table temporaire.

Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne. Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>JetOpenTempTable</strong> a échoué parce que JET_bitTTForwardOnly a été spécifié et que la table temporaire spécifiée n’a pas pu être créée à l’aide de l’optimisation avant uniquement. cette erreur est renvoyée uniquement par Windows Server 2003 et versions ultérieures.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Impossible de créer l’index, car une définition d’index non valide a été spécifiée.</p><p><strong>JetOpenTempTable</strong> renvoie cette erreur dans les cas suivants :</p><ul><li><p>Les paramètres régionaux de langue neutre sont spécifiés.</p></li><li><p>Un ensemble non valide d’indicateurs de normalisation est spécifié.</p></li></ul><p>cette erreur est renvoyée uniquement par Windows 2000.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Le champ CP de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Le champ <em>coltyp</em> de l' <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur un type de colonne valide.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>Impossible de créer l’index, car une tentative d’utilisation d’un ID de paramètres régionaux non valide a été effectuée. L’ID de paramètres régionaux peut être entièrement non valide ou le module linguistique associé n’est peut-être pas installé.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>Impossible de créer l’index, car une tentative d’utilisation d’un ensemble non valide d’indicateurs de normalisation a été effectuée. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures. sur Windows 2000, les indicateurs de normalisation non valides entraînent JET_errIndexInvalidDef à la place.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Le descripteur de session n’est pas valide ou fait référence à une session fermée.</p><p><strong>Remarque</strong>  Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errOutOfCursors</p> | <p>L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur. Les ressources de curseur sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué, car la mémoire peut être allouée pour être terminée.</p><p><strong>JetOpenTempTable</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté. Le gestionnaire de tables temporaire allouera toujours un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données à stocker.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p>cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée. Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache les index de la table. Le nombre d’index dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>L’opération a échoué, car le moteur ne peut pas allouer les ressources nécessaires pour mettre en cache le schéma de la table. Le nombre de tables dont le schéma peut être mis en cache est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</p> | 
| <p>JET_errTooManySorts</p> | <p>L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour créer une table temporaire. Les ressources de table temporaire sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</p> | 



En cas de réussite, un curseur ouvert sur la table temporaire nouvellement créée est retourné. L’état de la base de données temporaire sera préparé à contenir la nouvelle table temporaire. L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.

En cas d’échec, la table temporaire n’est pas créée et un curseur n’est pas renvoyé. L’état de la base de données temporaire peut être modifié. L’état de toutes les bases de données ordinaires utilisées par le moteur de base de données reste inchangé.

#### <a name="remarks"></a>Notes

Les tables temporaires ne prennent pas en charge le complément complet des options de définition de colonne généralement prises en charge par le moteur de base de données. En fait, seuls les JET_bitColumnFixed et les JET_bitColumnTagged sont pris en charge. Cela signifie qu’il n’est pas possible de créer une colonne à incrémentation automatique, une version ou une colonne à plusieurs valeurs dans une table temporaire. Enfin, les colonnes de mise à jour de tiers de confiance ne sont pas prises en charge car elles ne sont pas utiles dans une table temporaire, car elles ne peuvent être utilisées que par une seule session à la fois. Si l’une de ces options est demandée, elles seront ignorées.

Les tables temporaires ne prennent pas en charge les valeurs par défaut. Si une définition de colonne est fournie et contient une spécification de valeur par défaut, cette spécification sera ignorée.

Les tables temporaires sont retournées à l’appelant à la suite de nombreuses fonctions ESE différentes. Par exemple, [JetGetIndexInfo](./jetgetindexinfo-function.md) avec l’option JET_IdxInfo définie dans le paramètre *InfoLevel* retourne une table temporaire contenant une liste de toutes les colonnes clés d’un index donné. Les tables temporaires suivent les mêmes règles de cycle de vie que les tables temporaires ordinaires, comme décrit ici.

Les tables temporaires sont également utilisées en interne par le moteur de base de données pour de nombreuses tâches. La plus importante de ces tâches est la création d’un index sur une table existante. Une table temporaire sera utilisée pour trier les clés d’index utilisées pour construire cet index.

Toutes les tables temporaires sont stockées dans la base de données temporaire. La base de données temporaire est un fichier de base de données spécial qui est conservé pendant la durée de vie d’une instance ESE et qui est supprimé lorsque cette instance est arrêtée ou redémarrée. L’emplacement de la base de données temporaire peut être configuré à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramTempPath](./temporary-database-parameters.md). Le placement de la base de données temporaire sur le disque par rapport à vos fichiers journaux de transactions et vos fichiers de base de données peut être important si votre application utilise intensivement des tables temporaires ou crée fréquemment des index.

Le cycle de vie d’une table temporaire est lié aux curseurs qui la référencent. Si tous les curseurs qui font référence à une table temporaire sont fermés, de manière implicite ou explicite, la table temporaire est supprimée. Si une table temporaire est créée à l’intérieur d’une transaction et que la transaction est ensuite restaurée, la table temporaire est supprimée, car tous les curseurs qui y font référence sont implicitement fermés. Les nouveaux curseurs peuvent référencer une table temporaire uniquement par le biais de l’utilisation de [JetDupCursor](./jetdupcursor-function.md). Dans ce cas, les nouveaux curseurs sont positionnés sur la première entrée d’index de la table temporaire. [JetDupCursor](./jetdupcursor-function.md) ne fonctionnera que pendant certaines phases d’utilisation de la table temporaire. Pour plus d’informations, consultez les notes relatives aux fonctionnalités de curseur de table temporaires. Il n’est pas possible de référencer une table temporaire à partir de plusieurs sessions à la fois.

Il existe un problème important dans [JetDupCursor](./jetdupcursor-function.md) qui affecte les tables temporaires. Si une tentative est faite pour dupliquer une table temporaire en mode avant uniquement, le curseur résultant ne sera pas créé correctement et fonctionnera correctement. Il est toujours possible de dupliquer un curseur sur une table temporaire matérialisée.

Le gestionnaire de tables temporaire peut choisir d’implémenter une table temporaire de trois manières. La première méthode consiste à conserver une table en mémoire. Cette stratégie est la plus rapide, mais elle ne peut être utilisée que pour les petites tables temporaires simples. La deuxième méthode consiste à créer un tri sur disque qui peut être piloté à l’aide d’un itérateur avant uniquement. Cette stratégie ne peut être utilisée que dans certaines circonstances et est le moyen le plus rapide pour trier et supprimer les doublons d’un jeu de données très volumineux. La troisième méthode consiste à créer une arborescence B + dans la base de données temporaire pour contenir la table temporaire. Cette stratégie est la plus lente, mais la plus polyvalente, appelée « table temporaire matérialisée ». Ces stratégies peuvent être utilisées en association pour atteindre en fin de fonction la fonctionnalité demandée par la table temporaire.

Lorsque la table temporaire n’est pas matérialisée, elle est utilisée principalement en deux phases principales. La première phase correspond à la phase d’insertion où la table est remplie avec son jeu de données initial. Pendant cette phase, seule l’insertion de données est autorisée. Cette phase se termine lorsqu’une tentative est effectuée pour déplacer le curseur à l’aide de [JetMove](./jetmove-function.md) ou [JetSeek](./jetseek-function.md). La deuxième phase est la phase d’extraction des données. Au cours de cette phase, les données stockées dans la table temporaire peuvent être extraites en fonction des capacités requises lors de la création de la table temporaire.

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

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

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
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres de base de données temporaires](./temporary-database-parameters.md)
