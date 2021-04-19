---
description: 'En savoir plus sur : structure JET_TABLECREATE3'
title: Structure JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516824"
---
# <a name="jet_tablecreate3-structure"></a>Structure JET_TABLECREATE3


_**S’applique à :** Windows | Serveur Windows_

La structure **JET_TABLECREATE3** contient les informations nécessaires pour créer une table remplie avec des colonnes et des index dans une base de données ESE (Extensible Storage Engine) et qui désigne une fonction de rappel. La structure **JET_TABLECREATE3** est utilisée par la fonction [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) .

La structure **JET_TABLECREATE3** a été introduite dans le système d’exploitation Windows 7.

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a>Membres

**cbStruct**

Taille de cette structure en octets (pour une extension future). Elle doit être définie sur sizeof (JET_TABLECREATE3) en octets.

**szTableName**

Nom de la table à créer.

Le nom doit remplir les conditions suivantes :

  - Elle doit avoir une valeur inférieure à JET_cbNameMost, à l’exclusion de la valeur null de fin.

  - Il doit se composer du jeu de caractères suivant : de 0 à 9, de A à Z, de a à z et de toute autre ponctuation, à l’exception du point d’exclamation ( \! ), de la virgule (,), du crochet ouvrant ( \[ ) et du crochet fermant ( \] ), c’est-À-dire des caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c et 0x5d à 0x7F

  - Il ne doit pas commencer par un espace.

  - Il doit comporter au moins un caractère autre qu’un espace.

**szTemplateTableName**

Nom d’une table existante à partir de laquelle hériter le langage de définition de données (DDL) de base. L’utilisation d’une table de modèle permet de créer facilement de nombreuses tables avec des colonnes et des index identiques.

**ulPages**

Nombre initial de pages de base de données à allouer pour la table. La spécification d’un nombre supérieur à un peut réduire la fragmentation si de nombreuses lignes sont insérées dans cette table.

**ulDensity**

Densité de la table, en points de pourcentage. Le nombre doit être égal à 0 ou compris entre 20 et 100. Le passage de 0 signifie que la valeur par défaut doit être utilisée. La valeur par défaut est 80.

**rgcolumncreate**

Tableau de structures de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , chacune d’elles correspondant à une colonne à créer dans la nouvelle table.

**cColumns**

Nombre d’éléments [JET_COLUMNCREATE](./jet-columncreate-structure.md) dans le paramètre *rgcolumncreate* .

**rgindexcreate**

Tableau de structures de [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , chacune d’elles correspondant à un index à créer dans la nouvelle table.

**cIndexes**

Nombre d’éléments [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) dans le paramètre *rgindexcreate* .

**szCallback**

Fonction qui est appelée pendant certains événements. **cbtyp** détermine le moment où la fonction de rappel sera appelée.

Le format de **szCallback** doit être « fonction de module \! », par exemple, « alpha \! bêta » fait référence à la fonction bêta dans le module nommé « alpha ».

Le prototype de la fonction doit correspondre à la fonction de rappel [JET_CALLBACK](./jet-callback-callback-function.md) .

**cbtyp**

Décrit le type de fonction de rappel désigné par **szCallback**. Pour plus d’informations, consultez [JET_CBTYP](./jet-cbtyp.md).

Ce champ de bits est composé d’une ou plusieurs des valeurs de bit listées dans le tableau suivant.

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
<td><p>JET_cbtypFinalize</p></td>
<td><p>La fonction de rappel est appelée lorsqu’une colonne qui peut être finalisée est passée à zéro.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeInsert</p></td>
<td><p>La fonction de rappel sera appelée avant l’insertion de l’enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterInsert</p></td>
<td><p>La fonction de rappel est appelée une fois que le moteur de base de données a terminé l’insertion d’un enregistrement.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeReplace</p></td>
<td><p>La fonction de rappel sera appelée avant la modification d’un enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterReplace</p></td>
<td><p>La fonction de rappel est appelée après la fin de la modification d’un enregistrement.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeDelete</p></td>
<td><p>La fonction de rappel sera appelée avant la suppression d’un enregistrement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterDelete</p></td>
<td><p>La fonction de rappel est appelée après la suppression d’un enregistrement.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypUserDefinedDefaultValue</p></td>
<td><p>La fonction de rappel sera appelée pour calculer une valeur par défaut définie par l’utilisateur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS</p></td>
<td><p>La fonction de rappel sera appelée lorsque le stockage local qui est associé à un curseur doit être libéré.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS</p></td>
<td><p>La fonction de rappel sera appelée lorsque le stockage local qui est associé à une table doit être libéré.</p></td>
</tr>
</tbody>
</table>


**grbit**

Groupe de bits qui contient zéro, une ou plusieurs des valeurs d’option d’appel énumérées dans le tableau suivant.

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
<td><p>JET_bitTableCreateFixedDDL</p></td>
<td><p>Empêche les opérations DDL sur la table (telles que l’ajout ou la suppression de colonnes).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>Indique que la table est une table de modèles. Les nouvelles tables peuvent ensuite spécifier le nom de cette table comme table de modèle. La définition de JET_bitTableCreateTemplateTable implique JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Doit être utilisé conjointement avec JET_bitTableCreateTemplateTable. Obsolète. Ne pas utiliser.</p></td>
</tr>
</tbody>
</table>


**pSeqSpacehints**

Pointeur vers une structure [JET_SPACEHINTS](./jet-spacehints-structure.md) pour l’index séquentiel par défaut.

**pSeqSpacehints** a été introduit dans Windows 7.

**pLVSpacehints**

Pointeur vers une structure [JET_SPACEHINTS](./jet-spacehints-structure.md) pour une arborescence de valeurs longues séparée.

**pLVSpacehints** a été introduit dans Windows 7.

**cbSeparateLV**

Taille à laquelle séparer un LV intrinsèque de l’enregistrement principal. Toute structure c à valeurs longues pour une arborescence LV séparée. Pour plus d’informations, consultez ng-value in [JET_SPACEHINTS](./jet-spacehints-structure.md). Les colonnes de valeur longue inférieures à cette valeur peuvent être séparées si l’enregistrement devient trop volumineux.

**cbSeparateLV** a été introduit dans Windows 7.

**TableID**

Champ de sortie qui contient le [JET_TABLEID](./jet-tableid.md) de la nouvelle table si l’appel d’API a échoué. Si l’appel d’API échoue, la valeur n’est pas définie. Cette table est ouverte exclusivement.

**Encore**

Champ de sortie qui contient le nombre d’objets qui sont créés si l’appel d’API a échoué. Si l’appel d’API échoue, la valeur n’est pas définie.

Le nombre d’objets créés est égal à la somme des colonnes, des tables et des index qui ont été créés avec succès.

### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté comme <strong>JET_TABLECREATE3_W</strong> (Unicode) et <strong>JET_TABLECREATE3_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetDefragment2](./jetdefragment2-function.md)
