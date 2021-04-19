---
description: 'En savoir plus sur : structure JET_CONDITIONALCOLUMN'
title: Structure JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531813"
---
# <a name="jet_conditionalcolumn-structure"></a>Structure JET_CONDITIONALCOLUMN


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_conditionalcolumn-structure"></a>Structure JET_CONDITIONALCOLUMN

La structure **JET_CONDITIONALCOLUMN** définit la manière dont l’indexation conditionnelle est effectuée pour un index donné. Un index conditionnel contient une entrée d’index uniquement pour les lignes qui correspondent à la condition spécifiée. Toutefois, la colonne conditionnelle ne fait pas partie de la clé de l’index, elle contrôle uniquement la présence de l’entrée d’index.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Membres

**cbStruct**

Ce champ doit être initialisé à sizeof (JET_CONDITIONALCOLUMN), en octets.

**szColumnName**

Nom de la colonne qui contient les données sur lesquelles le moteur de base de données indexe conditionnellement la ligne.

**Grbit** Groupe de bits qui fournit les options pour l’index conditionnel. Le passage de valeurs zéro ou d’une valeur de logique **ou** Ed n’est pas valide pour **JET_CONDITIONALCOLUMN**. Le champ de bits doit correspondre exactement à l’un des éléments suivants :

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
<td><p>JET_bitIndexColumnMustBeNull</p></td>
<td><p>La colonne spécifiée par le paramètre <em>szColumnName</em> doit avoir la valeur null pour qu’une entrée d’index d’une ligne donnée apparaisse dans cet index.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexColumnMustBeNonNull</p></td>
<td><p>La colonne spécifiée par le paramètre <em>szColumnName</em> doit être non null pour une entrée d’index afin qu’une ligne donnée apparaisse dans cet index.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Notes

Un index conditionnel contient une entrée d’index uniquement pour les lignes qui correspondent à la condition spécifiée. Par exemple, une colonne peut être nommée « marquée » et lorsqu’une ligne est marquée, la colonne est définie sur une valeur non NULL. Un JET_bitIndexColumnMustBeNonNull index conditionnel sur cette colonne affiche toutes les lignes marquées, et un index conditionnel JET_bitIndexColumnMustBeNull affiche les lignes qui ne sont pas marquées. Il s’agit également d’un moyen pratique d’effectuer une suppression d’indicateur et un index de garbage collection.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté comme <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) et <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
