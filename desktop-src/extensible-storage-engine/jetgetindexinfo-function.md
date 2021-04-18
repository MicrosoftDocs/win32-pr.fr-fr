---
description: 'En savoir plus sur : fonction JetGetIndexInfo'
title: Fonction JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520044"
---
# <a name="jetgetindexinfo-function"></a>Fonction JetGetIndexInfo


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgetindexinfo-function"></a>Fonction JetGetIndexInfo

La fonction **JetGetIndexInfo** récupère des informations sur un index.

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*dbid*

Identificateur de base de données à utiliser pour l’appel d’API.

*szTableName*

Nom de la table contenant l’index avec les informations à récupérer.

*szIndexName*

Nom de l’index avec les informations à récupérer.

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations souhaitées. La mémoire tampon doit être alignée pour contenir le type requis. Le type de la mémoire tampon dépend du paramètre *InfoLevel* .

*cbResult*

Taille, en octets, de la mémoire tampon transmise en tant que *pvResult*.

*InfoLevel*

Informations qui seront stockées dans *pvResult*. Les options suivantes peuvent être utilisées pour ce paramètre.

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
<td><p>JET_IdxInfo</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . En cas de réussite, la structure <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> reçoit des informations sur l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCount</p></td>
<td><p><em>pvResult</em> est interprété comme ulong. En cas de réussite, ULONG conserve le nombre d’index sur la table spécifiée. <em>szIndexName</em> est ignoré. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoIndexId</p></td>
<td><p><em>pvResult</em> est interprété comme un <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. En cas de réussite, la structure <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> reçoit des informations sur l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoLangid</p></td>
<td><p>JET_IdxInfoLangid est déconseillé. Utilisez à la place JET_IdxInfoLCID et la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoLCID</p></td>
<td><p><em>pvResult</em> est interprété comme un LCID. En cas de réussite, le LCID contient l’identificateur de paramètres régionaux de l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p>
<p><strong>Windows XP :  </strong> JET_IdxInfoLCID est introduite dans Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoList</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . En cas de réussite, la structure <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> reçoit des informations sur l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoOLC</p></td>
<td><p>JET_IdxInfoOLC est obsolète.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoResetOLC</p></td>
<td><p>JET_IdxInfoResetOLC est obsolète.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoSpaceAlloc</p></td>
<td><p><em>pvResult</em> est interprété comme ulong. En cas de réussite, ULONG conserve l’utilisation de l’espace de l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoSysTabCursor</p></td>
<td><p>JET_IdxInfoSysTabCursor est obsolète.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoVarSegMac</p></td>
<td><p><em>pvResult</em> est interprété comme un UShort. En cas de réussite, le USHORT contient la valeur de <em>cbVarSegMac</em> utilisée lors de la création de l’index. Consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> pour obtenir une description de <em>cbVarSegMac</em>. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoKeyMost</p></td>
<td><p><em>pvResult</em> est interprété comme un UShort. En cas de réussite, le USHORT contient la valeur de <em>cbKeyMost</em> utilisée lors de la création de l’index. Consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> pour obtenir une description de <em>cbKeyMost</em>. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p>
<p><strong>Windows Vista :  </strong> JET_IdxInfoKeyMost est introduite dans Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_IdxInfoCreateIndex</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p>
<p><strong>Windows 7 :  </strong> JET_IdxInfoCreateIndex est introduite dans Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_IdxInfoCreateIndex2</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p>
<p><strong>Windows 7 :  </strong> JET_IdxInfoCreateIndex2 est introduite dans Windows 7.</p></td>
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
<td><p>JET_errIndexNotFound</p></td>
<td><p>L’index spécifié est introuvable dans la table spécifiée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>La mémoire tampon transmise en tant que <em>pvResult</em> est trop petite. Le contenu de la mémoire tampon n’est pas défini.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

**JetGetIndexInfo** et [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) récupèrent des informations identiques sur un index. La différence réside dans le mode de spécification de la table. **JetGetIndexInfo** attend une base de données (*dbid*) et un nom de table (*szTableName*), tandis que [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) attend un identificateur de table (*TableID*).

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
<td><p>Implémenté en tant que <strong>JetGetIndexInfoW</strong> (Unicode) et <strong>JetGetIndexInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
