---
description: 'En savoir plus sur : structure JET_ENUMCOLUMNID'
title: Structure JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526085"
---
# <a name="jet_enumcolumnid-structure"></a>Structure JET_ENUMCOLUMNID


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_enumcolumnid-structure"></a>Structure JET_ENUMCOLUMNID

La structure **JET_ENUMCOLUMNID** énumère un ensemble spécifique de colonnes et, éventuellement, un ensemble spécifique de plusieurs valeurs pour ces colonnes lorsque la fonction [JetEnumerateColumns](./jetenumeratecolumns-function.md) est utilisée. [JetEnumerateColumns](./jetenumeratecolumns-function.md) retourne un tableau de structures **JET_ENUMCOLUMNID** .

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>Membres

**ColumnID**

ID de colonne à énumérer.

Si l’ID de colonne est 0 (zéro), l’énumération de cette colonne est ignorée et un emplacement correspondant dans le tableau de sortie des structures de [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) est généré avec un état de colonne de JET_wrnColumnSkipped.

**ctagSequence**

Identifie éventuellement un tableau de valeurs de colonne (par index de base un) à énumérer pour l’ID de colonne spécifié.

Si **ctagSequence** a la valeur 0 (zéro), **rgtagSequence** est ignoré et toutes les valeurs de colonne pour l’ID de colonne spécifié seront énumérées.

Si un élément de **rgtagSequence** est 0 (zéro), l’énumération de cette valeur de colonne (par index de base un) sera ignorée. Un emplacement correspondant dans le tableau de sortie de la structure **JET_ENUMCOLUMNID** sera généré avec une valeur d’état de colonne de JET_wrnColumnSkipped.

**rgtagSequence**

Tableau d’index de base un dans le tableau de valeurs de colonne pour une colonne donnée. Un élément unique est un **itagSequence** qui est défini dans [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). Un **itagSequence** de 0 (zéro) signifie « Skip ». Un **itagSequence** de 1 signifie que retourne la première valeur de colonne de la colonne, 2 le second, et ainsi de suite.

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
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)
