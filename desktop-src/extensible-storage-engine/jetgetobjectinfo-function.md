---
description: 'En savoir plus sur : fonction JetGetObjectInfo'
title: JetGetObjectInfo, fonction
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e6317280c5e794e9809c15f47f01d55ffd48eeb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982422"
---
# <a name="jetgetobjectinfo-function"></a>JetGetObjectInfo, fonction


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetobjectinfo-function"></a>JetGetObjectInfo, fonction

La fonction **JetGetObjectInfo** récupère des informations sur les objets de base de données. Actuellement, seules les tables sont prises en charge. [JetGetTableInfo](./jetgettableinfo-function.md) peut être utilisé pour extraire plus d’informations que **JetGetObjectInfo**.

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser.

*dbid*

Base de données à partir de laquelle les informations sont récupérées.

*objtyp*

Objets qui contiennent des informations à récupérer. À l’heure actuelle, seuls les JET_objtypNil et les JET_objtypTable sont pris en charge, tous deux ayant un comportement identique. Seules les tables seront récupérées.

*szContainerName*

Ce paramètre est réservé pour une utilisation ultérieure et passe la **valeur null**. Nom des types d’objets à propos desquels récupérer des informations.

*szObjectName*

Nom de l’objet qui contient les informations à récupérer. Quand *InfoLevel* utilise les options JET_ObjInfoList ou JET_ObjInfoListNoStats pour récupérer une liste de tous les objets, cette valeur doit être **null** ou une chaîne vide.

Seuls les noms de tables sont actuellement pris en charge.

*pvResult*

Pointeur vers une mémoire tampon qui reçoit les informations spécifiées.

La taille de la mémoire tampon, en octets, est passée dans *cbMax*. En cas d’échec, le contenu de *pvResult* n’est pas défini.

Les informations stockées dans *pvResult* dépendent de *InfoLevel*.

*cbMax*

Taille, en octets, de la mémoire tampon passée dans *pvResult*.

*InfoLevel*

Spécifie le type d’informations à récupérer pour l’objet spécifié. Cela affecte la façon dont *pvResult* est interprété.

Les options suivantes peuvent être définies pour ce paramètre.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_ObjInfo</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</p><p>La structure <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> est remplie avec les informations relatives à l’objet nommé dans <em>szObjectName</em>.</p><p>Si l’appelant ne souhaite pas connaître le nombre d’enregistrements et de pages pour l’objet, envisagez d’utiliser JET_ObjInfoNoStats niveau d’informations, ce qui peut être plus rapide, car les statistiques ne sont pas incluses.</p> | 
| <p>JET_ObjInfoList</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Les informations sur tous les objets sont récupérées. Une table temporaire est créée, et les informations nécessaires pour parcourir la table temporaire sont décrites dans la structure <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Pour plus d’informations, consultez <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. Si l’appelant ne souhaite pas connaître le nombre d’enregistrements et de pages de l’objet, envisagez d’utiliser JET_ObjInfoListNoStats, ce qui peut être plus rapide.</p> | 
| <p>JET_ObjInfoListACM</p> | <p>Déconseillé et non pris en charge actuellement.</p> | 
| <p>JET_ObjInfoListNoStats</p> | <p><em>pvResult</em> est interprété comme une structure de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Les informations sur tous les objets sont récupérées. Une table temporaire est créée, et les informations nécessaires pour parcourir la table temporaire sont décrites dans la structure <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Pour plus d’informations, consultez <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. JET_ObjInfoListNoStats est identique à JET_ObjInfoList, sauf que les colonnes qui indiquent le nombre d’enregistrements (<em>columnidcRecord</em>) et les pages (<em>columnidcPage</em>) ne seront pas mises à jour.</p> | 
| <p>JET_ObjInfoMax</p> | <p><em>pvResult</em> est interprété comme un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. La taille maximale de l’objet est de pages. Actuellement, seules les tables sont retournées.</p> | 
| <p>JET_ObjInfoNoStats</p> | <p><em>pvResult</em> est interprété comme un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Les informations sur l’objet donné dans <em>szObjectName</em> sont récupérées.</p><p>La structure <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> sera remplie avec les informations relatives à l’objet nommé dans <em>szObjectName</em>.</p><p>JET_ObjInfoNoStats est identique à JET_ObjInfo, à ceci près que les champs qui indiquent le nombre d’enregistrements et de pages sont définis à zéro.</p> | 
| <p>JET_ObjInfoRulesLoaded</p> | <p>Déconseillé et non pris en charge actuellement.</p> | 
| <p>JET_ObjInfoSysTabCursor</p> | <p>Déconseillé et non pris en charge actuellement.</p> | 
| <p>JET_ObjInfoSysTabReadOnly</p> | <p>Déconseillé et non pris en charge actuellement.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>La taille de la mémoire tampon donnée dans <em>cbMax</em> est trop petite pour contenir les informations souhaitées.</p> | 
| <p>JET_errInvalidName</p> | <p>Un nom non valide a été spécifié dans <em>szObjectName</em> ou <em>szContainerName</em>.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un paramètre incorrect a été donné. Il est possible qu’un niveau incorrect a été passé à <em>InfoLevel</em>.</p> | 



#### <a name="remarks"></a>Remarques

Si **JetGetObjectInfo** crée avec succès une table temporaire (par exemple, JET_ObjInfoList ou JET_ObjInfoNoStats), l’appelant est responsable de la fermeture de la table temporaire avec [JetCloseTable](./jetclosetable-function.md).

Actuellement, **JetGetObjectInfo** prend uniquement en charge la récupération d’informations sur les tables.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetGetObjectInfoW</strong> (Unicode) et <strong>JetGetObjectInfoA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
