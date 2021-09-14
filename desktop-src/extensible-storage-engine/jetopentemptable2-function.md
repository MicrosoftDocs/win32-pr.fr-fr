---
description: 'En savoir plus sur : fonction JetOpenTempTable2'
title: Fonction JetOpenTempTable2
TOCTitle: JetOpenTempTable2 Function
ms:assetid: 788ec4f9-b0c3-409b-850c-7567dec47024
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269302(v=EXCHG.10)
ms:contentKeyID: 32765594
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f6ac33866ea2f58c6dc5de593aeed046c981c48c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192156"
---
# <a name="jetopentemptable2-function"></a>Fonction JetOpenTempTable2


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetopentemptable2-function"></a>Fonction JetOpenTempTable2

La fonction **JetOpenTempTable2** crée une table temporaire avec un index unique qui peut être utilisé pour stocker et récupérer des enregistrements comme une table ordinaire créée à l’aide de [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). Cette fonction a également un ID de paramètres régionaux qui peut être utilisé pour comparer les données de colonne de clé Unicode dans la table temporaire. Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile. Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle.

```cpp
    JET_ERR JET_API JetOpenTempTable2(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          unsigned long lcid,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser.

*prgcolumndef*

Définitions de colonne des colonnes à créer dans la table temporaire.

Il existe des limitations importantes pour les options de définition de colonne utilisées avec une table temporaire. Pour plus d'informations, consultez la section Notes.

Outre les options de définition de colonne habituelles, aucune ou plusieurs des options suivantes peuvent également être spécifiées qui ne sont pertinentes que dans le contexte d’une table temporaire.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>L’ordre de tri de la colonne clé pour la table temporaire doit être décroissant plutôt que croissant. Si cette option est spécifiée sans JET_bitColumnTTKey, cette option est ignorée.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>La colonne est une colonne clé pour la table temporaire.</p><p>L’ordre des définitions de colonne avec cette option spécifiée dans le tableau d’entrée détermine la précédence de chaque colonne clé pour la table temporaire. La première définition de colonne dans le tableau avec cette option est définie sur la colonne clé la plus significative, et ainsi de suite. Si le moteur de base de données demande plus de colonnes clés que ce qui peut être pris en charge par le moteur de base de données, cette option est ignorée pour les colonnes clés non prises en charge.</p> | 



*ccolumn*

Consultez *prgcolumndef*.

*lcid*

ID de paramètres régionaux à utiliser pour comparer les données de colonne de clé Unicode dans la table temporaire.

Les paramètres régionaux peuvent être utilisés tant que le module linguistique approprié a été installé sur l’ordinateur. La seule exception est que les paramètres régionaux de langue neutre (LCID de zéro) ne sont pas conformes.

sur Windows Server 2003 et versions ultérieures, si les paramètres régionaux de langue neutre sont spécifiés pour ce paramètre, l’ID de paramètres régionaux par défaut (anglais des états-unis) sera utilisé à la place. Cela permet d’autoriser une valeur de zéro pour signifier la valeur par défaut plutôt qu’une valeur non conforme.

Lorsque ce paramètre n’est pas présent et que le paramètre *pidxunicode* n’est pas présent, le LCID par défaut est utilisé pour comparer les données de colonne de clé Unicode dans la table temporaire. Le LCID par défaut est le paramètre régional anglais (États-Unis).

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>Cette option demande que toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échoue avec JET_errKeyDuplicate. Si cette option n’est pas demandée, un doublon peut être détecté immédiatement et échouer ou peut être supprimé en mode silencieux ultérieurement selon la stratégie choisie par le moteur de base de données pour implémenter la table temporaire en fonction de la fonctionnalité demandée.</p><p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>Cette option force le gestionnaire de tables temporaires à abandonner toute tentative de choix d’une stratégie astucieuse pour la gestion de la table temporaire qui entraîne des performances améliorées.</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>Cette option demande que la table temporaire soit créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation optimisée pour les résultats de requête intermédiaires. Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</p><p>L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées. Pour plus d’informations, consultez JET_bitTTUnique.</p><p>cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</p> | 
| <p>JET_bitTTIndexed</p> | <p>Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de <a href="gg294103(v=exchg.10).md">JetSeek</a> pour rechercher des enregistrements par clé d’index.</p><p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTScrollable</p> | <p>Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="gg294117(v=exchg.10).md">JetMove</a>.</p><p>Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>Cette option demande que les valeurs de colonne clé NULL soient triées plus près de la fin de l’index que les valeurs de colonne clé non NULL.</p> | 
| <p>JET_bitTTUnique</p> | <p>Cette option demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire.</p><p>avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques. à partir de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons lorsque l’option JET_bitTTForwardOnly est également spécifiée.</p><p>Il n’est pas possible de savoir quels doublons seront remportés et quels doublons seront ignorés en général. Toutefois, lorsque l’option JET_bitTTErrorOnDuplicateInsertion est demandée, alors le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire est toujours gagnant.</p> | 
| <p>JET_bitTTUpdatable</p> | <p>Cette option demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment. Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</p><p>Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>Demande d’autoriser uniquement les valeurs longues intrinsèques.</p><p><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> est introduite dans Windows 7.</p> | 



*pTableID*

Mémoire tampon de sortie qui recevra le nouveau curseur ouvert sur la table temporaire nouvellement créée.

*prgcolumnid*

Mémoire tampon de sortie qui recevra le tableau d’ID de colonne générés au cours de la création de la table temporaire.

Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne. Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>JetOpenTempTable2</strong> a échoué parce que JET_bitTTForwardOnly a été spécifié et que la table temporaire spécifiée n’a pas pu être créée à l’aide de l’optimisation avant uniquement. cette erreur est renvoyée uniquement par Windows Server 2003 et versions ultérieures.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Le champ CP de la <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Le champ <em>coltyp</em> de l' <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur un type de colonne valide.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Impossible de créer l’index, car une définition d’index non valide a été spécifiée.</p><p><strong>JetOpenTempTable2</strong> renvoie cette erreur dans les cas suivants :</p><ul><li><p>Les paramètres régionaux de langue neutre sont spécifiés.</p></li><li><p>Un ensemble non valide d’indicateurs de normalisation est spécifié.</p></li></ul><p>cette erreur est renvoyée uniquement par Windows 2000.</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>Impossible de créer l’index, car une tentative d’utilisation d’un ID de paramètres régionaux non valide a été effectuée. L’ID de paramètres régionaux peut être entièrement non valide ou le module linguistique associé n’est peut-être pas installé.</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>Impossible de créer l’index, car une tentative d’utilisation d’un ensemble non valide d’indicateurs de normalisation a été effectuée. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures. sur Windows 2000, les indicateurs de normalisation non valides entraînent JET_errIndexInvalidDef à la place.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errOutOfCursors</p> | <p>L’opération a échoué, car le moteur ne peut pas allouer les ressources requises pour ouvrir un nouveau curseur. Les ressources de curseur sont configurées à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>L’opération a échoué, car la mémoire peut être allouée pour être terminée.</p><p><strong>JetOpenTempTable2</strong> peut retourner JET_errOutOfMemory si l’espace d’adressage du processus hôte est trop fragmenté. Le gestionnaire de tables temporaire allouera toujours un segment d’espace d’adressage de 1 Mo pour chaque table temporaire créée, quelle que soit la quantité de données à stocker.</p> | 
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

Consultez [JetOpenTempTable](./jetopentemptable-function.md).

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
[Paramètres système](./extensible-storage-engine-system-parameters.md)
