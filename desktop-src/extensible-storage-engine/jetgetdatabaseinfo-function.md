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
ms.openlocfilehash: 335ad13411dbfcc83dce559eb4b77adefcc8a5da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477955"
---
# <a name="jetgetdatabaseinfo-function"></a>Fonction JetGetDatabaseInfo


_**S’applique à :** Windows | Windows Serveurs_

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


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_DbInfoCollate</p> | <p>Pas encore pris en charge et retournent les valeurs par défaut. Ne pas utiliser.</p> | 
| <p>JET_DbInfoConnect</p> | <p>Ces <em>InfoLevels</em> sont déconseillés et ne sont pas pris en charge actuellement. Ne pas utiliser.</p> | 
| <p>JET_DbInfoCountry</p> | <p>Pas encore pris en charge et retournent les valeurs par défaut. Ne pas utiliser.</p> | 
| <p>JET_DbInfoCp</p> | <p>Pas encore pris en charge et retournent les valeurs par défaut. Ne pas utiliser.</p> | 
| <p>JET_DbInfoFilename</p> | <p><em>pvResult</em> sera interprété comme une mémoire tampon de chaîne (Char *). Une mémoire tampon de MAX_PATH est suggérée, mais pas obligatoire. Si la mémoire tampon n’est pas assez longue, JET_errBufferTooSmall est retourné. La chaîne sera remplie avec le chemin d’accès de la base de données pour ce DBID.</p> | 
| <p>JET_DbInfoFilesize</p> | <p><em>pvResult</em> sera interprété comme un DWORD (4 octets). Retourne la taille de la base de données en pages.</p> | 
| <p>JET_DbInfoIsam</p> | <p>Ces <em>InfoLevels</em> sont déconseillés et ne sont pas pris en charge actuellement. Ne pas utiliser.</p> | 
| <p>JET_DbInfoLCID</p> | <p>(Windows XP et versions ultérieures) ce <em>InfoLevel</em> a été initialement spécifié comme suit : JET_DbInfoLangid (Windows 2000)</p><p><em>pvResult</em> sera interprété comme long. Cela retourne l’identificateur de paramètres régionaux (LCID) associé à cette base de données.</p> | 
| <p>JET_DbInfoMisc</p> | <p><em>pvResult</em> sera interprété comme un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>. La structure <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> sera remplie avec les informations relatives à la base de données spécifiée.</p> | 
| <p>JET_DbInfoOptions</p> | <p><em>pvResult</em> sera interprété comme un <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD). Cela indique si la base de données est ouverte en mode exclusif. Si la base de données est en mode exclusif JET_bitDbExclusive sera définie dans le <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> fourni, sinon zéro est défini. Notez que les autres options de base de données <em>Grbit</em> pour <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> et <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> ne sont pas renvoyées.</p> | 
| <p>JET_DbInfoPageSize</p> | <p>disponible uniquement sur Windows XP et versions ultérieures. <em>pvResult</em> sera interprété comme un entier long non signé. Cela renverra la taille de page de la base de données en octets.</p> | 
| <p>JET_DbInfoSpaceAvailable</p> | <p><em>pvResult</em> sera interprété comme un DWORD. Cela retourne l’espace disponible pour la base de données dans les pages.</p> | 
| <p>JET_DbInfoSpaceOwned</p> | <p><em>pvResult</em> sera interprété comme un DWORD. Cela retourne l’espace détenu pour la base de données dans les pages.</p> | 
| <p>JET_DbInfoTransactions</p> | <p><em>pvResult</em> sera interprété comme long. Cela retourne une valeur supérieure au niveau maximal dans lequel les transactions peuvent être imbriquées. Si <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> est appelé (de manière imbriquée, autrement dit, sur la même session, sans validation ou ROLLBACK) autant de fois que cette valeur, sur le dernier appel JET_errTransTooDeep est retourné à partir de <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>. notez que la valeur de Windows 2000, Windows XP et Windows Server 2003 est 7.</p> | 
| <p>JET_DbInfoVersion</p> | <p><em>pvResult</em> sera interprété comme long. Cela retourne la version principale native du moteur de base de données. cette valeur est 0x620 pour Windows 2000, Windows XP et Windows Server 2003.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>La taille de la mémoire tampon donnée dans <em>cbMax</em> est trop petite (ou incorrecte) pour contenir les informations souhaitées.</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>Le <em>InfoLevel</em> demandé a été JET_DbInfoIsam. Cela n'est pas pris en charge.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>La taille de la mémoire tampon donnée dans <em>cbMax</em> est trop petite (ou incorrecte) pour contenir les informations souhaitées.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cette erreur est retournée par <strong>JetGetDatabaseInfo</strong> lorsque le <a href="gg269248(v=exchg.10).md">JET_DBID</a> fourni n’est pas une base de données (attachée) valide. Cette erreur est retournée par <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> et <strong>JetGetDatabaseInfo</strong> lorsqu’un <em>InfoLevel</em> demandé n’est pas pris en charge par cette version de la fonction.</p> | 



En cas de réussite, les données demandées sont retournées dans la mémoire tampon de sortie.

En cas d’échec, la mémoire tampon de sortie est dans un État indéfini.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetGetDatabaseInfoW</strong> (Unicode) et <strong>JetGetDatabaseInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
