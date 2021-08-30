---
description: 'En savoir plus sur : structure JET_ENUMCOLUMN'
title: Structure JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: 7f0fa6d326120355e43b29cd87e13d5c0ebbf68b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474535"
---
# <a name="jet_enumcolumn-structure"></a>Structure JET_ENUMCOLUMN


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_enumcolumn-structure"></a>Structure JET_ENUMCOLUMN

La structure **JET_ENUMCOLUMN** énumère les valeurs de colonne d’un enregistrement lorsque la fonction [JetEnumerateColumns](./jetenumeratecolumns-function.md) est utilisée. [JetEnumerateColumns](./jetenumeratecolumns-function.md) retourne un tableau de structures **JET_ENUMCOLUMN** . Le tableau est retourné dans la mémoire qui est allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible qui a été fourni à cette API.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a>Membres

**ColumnID**

ID de colonne qui a été énuméré.

**Raise**

Code d’état de la colonne qui résulte de l’énumération de la colonne.


| <p>Codes d’erreur</p> | <p>Signification</p> | 
|--------------------|----------------|
| <p>JET_errBadColumnId</p> | <p>L’ID de colonne est en dehors des limites autorisées d’un ID de colonne.</p> | 
| <p>JET_errColumnNotFound</p> | <p>La colonne décrite par l’ID de colonne n’existe pas dans la table.</p> | 
| <p>JET_wrnColumnNull</p> | <p>Toutes les valeurs de cette colonne sont NULL.</p> | 
| <p>JET_wrnColumnPresent</p> | <p>JET_bitEnumeratePresenceOnly a été spécifié et au moins une valeur de colonne non NULL aurait été retournée pour cette colonne.</p> | 
| <p>JET_wrnColumnSingleValue</p> | <p>JET_bitEnumerateCompressOutput a été spécifié et une seule valeur de colonne non NULL a été retournée pour cette colonne. Par conséquent, la forme compressée de <strong>JET_ENUMCOLUMN</strong> a été retournée. Pour plus d’informations, consultez <strong>JET_ENUMCOLUMN</strong> .</p> | 
| <p>JET_wrnColumnSkipped</p> | <p>L’ID de colonne dans le struct <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> qui correspond à ce <strong>JET_ENUMCOLUMN</strong> struct était égal à zéro.</p> | 



**cEnumColumnValue**

Tableau de valeurs de colonne qui a été énuméré pour la colonne. La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Cette mémoire tampon de sortie est utilisée lorsque le code d’état de la colonne n’est pas égal à JET_wrnColumnSingleValue. Pour plus d’informations, consultez [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Cette erreur est retournée si « Err \! = JET_wrnColumnSingleValue ».

**rgEnumColumnValue**

Tableau de valeurs de colonne qui a été énuméré pour la colonne. La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Cette mémoire tampon de sortie est utilisée lorsque le code d’état de la colonne n’est pas égal à JET_wrnColumnSingleValue. Pour plus d’informations, consultez [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Cette erreur est retournée si « Err \! = JET_wrnColumnSingleValue ».

**cbData**

Valeur de colonne qui a été énumérée pour la colonne.

La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Cette mémoire tampon de sortie est utilisée uniquement lorsque le code d’état de la colonne est JET_wrnColumnSingleValue. Pour plus d’informations, consultez [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Cette erreur est retournée si « Err = = JET_wrnColumnSingleValue ».

**pvData**

Valeur de colonne qui a été énumérée pour la colonne.

La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Cette mémoire tampon de sortie est utilisée uniquement lorsque le code d’état de la colonne est JET_wrnColumnSingleValue. Pour plus d’informations, consultez [JetEnumerateColumns](./jetenumeratecolumns-function.md).

Cette erreur est retournée si « Err = = JET_wrnColumnSingleValue ».

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
