---
description: 'En savoir plus sur : fonction JetGetTableColumnInfo'
title: JetGetTableColumnInfo fonction)
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3940c07cc641d8c8d077c420f8c492ab5122b3f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984732"
---
# <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo fonction)

La fonction **JetGetTableColumnInfo** récupère des informations sur une colonne de table.

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table qui contient la colonne pour laquelle extraire des informations.

*szColumnName*

Nom de la colonne dont les informations doivent être récupérées.

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations. Le type de la mémoire tampon dépend de *InfoLevel*. L’appelant doit être configuré pour aligner la mémoire tampon de manière appropriée.

*cbMax*

Taille, en octets, de la mémoire tampon qui a été passée dans *pvResult*.

*InfoLevel*

Type des informations qui seront récupérées pour la colonne spécifiée par *szColumnName*. Le format des données stockées dans *pvResult* dépend de *InfoLevel*. Pour obtenir le schéma de la table temporaire, consultez [JET_COLUMNLIST](./jet-columnlist-structure.md).

  - JET_ColInfoListSortColumnid triera la table temporaire par *ColumnID*.

  - JET_ColInfoListCompact compacte la sortie. Pour plus d’informations sur la sortie compacte, consultez [JET_COLUMNLIST](./jet-columnlist-structure.md).

Les options suivantes peuvent être définies pour ce paramètre :


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p><em>pvResult</em> est interprété comme un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>et les champs de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> sont remplis de manière appropriée. JET_ColInfo et JET_ColInfoByColid récupérer les mêmes informations.</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Cela est similaire à une structure de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées. Si cette fonction échoue, la structure contient des données non définies.</p> | 
| <p>JET_ColInfoByColid</p> | <p><em>pvResult</em> est interprété comme un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, sauf que ce <em>InfoLevel</em> indique que la colonne demandée (<em>szColumName</em>) n’est pas le nom de la colonne de chaîne, mais un pointeur vers une <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>. JET_ColInfo et JET_ColInfoByColid récupérer les mêmes informations.</p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées. Une table temporaire est ouverte et identifiée par le membre <em>TableID</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. La table doit être fermée avec <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Si cette fonction échoue, la structure contient des données non définies.</p> | 
| <p>JET_ColInfoListCompact</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées. Une table temporaire est ouverte et identifiée par le membre <em>TableID</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>. La table doit être fermée avec <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Si cette fonction échoue, la structure contient des données non définies.</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>Comme JET_ColInfoList, toutefois, la table résultante est triée par <em>ColumnID</em>, et non par nom de colonne.</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor est déconseillé et son utilisation retourne JET_errFeatureNotAvailable.</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>Comme JET_ColInfoBase, <em>pvResult</em> est interprété comme un <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, sauf que ce <em>InfoLevel</em> indique que la colonne demandée (<em>szColumName</em>) n’est pas le nom de la colonne de chaîne, mais un pointeur vers un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p><p><strong>Windows Vista :</strong> cette version est disponible dans Windows Vista et versions ultérieures.</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>Retourne uniquement les colonnes non dérivées (si la table est dérivée d’un modèle).</p><p>Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</p><p><strong>Windows Vista :</strong> cette valeur est introduite dans Windows Vista.</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>Retourne uniquement le nom de colonne et le ColumnID de chaque colonne.</p><p>Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</p><p><strong>Windows Vista :</strong> cette valeur est introduite dans Windows Vista.</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>Trie la liste des colonnes retournées par ColumnId (par défaut, trie la liste par nom de colonne).</p><p>Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</p><p><strong>Windows Vista :</strong> cette valeur est introduite dans Windows Vista.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonne nommée <em>szColumnName</em> est introuvable dans la table.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Un <em>InfoLevel</em> incorrect a été spécifié.</p> | 
| <p>JET_errInvalidName</p> | <p>Cette erreur peut être retournée dans les cas suivants :</p><ul><li><p>Un nom incorrect a été donné pour <em>szTableName</em> .</p></li><li><p>Un nom incorrect a été donné pour <em>szColumnName</em> .</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Cette erreur peut être retournée dans les cas suivants :</p><ul><li><p>Un <em>InfoLevel</em> incorrect a été spécifié.</p></li><li><p>Un <em>SZTABLENAME</em> null a été passé.</p></li><li><p>La mémoire tampon est insuffisante.</p></li></ul> | 



#### <a name="remarks"></a>Remarques

**JetGetTableColumnInfo** et [JetGetColumnInfo](./jetgetcolumninfo-function.md) récupèrent les informations sur une colonne. La différence entre les deux est la manière dont la table est identifiée :

  - **JetGetTableColumnInfo** identifie une table par *TableID*.

  - [JetGetColumnInfo](./jetgetcolumninfo-function.md) identifie une table par la combinaison *dbid* et *szTableName* .

Lorsque vous récupérez des données avec JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, une table temporaire est ouverte. La table temporaire contient des données et la structure [JET_COLUMNLIST](./jet-columnlist-structure.md) contient des informations suffisantes pour parcourir la table temporaire. La table temporaire doit être fermée avec [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetGetTableColumnInfoW</strong> (Unicode) et <strong>JetGetTableColumnInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md)  
[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo]()
