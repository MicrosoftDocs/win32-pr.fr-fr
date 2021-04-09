---
description: 'En savoir plus sur : fonction JetGetTableInfo'
title: Fonction JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952928"
---
# <a name="jetgettableinfo-function"></a>Fonction JetGetTableInfo


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgettableinfo-function"></a>Fonction JetGetTableInfo

La fonction **JetGetTableInfo** récupère différents éléments d’informations sur une table dans une base de données.

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table à laquelle les informations s’appliquent.

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations. Le type de la mémoire tampon dépend de *InfoLevel*. Il incombe à l’appelant d’aligner la mémoire tampon en conséquence.

*cbMax*

Taille, en octets, de la mémoire tampon qui a été passée dans *pvResult*.

*InfoLevel*

Type d’information qui sera récupéré pour la table spécifiée par *TableID*. Le format des données stockées dans *pvResult* dépend de *InfoLevel*.

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
<td><p>JET_TblInfo</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> . Si la méthode est réussie, la structure <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> est renseignée avec les données appropriées. En cas d’échec, le contenu n’est pas défini.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoDbid</p></td>
<td><p><em>pvResult</em> est traité comme un tableau de deux objets <a href="gg269248(v=exchg.10).md">JET_DBID</a> . L’identificateur de base de données de la base de données qui possède la table est stocké à deux reprises dans ce tableau.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoDumpTable</p></td>
<td><p>JET_TblInfoDumpTable est déconseillé. L’API retourne JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoName</p></td>
<td><p>JET_TblInfoName récupère le nom de la table et le stocke dans <em>pvResult</em>. Si la mémoire tampon est trop petite, le comportement n’est pas défini.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoMostMany</p></td>
<td><p>JET_TblInfoMostMany récupère le nom de la table et le stocke dans <em>pvResult</em>. Si la mémoire tampon est trop petite, le comportement n’est pas défini.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoOLC</p></td>
<td><p>JET_TblInfoOLC est déconseillé. L’API retourne JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoRvt</p></td>
<td><p>JET_TblInfoRvt est déconseillé. L’API retourne JET_errQueryNotSupported.</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoResetOLC</p></td>
<td><p>JET_TblInfoResetOLC est déconseillé. L’API retourne JET_errFeatureNotAvailable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceAlloc</p></td>
<td><p><em>pvResult</em> est interprété comme un tableau de deux ULONGs :</p>
<ul>
<li><p>Le premier <strong>ULong</strong> est le nombre de pages dans la table.</p></li>
<li><p>Le deuxième <strong>ULong</strong> est la densité cible des pages de la table.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceAvailable</p></td>
<td><p><em>pvResult</em> est interprété comme <strong>ULong</strong>. <strong>ULong</strong> est la somme du nombre de pages disponibles dans la table, ses index et l’arborescence de valeurs longues.</p></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoSpaceOwned</p></td>
<td><p><em>pvResult</em> est interprété comme <strong>ULong</strong>. <strong>ULong</strong> correspond à la somme du nombre de pages appartenant à la table (y compris ses index et à l’arborescence de valeurs longues et à toutes les pages disponibles).</p></td>
</tr>
<tr class="even">
<td><p>JET_TblInfoSpaceUsage</p></td>
<td><p>Le comportement de l’API dépend de la taille de la mémoire tampon qui est transmise à l’API. Deux valeurs <em>cbMax</em> doivent être au moins (2 * sizeof (ULONG)).</p>
<ul>
<li><p>Si <em>cbMax</em> est (2 * sizeof (ULONG)), <em>pvResult</em> est interprété comme un tableau de deux ULONGs :</p>
<ul>
<li><p>Le premier <strong>ULong</strong> est le nombre d’étendues appartenant à la table.</p></li>
<li><p>Le deuxième <strong>ULong</strong> est le nombre d’étendues disponibles de la table.</p></li>
</ul></li>
<li><p><em>pvResult</em> est interprété comme un tableau de :</p>
<ul>
<li><p>Le premier <strong>ULong</strong> est le nombre d’étendues appartenant à la table.</p></li>
<li><p>Le deuxième <strong>ULong</strong> est le nombre d’étendues disponibles de la table.</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_TblInfoTemplateTableName</p></td>
<td><p><em>pvResult</em> est interprété comme une mémoire tampon de chaîne. La mémoire tampon doit être au moins JET_cbNameMost + 1, y compris le caractère <strong>null</strong>de fin. Si la table est une table dérivée, la mémoire tampon est remplie avec le nom de la table à partir de laquelle la table dérivée a hérité son DDL. Si la table n’est pas une table dérivée, la mémoire tampon est une chaîne vide.</p></td>
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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>La mémoire tampon est insuffisante.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Un <em>InfoLevel</em> déconseillé a été spécifié.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>La mémoire tampon n’est pas de la bonne taille.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidOperation</p></td>
<td><p>La table qui a été transmise était une table temporaire et le <em>InfoLevel</em> demandé ne peut pas être récupéré pour une table temporaire.</p></td>
</tr>
<tr class="even">
<td><p>JET_errObjectNotFound</p></td>
<td><p>La table qui a été transmise était une table temporaire et le <em>InfoLevel</em> demandé ne peut pas être récupéré pour une table temporaire.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errQueryNotSupported</p></td>
<td><p><em>InfoLevel</em> n’est pas pris en charge.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>La table est utilisée par une autre opération de base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>La table est verrouillée par une autre opération de base de données.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>La table est utilisée par le système. Cet avertissement n’est pas irrécupérable.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

Certaines informations ne sont pas valides pour les tables temporaires (voir [JetOpenTempTable](./jetopentemptable-function.md)).

Les statistiques de table incluent le nombre d’enregistrements et le nombre de pages dans l’index cluster (autrement dit, l’index contenant les données d’enregistrement). Les statistiques d’index sont accessibles séparément par nom, à l’aide de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

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
<td><p>Implémenté en tant que <strong>JetGetTableInfoW</strong> (Unicode) et <strong>JetGetTableInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)
