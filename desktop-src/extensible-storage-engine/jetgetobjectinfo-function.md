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
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538899"
---
# <a name="jetgetobjectinfo-function"></a>JetGetObjectInfo, fonction


_**S’applique à :** Windows | Serveur Windows_

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
<td><p>JET_ObjInfo</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</p>
<p>La structure <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> est remplie avec les informations relatives à l’objet nommé dans <em>szObjectName</em>.</p>
<p>Si l’appelant ne souhaite pas connaître le nombre d’enregistrements et de pages pour l’objet, envisagez d’utiliser JET_ObjInfoNoStats niveau d’informations, ce qui peut être plus rapide, car les statistiques ne sont pas incluses.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoList</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Les informations sur tous les objets sont récupérées. Une table temporaire est créée, et les informations nécessaires pour parcourir la table temporaire sont décrites dans la structure <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Pour plus d’informations, consultez <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. Si l’appelant ne souhaite pas connaître le nombre d’enregistrements et de pages de l’objet, envisagez d’utiliser JET_ObjInfoListNoStats, ce qui peut être plus rapide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoListACM</p></td>
<td><p>Déconseillé et non pris en charge actuellement.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoListNoStats</p></td>
<td><p><em>pvResult</em> est interprété comme une structure de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Les informations sur tous les objets sont récupérées. Une table temporaire est créée, et les informations nécessaires pour parcourir la table temporaire sont décrites dans la structure <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> . Pour plus d’informations, consultez <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>. JET_ObjInfoListNoStats est identique à JET_ObjInfoList, sauf que les colonnes qui indiquent le nombre d’enregistrements (<em>columnidcRecord</em>) et les pages (<em>columnidcPage</em>) ne seront pas mises à jour.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoMax</p></td>
<td><p><em>pvResult</em> est interprété comme un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. La taille maximale de l’objet est de pages. Actuellement, seules les tables sont retournées.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoNoStats</p></td>
<td><p><em>pvResult</em> est interprété comme un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>. Les informations sur l’objet donné dans <em>szObjectName</em> sont récupérées.</p>
<p>La structure <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> sera remplie avec les informations relatives à l’objet nommé dans <em>szObjectName</em>.</p>
<p>JET_ObjInfoNoStats est identique à JET_ObjInfo, à ceci près que les champs qui indiquent le nombre d’enregistrements et de pages sont définis à zéro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoRulesLoaded</p></td>
<td><p>Déconseillé et non pris en charge actuellement.</p></td>
</tr>
<tr class="even">
<td><p>JET_ObjInfoSysTabCursor</p></td>
<td><p>Déconseillé et non pris en charge actuellement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ObjInfoSysTabReadOnly</p></td>
<td><p>Déconseillé et non pris en charge actuellement.</p></td>
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
<td><p>La taille de la mémoire tampon donnée dans <em>cbMax</em> est trop petite pour contenir les informations souhaitées.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Un nom non valide a été spécifié dans <em>szObjectName</em> ou <em>szContainerName</em>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un paramètre incorrect a été donné. Il est possible qu’un niveau incorrect a été passé à <em>InfoLevel</em>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

Si **JetGetObjectInfo** crée avec succès une table temporaire (par exemple, JET_ObjInfoList ou JET_ObjInfoNoStats), l’appelant est responsable de la fermeture de la table temporaire avec [JetCloseTable](./jetclosetable-function.md).

Actuellement, **JetGetObjectInfo** prend uniquement en charge la récupération d’informations sur les tables.

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
<td><p>Implémenté en tant que <strong>JetGetObjectInfoW</strong> (Unicode) et <strong>JetGetObjectInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
