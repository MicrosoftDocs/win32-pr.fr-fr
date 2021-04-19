---
description: 'En savoir plus sur : fonction de rappel JET_CALLBACK'
title: JET_CALLBACK fonction de rappel
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519773"
---
# <a name="jet_callback-callback-function"></a>JET_CALLBACK fonction de rappel


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_callback-callback-function"></a>JET_CALLBACK fonction de rappel

La fonction **JET_CALLBACK** est une fonction de rappel polyvalente utilisée par le moteur de base de données pour informer l’application d’un événement impliquant la défragmentation en ligne et les notifications de l’état du curseur.

Consultez [JET_CBTYP](./jet-cbtyp.md) pour connaître les paramètres spécifiques à utiliser pour les paramètres de cette fonction, car ces paramètres diffèrent en fonction de l’option **JET_CBTYP** sélectionnée pour être utilisée dans le paramètre *CBTYP* .

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session pour laquelle le rappel est effectué.

*dbid*

Base de données pour laquelle le rappel est effectué.

*TableID*

Curseur pour lequel le rappel est effectué.

*cbtyp*

Point de l’opération au niveau duquel le rappel est effectué. Consultez [JET_CBTYP](./jet-cbtyp.md) pour obtenir la liste des valeurs et la signification des paramètres suivants dans chaque cas.

*pvArg1*

Paramètre utilisé pour communiquer avec l’application à l’aide du rappel. Consultez [JET_CBTYP](./jet-cbtyp.md) pour plus d’informations sur l’utilisation de ce paramètre pour chaque rappel pris en charge par le moteur de base de données.

*pvArg2*

Paramètre utilisé pour communiquer avec l’application à l’aide du rappel. Consultez [JET_CBTYP](./jet-cbtyp.md) pour plus d’informations sur l’utilisation de ce paramètre pour chaque rappel pris en charge par le moteur de base de données.

*pvContext*

Paramètre utilisé pour communiquer avec l’application à l’aide du rappel. Consultez [JET_CBTYP](./jet-cbtyp.md) pour plus d’informations sur l’utilisation de ce paramètre pour chaque rappel pris en charge par le moteur de base de données.

*ulUnused*

Paramètre utilisé pour communiquer avec l’application à l’aide du rappel. Consultez [JET_CBTYP](./jet-cbtyp.md) pour plus d’informations sur l’utilisation de ce paramètre pour chaque rappel pris en charge par le moteur de base de données.

#### <a name="return-value"></a>Valeur renvoyée

La fonction retourne l’un des [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md). Pour plus d’informations sur la façon de renvoyer ces codes en tant que HRESULT, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md). En cas de réussite, l’opération qui a émis le rappel peut se poursuivre normalement. Dans certains cas, le rappel peut retourner un avertissement qui influence cette opération. Pour plus d’informations sur l’utilisation de ces avertissements par l’opération, consultez [JET_CBTYP](./jet-cbtyp.md) .

En cas d’échec, l’opération qui a émis le rappel peut se poursuivre normalement ou échouer. Pour plus d’informations sur l’utilisation du code d’erreur par l’opération, consultez [JET_CBTYP](./jet-cbtyp.md) .

#### <a name="remarks"></a>Notes

Si le rappel passe un curseur à l’application, il est important de savoir que ce curseur est intentionnellement limité à un ensemble de fonctionnalités plus réduit pour éviter la récursivité et d’autres ugliness. Les opérations suivantes sont autorisées :

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCurrentIndex](./jetgetcurrentindex-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordPosition](./jetgetrecordposition-function.md)

  - [JetGetSecondaryIndexBookmark](./jetgetsecondaryindexbookmark-function.md)

  - [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)

  - [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetRegisterCallback](./jetregistercallback-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUnregisterCallback](./jetunregistercallback-function.md)

Lorsque vous concevez votre rappel, prenez en compte le fait que même avec ces restrictions, il est toujours possible que le rappel échoue.

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
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)
