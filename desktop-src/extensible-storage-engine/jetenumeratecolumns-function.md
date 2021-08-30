---
description: 'En savoir plus sur : fonction JetEnumerateColumns'
title: Fonction JetEnumerateColumns
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a9d5b8d32db7fdb786edc7aaade92bf2e074080
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988076"
---
# <a name="jetenumeratecolumns-function"></a>Fonction JetEnumerateColumns


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetenumeratecolumns-function"></a>Fonction JetEnumerateColumns

La fonction **JetEnumerateColumns** récupère efficacement un ensemble de colonnes et leurs valeurs à partir de l’enregistrement actuel d’un curseur ou de la mémoire tampon de copie de ce curseur. Les colonnes et les valeurs récupérées peuvent être restreintes par une liste d’ID de colonne, de nombres *itagSequence* et d’autres caractéristiques. Cette API de récupération de colonne est unique dans la mesure où elle retourne des informations dans la mémoire allouée dynamiquement obtenue à l’aide d’un rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fourni par l’utilisateur. Cette nouvelle flexibilité permet une récupération efficace des données de colonne avec des caractéristiques spécifiques (telles que la taille et la multiplicité) qui sont inconnues pour l’appelant. Cela élimine le besoin d’utiliser les modes de découverte de [JetRetrieveColumn](./jetretrievecolumn-function.md) pour déterminer ces caractéristiques afin de configurer un dernier appel à [JetRetrieveColumn](./jetretrievecolumn-function.md) qui récupérera correctement les données souhaitées.

**Windows xp : JetEnumerateColumns** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*cEnumColumnId*

Tableau d’ID de colonne, chacun avec un tableau facultatif de nombres *itagSequence* à énumérer.

Si *cEnumColumnId* a la valeur 0 (zéro), *rgEnumColumnId* est ignoré et toutes les valeurs de colonne sont énumérées et retournées à l’appelant. Si un élément du tableau d’ID de colonne fait référence à un ID de colonne 0 (zéro), l’énumération de cette colonne est ignorée et un emplacement correspondant dans la sortie est généré avec un état de colonne de JET_wrnColumnSkipped.

Si *ctagSequence* a la valeur 0 (zéro) pour un élément donné du tableau d’ID de colonne, *rgtagSequence* est ignoré et toutes les valeurs de colonne pour cet ID de colonne sont énumérées et retournées à l’appelant. Si un élément d’un tableau de nombres *itagSequence* fait référence à un nombre *itagSequence* égal à 0 (zéro), l’énumération de ce numéro de *itagSequence* est ignorée et un emplacement correspondant dans la sortie est généré avec un état de valeur de colonne JET_wrnColumnSkipped.

*rgEnumColumnId*

Consultez *cEnumColumnId*.

*pcEnumColumn*

Retourne le tableau énuméré des colonnes et leurs valeurs en mémoire allouées via le rappel compatible *itagSequence* fourni.

Si un tableau d’ID de colonne est demandé en entrée, l’ordre et la taille du tableau de sortie reflètent l’ordre et la taille du tableau d’entrée. De même, si un tableau de nombres *itagSequence* est demandé pour un ID de colonne particulier en entrée, l’ordre et la taille du tableau de sortie des valeurs de colonne pour cette colonne reflètent l’ordre et la taille du tableau d’entrée.

Les paramètres de sortie ont la valeur 0 (zéro) et la **valeur null** pour toutes les erreurs, à l’exception de JET_errBadColumnId et JET_errColumnNotFound. Lorsque ces erreurs sont retournées, les données de sortie sont valides et complètes pour tous les ID de colonne sauf les affectés. Le code d’état de chacun des ID de colonne affectés est défini sur l’une de ces erreurs, de sorte que l’appelant peut déterminer les ID de colonne qui sont incorrects et éventuellement prendre des mesures correctives.

*prgEnumColumn*

Consultez *pcEnumColumn*.

*pfnRealloc*

Identifie un rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) et un pointeur de contexte facultatif utilisé pour allouer de la mémoire pour le tableau de sortie des colonnes et leurs valeurs.

*pvReallocContext*

Consultez *pfnRealloc*.

*cbDataMost*

Définit une limite sur la quantité de données à retourner à partir d’une colonne de texte long ou d’une colonne binaire longue.

Ce paramètre peut être utilisé pour empêcher l’énumération d’une valeur de colonne extrêmement volumineuse. En règle générale, une telle énumération peut échouer l’appel d’API avec JET_errOutOfMemory. Si une valeur de colonne importante est tronquée de telle manière, l’état de la valeur de colonne sera JET_wrnColumnTruncated.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitEnumerateCompressOutput</p> | <p>Lors de l’énumération des valeurs de colonne, toutes les colonnes pour lesquelles nous récupérons toutes les valeurs et qui ont une seule valeur de colonne non NULL peuvent être retournées dans un format compressé. L’état de ces colonnes est défini sur JET_wrnColumnSingleValue et la taille de la valeur de colonne et la mémoire contenant la valeur de colonne sont retournées directement dans la structure <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> . Il n’est pas garanti que toutes les colonnes admissibles soient compressées de cette manière. Pour plus d’informations, consultez <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</p> | 
| <p>JET_bitEnumerateCopy</p> | <p>Cette option indique que les valeurs de colonne modifiées de l’enregistrement doivent être énumérées au lieu des valeurs de colonne d’origine. Si une valeur de colonne n’a pas été modifiée, la valeur de colonne d’origine est énumérée. De cette façon, une valeur de colonne qui n’a pas encore été insérée ou mise à jour peut être énumérée lors de l’insertion ou de la mise à jour d’un enregistrement.</p><p>Cette option est identique à JET_bitRetrieveCopy lorsqu’elle est utilisée avec <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ou <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</p> | 
| <p>JET_bitEnumerateIgnoreDefault</p> | <p>Si une colonne donnée n’est pas présente dans l’enregistrement, aucune valeur de colonne n’est retournée. En règle générale, la valeur par défaut de la colonne, le cas échéant, est retournée dans ce cas. Il est garanti que si la colonne est définie sur une valeur différente de la valeur par défaut, cette valeur différente sera retournée (autrement dit, si une colonne avec une valeur par défaut est explicitement définie sur <strong>null</strong> , une valeur <strong>null</strong> est retournée en tant que valeur pour cette colonne). Notez que, même si cette option est demandée, il est toujours possible de voir une valeur de colonne qui se trouve être égale à la valeur par défaut. Aucun effort n’est apporté pour supprimer des valeurs de colonne qui correspondent à leurs valeurs par défaut.</p><p>Il est important de noter que cette option affecte la sortie de <strong>JetEnumerateColumns</strong> lorsqu’elle est utilisée avec JET_bitEnumeratePresenceOnly ou JET_bitEnumerateTaggedOnly.</p> | 
| <p>JET_bitEnumerateIgnoreUserDefinedDefault</p> | <p>Si une colonne donnée n’est pas présente dans l’enregistrement et qu’elle a une valeur par défaut définie par l’utilisateur, aucune valeur de colonne n’est retournée. Cette option empêchera le rappel qui calcule la valeur par défaut définie par l’utilisateur pour la colonne à être appelée lors de l’énumération des valeurs de cette colonne.</p><p><strong>Windows Server 2003 et versions antérieures :</strong> pour Windows Server 2003 et versions antérieures, l’opération échoue avec JET_errCallbackFailed.</p><p><strong>Windows Server 2003 SP1 :</strong> cette valeur possible est disponible uniquement pour les systèmes d’exploitation Windows Server 2003 SP1 et versions ultérieures. Si cette valeur possible est spécifiée et que la table contient une colonne qui a une valeur par défaut définie par l’utilisateur, l’opération échoue avec JET_errCallbackFailed.</p> | 
| <p>JET_bitEnumeratePresenceOnly</p> | <p>Si une valeur non NULL existe pour la colonne ou la valeur de colonne demandée, les données associées ne sont pas retournées. Au lieu de cela, l’état associé à la colonne ou à la valeur de cette colonne sera défini sur JET_wrnColumnPresent. Si la colonne ou la valeur de colonne est <strong>null</strong> , JET_wrnColumnNull est retourné comme d’habitude.</p> | 
| <p>JET_bitEnumerateTaggedOnly</p> | <p>Lors de l’énumération de toutes les valeurs de colonne dans l’enregistrement (par exemple, lorsque <em>cEnumColumnId</em> est égal à zéro), seules les valeurs de colonne avec balises sont retournées. Cette option n’est pas autorisée lors de l’énumération d’un tableau spécifique d’ID de colonne.</p> | 
| <p>JET_bitEnumerateInRecordOnly</p> | <p><strong>Windows 7 :</strong> JET_bitEnumerateInRecordOnly est introduite dans Windows 7.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBadColumnId</p> | <p>L’ID de colonne indiqué est en dehors des limites autorisées d’un ID de colonne. Cette erreur est retournée par <strong>JetEnumerateColumns</strong> si des ID de colonne spécifiques ont été demandés, si l’un de ces ID de colonne n’était pas valide et si le premier ID de colonne non valide a échoué avec cette erreur pour son code d’état de colonne.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonne décrite par l’ID de colonne indiqué n’existe pas dans la table. Cette erreur est retournée par <strong>JetEnumerateColumns</strong> si des ID de colonne spécifiques ont été demandés, si l’un de ces ID de colonne n’était pas valide et si le premier ID de colonne non valide a échoué avec cette erreur pour son code d’état de colonne.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong> cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>L’une des options demandées n’est pas valide ou n’est pas implémentée. Cette erreur est retournée par <strong>JetEnumerateColumns</strong> quand :</p><ul><li><p>JET_bitEnumerateLocal est spécifié.</p></li><li><p>Un <em>Grbit</em> illégal est spécifié.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cette erreur est retournée par <strong>JetEnumerateColumns</strong> quand :</p><ul><li><p><em>pcEnumColumn</em> a la <strong>valeur null</strong>.</p></li><li><p><em>prgEnumColumn</em> a la <strong>valeur null</strong>.</p></li><li><p><em>pfnRealloc</em> a la <strong>valeur null</strong>.</p></li></ul> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur n’est pas positionné sur un enregistrement. Cela peut se produire pour de nombreuses raisons différentes. Par exemple, cela se produit si le curseur est actuellement positionné après le dernier enregistrement de l’index actuel.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRecordDeleted</p> | <p>Le curseur est positionné sur un enregistrement qui a été supprimé. Cela peut se produire pour de nombreuses raisons différentes. La raison la plus courante est que la session n’est pas dans une transaction, que le curseur a été placé sur un enregistrement, que cet enregistrement a été supprimé, puis que le curseur a tenté de référencer cet enregistrement.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows XP :</strong> cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, les données demandées sont retournées dans les tampons de sortie. Il incombe à l’appelant de libérer la mémoire allouée par ce rappel et renvoyée dans les mémoires tampons de sortie. Cette mémoire doit être libérée par le rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fourni. Aucune modification de l’état de la base de données ne se produit.

En cas d’échec, aucune des données demandées n’est retournée. Toute mémoire qui a été allouée pendant l’appel sera libérée automatiquement à l’aide du rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fourni. Aucune modification de l’état de la base de données ne se produit.

#### <a name="remarks"></a>Remarques

Si vous énumérez toutes les valeurs de colonne dans l’enregistrement et que vous n’avez pas spécifié JET_bitEnumerateIgnoreDefaults, vous ne pouvez pas supposer que vous ne verrez jamais une colonne ou une valeur de colonne avec le code d’État JET_wrnColumnNull. Vous pouvez voir ce code d’État si une colonne a une valeur par défaut et a été explicitement définie sur **null** ou si la colonne est une colonne non éparse (par exemple, une colonne fixe ou variable).

Le paramètre *cbDataMost* ne s’applique pas à toutes les valeurs de colonne. Ce paramètre tronque uniquement le texte long et les valeurs de colonne binaires longues qui sont tellement volumineuses qu’elles ont été stockées séparément de l’enregistrement.

Si **JetEnumerateColumns** retourne des données dans ses paramètres de sortie, l’appelant est chargé de libérer la mémoire dans le tableau, ainsi que toute mémoire référencée par des pointeurs incorporés dans ce tableau.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JET_PFNREALLOC](./jet-pfnrealloc-callback-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
