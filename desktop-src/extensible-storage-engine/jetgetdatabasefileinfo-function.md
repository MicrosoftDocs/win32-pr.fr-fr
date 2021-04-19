---
description: 'En savoir plus sur : fonction JetGetDatabaseFileInfo'
title: JetGetDatabaseFileInfo fonction)
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524732"
---
# <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgetdatabasefileinfo-function"></a>JetGetDatabaseFileInfo fonction)

La fonction **JetGetDatabaseFileInfo** récupère différents types d’informations sur la base de données. Cette API peut être appelée lorsqu’une base de données est attachée ou en ligne (avec [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) ou que la base de données ou le moteur de base de données est hors connexion (avec **JetGetDatabaseFileInfo**).

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*szDatabaseName*

Chemin d’accès de la base de données à partir de laquelle récupérer les informations.

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations spécifiées. La taille de la mémoire tampon, en octets, est passée dans *cbMax*.

Si cette fonction échoue, le contenu de *pvResult* n’est pas défini.

Les informations stockées dans *pvResult* dépendent de *InfoLevel*.

*cbMax*

Taille, en octets, de la mémoire tampon passée dans *pvResult*.

*InfoLevel*

*InfoLevel* spécifie le type d’informations à récupérer sur la base de données spécifiée. Cela affecte la façon dont *pvResult* est interprété. Certains objets *InfoLevel* sont disponibles uniquement dans la version hors connexion (**JetGetDatabaseFileInfo**) ou en ligne ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) de l’API.

Si la mémoire tampon *pvResult* fournie est trop petite, JET_errInvalidBufferSize ou JET_errBufferTooSmall sera retourné, en fonction du *InfoLevel*.

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
<td><p>JET_DbInfoFilesize</p></td>
<td><p><em>pvResult</em> sera interprété comme un QWORD (8 octets). Retourne la taille de la base de données en octets.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoUpgrade</p></td>
<td><p><em>pvResult</em> sera interprété comme un <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>. La structure <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> sera remplie avec les informations relatives à la base de données spécifiée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoMisc</p></td>
<td><p><em>pvResult</em> sera interprété comme un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La structure <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> sera remplie avec les informations relatives à la base de données spécifiée.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoDBInUse</p></td>
<td><p><em>pvResult</em> sera interprété comme un bool (4 octets). Cela indique si le moteur de base de données a actuellement des bases de données ouvertes ou attachées.</p>
<p><strong>Windows XP :  </strong> Cette valeur est introduite dans Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoPageSize</p></td>
<td><p><em>pvResult</em> sera interprété comme un entier long non signé. Cela renverra la taille de page de la base de données en octets.</p>
<p><strong>Windows XP :  </strong> Cette valeur est introduite dans Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCp</p></td>
<td><p>Ces <em>InfoLevels</em> ne sont pas encore pris en charge et retournent des valeurs par défaut. N’utilisez pas ces <em>InfoLevels</em>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoCountry</p></td>
<td><p>Ces <em>InfoLevels</em> ne sont pas encore pris en charge et retournent des valeurs par défaut. N’utilisez pas ces <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoCollate</p></td>
<td><p>Identique à JET_DbInfoCp.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoIsam</p></td>
<td><p>Ces <em>InfoLevels</em> sont déconseillés et ne sont pas pris en charge actuellement. N’utilisez pas ces <em>InfoLevels</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_DbInfoConnect</p></td>
<td><p>Identique à JET_DbInfoIsam.</p></td>
</tr>
<tr class="odd">
<td><p>JET_DbInfoFileType</p></td>
<td><p><strong>Windows Vista :  </strong> Cette valeur <em>InfoLevel</em> est introduite dans Windows Vista.</p>
<p><em>pvResult</em> sera traité comme un pointeur vers une valeur DWORD. Retourne une valeur d’énumération, indiquant le type de fichier que le moteur considère comme étant. Les types de fichiers sont répertoriés dans le tableau suivant. Pour plus d’informations sur ces types de fichiers et leur utilisation pour le moteur, voir <a href="gg294069(v=exchg.10).md">fichiers ESE (Extensible Storage Engine</a>).</p>
<div class="tableSection">
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
<td><p>JET_filetypeUnknown</p></td>
<td><p>Le type de fichier est inconnu ou n’est pas un type de fichier ESE.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeDatabase</p></td>
<td><p>Le fichier est un fichier de base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeLog</p></td>
<td><p>Le fichier est un fichier journal de transactions.</p></td>
</tr>
<tr class="even">
<td><p>JET_filetypeCheckpoint</p></td>
<td><p>Le fichier est un fichier de point de contrôle.</p></td>
</tr>
<tr class="odd">
<td><p>JET_filetypeTempDatabase</p></td>
<td><p>Le fichier est un fichier de base de données temporaire.</p></td>
</tr>
</tbody>
</table>

</div></td>
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
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>Le <em>InfoLevel</em> demandé a été JET_DbInfoIsam. Cela n'est pas pris en charge.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>La mémoire tampon fournie dans <em>cbMax</em> est trop petite pour les informations souhaitées.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>La mémoire tampon fournie dans <em>cbMax</em> n’est pas la taille correcte pour les informations souhaitées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a produit un résultat inattendu. Cette erreur est retournée par <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> lorsque le dbid fourni n’est pas une base de données (attachée) valide. Cette erreur est retournée par <strong>JetGetDatabaseFileInfo</strong> et <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> lorsqu’un <em>InfoLevel</em> demandé n’est pas pris en charge par cette version de la fonction.</p></td>
</tr>
</tbody>
</table>


Si cette fonction est réussie, les données demandées sont retournées dans la mémoire tampon de sortie.

Si cette fonction échoue, la mémoire tampon de sortie est dans un État indéfini.

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
<td><p>Implémenté en tant que <strong>JetGetDatabaseFileInfoW</strong> (Unicode) et <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)
