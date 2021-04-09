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
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112107"
---
# <a name="jet_enumcolumn-structure"></a>Structure JET_ENUMCOLUMN


_**S’applique à :** Windows | Serveur Windows_

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codes d’erreur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errBadColumnId</p></td>
<td><p>L’ID de colonne est en dehors des limites autorisées d’un ID de colonne.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>La colonne décrite par l’ID de colonne n’existe pas dans la table.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>Toutes les valeurs de cette colonne sont NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnPresent</p></td>
<td><p>JET_bitEnumeratePresenceOnly a été spécifié et au moins une valeur de colonne non NULL aurait été retournée pour cette colonne.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnSingleValue</p></td>
<td><p>JET_bitEnumerateCompressOutput a été spécifié et une seule valeur de colonne non NULL a été retournée pour cette colonne. Par conséquent, la forme compressée de <strong>JET_ENUMCOLUMN</strong> a été retournée. Pour plus d’informations, consultez <strong>JET_ENUMCOLUMN</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnSkipped</p></td>
<td><p>L’ID de colonne dans le struct <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> qui correspond à ce <strong>JET_ENUMCOLUMN</strong> struct était égal à zéro.</p></td>
</tr>
</tbody>
</table>


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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
