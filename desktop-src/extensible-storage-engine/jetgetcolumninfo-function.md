---
description: 'En savoir plus sur : fonction JetGetColumnInfo'
title: Fonction JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522104"
---
# <a name="jetgetcolumninfo-function"></a>Fonction JetGetColumnInfo


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgetcolumninfo-function"></a>Fonction JetGetColumnInfo

La fonction **JetGetColumnInfo** récupère des informations sur une colonne.

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*dbid*

Identifie, avec *szTableName*, la table qui contient la colonne à partir de laquelle les informations sont récupérées.

*szTableName*

Identifie, avec *dbid*, la table qui contient la colonne à partir de laquelle les informations sont récupérées.

*szColumnName*

Nom de la colonne pour laquelle les informations sont extraites.

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations. Le type de la mémoire tampon dépend de *InfoLevel*. L’appelant doit être configuré pour aligner la mémoire tampon de manière appropriée.

*cbMax*

Taille, en octets, de la mémoire tampon passée dans *pvResult*.

*InfoLevel*

Type d’informations à récupérer pour la colonne spécifiée par *szColumnName*. Le format des données stockées dans *pvResult* dépend de ce paramètre. Pour obtenir le schéma de la table temporaire, consultez [JET_COLUMNLIST](./jet-columnlist-structure.md).

Ces *InfoLevels* sont différenciées par :

  - JET_ColInfoListSortColumnid triera la table temporaire par *ColumnID*.

  - JET_ColInfoListCompact compacte la sortie. Pour plus d’informations sur la sortie compacte, consultez [JET_COLUMNLIST](./jet-columnlist-structure.md).

Les options suivantes peuvent être utilisées avec ce paramètre.

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
<td><p>JET_ColInfo</p></td>
<td><p>JET_ColInfo et JET_ColInfoByColid récupérer les mêmes informations. <em>pvResult</em> est interprété comme un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>et les champs de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> sont remplis de manière appropriée.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBase</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> . Cela est similaire à une structure de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> . Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées. Si cette fonction échoue, la structure contient des données non définies.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoByColid</p></td>
<td><p>Comme JET_ColInfo, <em>pvResult</em> est interprété comme un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, sauf que ce <em>InfoLevel</em> indique que la colonne demandée (<em>szColumName</em>) n’est pas le nom de la colonne de chaîne, mais un pointeur vers un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoList</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées. Une table temporaire est ouverte et identifiée par le membre <strong>TableID</strong> de la structure <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> . La table doit être fermée avec <a href="gg294087(v=exchg.10).md">JetCloseTable</a>. Si cette fonction échoue, la structure contient des données non définies.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoListCompact</p></td>
<td><p>Identique à JET_ColInfoList.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoListSortColumnid</p></td>
<td><p>Identique à JET_ColInfoList ; Toutefois, la table résultante est triée par ColumnId, au lieu du nom de colonne.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoSysTabCursor</p></td>
<td><p>JET_ColInfoSysTabCursor est déconseillé et son utilisation retourne JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoBaseByColId</p></td>
<td><p>Comme JET_ColInfoBase, <em>pvResult</em> est interprété comme un <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, sauf que ce <em>InfoLevel</em> indique que la colonne demandée (<em>szColumName</em>) n’est pas le nom de la colonne de chaîne, mais un pointeur vers un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</p>
<p><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitNonDerivedColumnsOnly</p></td>
<td><p>Retourne uniquement les colonnes non dérivées (si la table est dérivée d’un modèle).</p>
<p>Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</p>
<p><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_ColInfoGrbitMinimalInfo</p></td>
<td><p>Retourne uniquement le nom de colonne et le ColumnID de chaque colonne.</p>
<p>Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</p>
<p><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ColInfoGrbitSortByColumnid</p></td>
<td><p>Trie la liste des colonnes retournées par ColumnId (par défaut, trie la liste par nom de colonne).</p>
<p>Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</p>
<p><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</p></td>
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
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonne nommée <em>szColumnName</em> est introuvable dans la table.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Un <em>InfoLevel</em> incorrect a été spécifié.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Cette erreur peut être retournée dans les cas suivants :</p>
<ul>
<li><p>Un nom incorrect a été donné pour <em>szTableName</em> .</p></li>
<li><p>Un nom incorrect a été donné pour <em>szColumnName</em> .</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Cette erreur peut être retournée dans les cas suivants :</p>
<ul>
<li><p>Un <em>InfoLevel</em> incorrect a été spécifié.</p></li>
<li><p>Un <em>SZTABLENAME</em> null a été passé.</p></li>
<li><p>La mémoire tampon est insuffisante.</p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) et **JetGetColumnInfo** récupèrent les informations sur une colonne. La différence entre les deux est la manière dont la table est identifiée :

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifie une table par *TableID*.

  - **JetGetColumnInfo** identifie une table par la combinaison *dbid* et *szTableName* .

Lorsque vous récupérez des données avec JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, une table temporaire est ouverte. La table temporaire contient des données et la structure [JET_COLUMNLIST](./jet-columnlist-structure.md) contient des informations suffisantes pour parcourir la table temporaire. La table temporaire doit être fermée avec [JetCloseTable](./jetclosetable-function.md).

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetGetColumnInfoW</strong> (Unicode) et <strong>JetGetColumnInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)  
[Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
