---
description: 'En savoir plus sur : fonction JetGetTableIndexInfo'
title: Fonction JetGetTableIndexInfo
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2066e3d20ef98d71c4c891d941d322e993b309e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917191"
---
# <a name="jetgettableindexinfo-function"></a>Fonction JetGetTableIndexInfo


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgettableindexinfo-function"></a>Fonction JetGetTableIndexInfo

La fonction **JetGetTableIndexInfo** récupère des informations sur un index.

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table de base de données qui contient l’index qui contient les informations nécessaires.

*szIndexName*

Nom de l’index qui contient les informations qui seront récupérées.

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations. La mémoire tampon doit être alignée pour contenir le type requis. Le type de la mémoire tampon dépend du paramètre *InfoLevel* .

*cbResult*

Taille, en octets, de la mémoire tampon passée dans le paramètre *pvResult* .

*InfoLevel*

Spécifie les informations qui seront stockées dans *pvResult*. Les valeurs valides sont les suivantes :


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_IdxInfo</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . En cas de réussite, la structure <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> reçoit des informations sur l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p> | 
| <p>JET_IdxInfoLCID</p> | <p><em>pvResult</em> est interprété comme un LCID. En cas de réussite, le LCID contient l’identificateur de paramètres régionaux de l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p> | 
| <p>JET_IdxInfoList</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> . En cas de réussite, la structure <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> reçoit des informations sur l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p> | 
| <p>JET_IdxInfoOLC</p> | <p>JET_IdxInfoOLC est obsolète.</p> | 
| <p>JET_IdxInfoResetOLC</p> | <p>JET_IdxInfoResetOLC est obsolète.</p> | 
| <p>JET_IdxInfoSpaceAlloc</p> | <p><em>pvResult</em> est interprété comme ulong. En cas de réussite, ULONG conserve l’utilisation de l’espace de l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p> | 
| <p>JET_IdxInfoSysTabCursor</p> | <p>JET_IdxInfoSysTabCursor est obsolète.</p> | 
| <p>JET_IdxInfoLangid</p> | <p>JET_IdxInfoLangid est déconseillé. Utilisez à la place JET_IdxInfoLCID et la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</p> | 
| <p>JET_IdxInfoCount</p> | <p><em>pvResult</em> est interprété comme ulong. En cas de réussite, ULONG conserve le nombre d’index sur la table spécifiée. <em>szIndexName</em> est ignoré. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p> | 
| <p>JET_IdxInfoVarSegMac</p> | <p><em>pvResult</em> est interprété comme un UShort. En cas de réussite, le USHORT contient la valeur de <em>cbVarSegMac</em> utilisée lors de la création de l’index. Consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> pour obtenir une description de <em>cbVarSegMac</em>. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p> | 
| <p>JET_IdxInfoIndexId</p> | <p><em>pvResult</em> est interprété comme un <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>. En cas de réussite, la structure <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> reçoit des informations sur l’index. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p> | 
| <p>JET_IdxInfoKeyMost</p> | <p><em>pvResult</em> est interprété comme un UShort. En cas de réussite, le USHORT contient la valeur de cbKeyMost utilisée lors de la création de l’index. Consultez la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> pour obtenir une description de cbKeyMost. En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p> | 
| <p>JET_IdxInfoCreateIndex</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p><p><strong>Windows 7 :</strong> JET_IdxInfoCreateIndex est introduite dans Windows 7.</p> | 
| <p>JET_IdxInfoCreateIndex2</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</p><p><strong>Windows 7 :</strong> JET_IdxInfoCreateIndex2 est introduite dans Windows 7.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errIndexNotFound</p> | <p>L’index spécifié est introuvable dans la table spécifiée.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>La mémoire tampon transmise en tant que <em>pvResult</em> est trop petite. Le contenu de la mémoire tampon n’est pas défini.</p> | 



#### <a name="remarks"></a>Notes

[JetGetIndexInfo](./jetgetindexinfo-function.md) et **JetGetTableIndexInfo** récupèrent des informations identiques sur un index. La différence réside dans le mode de spécification de la table. [JetGetIndexInfo](./jetgetindexinfo-function.md) attend une base de données (*dbid*) et un nom de table (*szTableName*), tandis que **JetGetTableIndexInfo** attend un identificateur de table (*TableID*).

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetGetTableIndexInfoW</strong> (Unicode) et <strong>JetGetTableIndexInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)
