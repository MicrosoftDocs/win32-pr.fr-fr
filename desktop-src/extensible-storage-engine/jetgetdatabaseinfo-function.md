---
description: 'En savoir plus sur : fonction JetGetDatabaseInfo'
title: Fonction JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203134"
---
# <a name="jetgetdatabaseinfo-function"></a>Fonction JetGetDatabaseInfo


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgetdatabaseinfo-function"></a>Fonction JetGetDatabaseInfo

La fonction **JetGetDatabaseInfo** récupère différents types d’informations sur la base de données. Cette API peut être appelée lorsqu’une base de données est attachée ou en ligne (avec **JetGetDatabaseInfo**) ou que la base de données ou le moteur de base de données est hors connexion (avec [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*dbid*

[JET_DBID](./jet-dbid.md) de la base de données à partir de laquelle récupérer les informations.

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations spécifiées. La taille de la mémoire tampon, en octets, est passée dans *cbMax*.

En cas d’échec, le contenu de *pvResult* n’est pas défini.

Les informations stockées dans *pvResult* dépendent de *InfoLevel*.

*cbMax*

Taille, en octets, de la mémoire tampon qui a été passée dans *pvResult*.

*InfoLevel*

*InfoLevel* spécifie le type d’informations à récupérer sur la base de données spécifiée. Cela affecte la façon dont *pvResult* est interprété. Certains *InfoLevel* sont disponibles uniquement dans la version hors connexion ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) ou en ligne (**JetGetDatabaseInfo**) de l’API.

Si la mémoire tampon *pvResult* fournie est trop petite, JET_errInvalidBufferSize ou JET_errBufferTooSmall sont retournés en fonction du *InfoLevel*.

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
<td><p>JET_DbInfoCollate</p></td>
<td><p>Pas encore pris en charge et retournent les valeurs par défaut. Ne pas utiliser.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Ces <em>InfoLevels</em> sont déconseillés et ne sont pas pris en charge actuellement. Ne pas utiliser.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Pas encore pris en charge et retournent les valeurs par défaut. Ne pas utiliser.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Pas encore pris en charge et retournent les valeurs par défaut. Ne pas utiliser.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFilename</p></td>
<td><p><em>pvResult</em> sera interprété comme une mémoire tampon de chaîne (Char *). Une mémoire tampon de MAX_PATH est suggérée, mais pas obligatoire. Si la mémoire tampon n’est pas assez longue, JET_errBufferTooSmall est retourné. La chaîne sera remplie avec le chemin d’accès de la base de données pour ce DBID.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvResult</em> sera interprété comme un DWORD (4 octets). Retourne la taille de la base de données en pages.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Ces <em>InfoLevels</em> sont déconseillés et ne sont pas pris en charge actuellement. Ne pas utiliser.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoLCID</p></td>
<td><p>(Windows XP et versions ultérieures) Ce <em>InfoLevel</em> a été initialement spécifié comme suit : JET_DbInfoLangid (Windows 2000)</p>
<p><em>pvResult</em> sera interprété comme long. Cela retourne l’identificateur de paramètres régionaux (LCID) associé à cette base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> sera interprété comme un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La structure <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> sera remplie avec les informations relatives à la base de données spécifiée.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoOptions</p></td>
<td><p><em>pvResult</em> sera interprété comme un <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD). Cela indique si la base de données est ouverte en mode exclusif. Si la base de données est en mode exclusif JET_bitDbExclusive sera définie dans le <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> fourni, sinon zéro est défini. Notez que les autres options de base de données <em>Grbit</em> pour <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> et <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> ne sont pas renvoyées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p>Disponible uniquement sur Windows XP et versions ultérieures. <em>pvResult</em> sera interprété comme un entier long non signé. Cela renverra la taille de page de la base de données en octets.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoSpaceAvailable</p></td>
<td><p><em>pvResult</em> sera interprété comme un DWORD. Cela retourne l’espace disponible pour la base de données dans les pages.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoSpaceOwned</p></td>
<td><p><em>pvResult</em> sera interprété comme un DWORD. Cela retourne l’espace détenu pour la base de données dans les pages.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoTransactions</p></td>
<td><p><em>pvResult</em> sera interprété comme long. Cela retourne une valeur supérieure au niveau maximal dans lequel les transactions peuvent être imbriquées. Si <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> est appelé (de manière imbriquée, autrement dit, sur la même session, sans validation ou ROLLBACK) autant de fois que cette valeur, sur le dernier appel JET_errTransTooDeep est retourné à partir de <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>. Notez que la valeur dans Windows 2000, Windows XP et Windows Server 2003 est 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoVersion</p></td>
<td><p><em>pvResult</em> sera interprété comme long. Cela retourne la version principale native du moteur de base de données. Cette valeur est 0x620 pour Windows 2000, Windows XP et Windows Server 2003.</p></td>
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
<td><p>La taille de la mémoire tampon donnée dans <em>cbMax</em> est trop petite (ou incorrecte) pour contenir les informations souhaitées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Le <em>InfoLevel</em> demandé a été JET_DbInfoIsam. Cela n'est pas pris en charge.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>La taille de la mémoire tampon donnée dans <em>cbMax</em> est trop petite (ou incorrecte) pour contenir les informations souhaitées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cette erreur est retournée par <strong>JetGetDatabaseInfo</strong> lorsque le <a href="gg269248(v=exchg.10).md">JET_DBID</a> fourni n’est pas une base de données (attachée) valide. Cette erreur est retournée par <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> et <strong>JetGetDatabaseInfo</strong> lorsqu’un <em>InfoLevel</em> demandé n’est pas pris en charge par cette version de la fonction.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, les données demandées sont retournées dans la mémoire tampon de sortie.

En cas d’échec, la mémoire tampon de sortie est dans un État indéfini.

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
<td><p>Implémenté en tant que <strong>JetGetDatabaseInfoW</strong> (Unicode) et <strong>JetGetDatabaseInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
