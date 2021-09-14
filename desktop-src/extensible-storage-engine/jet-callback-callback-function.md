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
ms.openlocfilehash: 8a49c63a948cd25abe97dfc58e10a97720eae248
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012533"
---
# <a name="jet_callback-callback-function"></a>JET_CALLBACK fonction de rappel


_**S’applique à :** Windows | Windows Serveurs_

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

la fonction retourne l’un des [codes d’erreur du moteur d’Stockage Extensible](./extensible-storage-engine-error-codes.md). pour plus d’informations sur la façon de retourner ces codes en tant que HRESULTs, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md). En cas de réussite, l’opération qui a émis le rappel peut se poursuivre normalement. Dans certains cas, le rappel peut retourner un avertissement qui influence cette opération. Pour plus d’informations sur l’utilisation de ces avertissements par l’opération, consultez [JET_CBTYP](./jet-cbtyp.md) .

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

#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_API_PTR](./jet-api-ptr.md)  
[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_CBTYP](./jet-cbtyp.md)
