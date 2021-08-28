---
description: 'En savoir plus sur : structure JET_TABLECREATE'
title: Structure JET_TABLECREATE
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
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
ms.openlocfilehash: fcc6c63b06614eb16379fbb18d59a5459a8e5085
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983032"
---
# <a name="jet_tablecreate-structure"></a>Structure JET_TABLECREATE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_tablecreate-structure"></a>Structure JET_TABLECREATE

La structure **JET_TABLECREATE** contient les informations nécessaires à la création d’une table remplie avec des colonnes et des index dans une base de données ESE. La structure **JET_TABLECREATE** est utilisée par [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de cette structure en octets (pour une extension future). Elle doit être définie sur sizeof (JET_TABLECREATE) en octets.

**szTableName**

Nom de la table à créer.

Le nom doit être utilisé pour remplir les conditions suivantes :

  - A une valeur inférieure à JET_cbNameMost, à l’exclusion de la valeur NULL de fin.

<!-- end list -->

  - Se compose du jeu de caractères suivant : de 0 à 9, de A à Z, de a à z et de toute autre ponctuation, à l’exception du point d’exclamation ( \! ), de la virgule (,), du crochet ouvrant ( \[ ) et du crochet fermant ( \] ), c’est-À-dire des caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c et 0x5d à 0x7F.

<!-- end list -->

  - Ne commence pas par un espace.

<!-- end list -->

  - Se compose d’au moins un caractère autre qu’un espace.

**szTemplateTableName**

Nom d’une table déjà existante à partir de laquelle hériter le DDL de base (langage de définition de données). L’utilisation d’une table de modèle permet de créer facilement de nombreuses tables avec des colonnes et des index identiques.

**ulPages**

Nombre initial de pages de base de données à allouer pour la table. La spécification d’un nombre supérieur à un peut réduire la fragmentation si de nombreuses lignes sont insérées dans cette table.

**ulDensity**

Densité de la table, en points de pourcentage. Le nombre doit être égal à 0 ou compris entre 20 et 100. Le passage de 0 signifie que la valeur par défaut doit être utilisée. La valeur par défaut est 80.

**rgcolumncreate**

Tableau de structures de [JET_COLUMNCREATE](./jet-columncreate-structure.md) , chacune d’elles correspondant à une colonne à créer dans la nouvelle table.

**cColumns**

Nombre d’éléments [JET_COLUMNCREATE](./jet-columncreate-structure.md) dans **rgcolumncreate**.

**rgindexcreate**

Tableau de structures de [JET_INDEXCREATE](./jet-indexcreate-structure.md) , chacune d’elles correspondant à un index à créer dans la nouvelle table.

**cIndexes**

Nombre d’éléments [JET_INDEXCREATE](./jet-indexcreate-structure.md) dans **rgindexcreate**.

**grbit**

Groupe de bits qui contiennent les options pour cet appel, qui incluent zéro, une ou plusieurs des valeurs suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>La définition de JET_bitTableCreateFixedDDL empêche les opérations DDL sur la table (telles que l’ajout ou la suppression de colonnes).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>La définition de JET_bitTableCreateTemplateTable fait que la table est une table de modèle. Les nouvelles tables peuvent ensuite spécifier le nom de cette table comme table de modèle. La définition de JET_bitTableCreateTemplateTable implique JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Obsolète. Ne pas utiliser.</p> | 



**TableID**

Champ de sortie qui contient le [JET_TABLEID](./jet-tableid.md) de la nouvelle table si l’appel d’API a échoué. Si l’appel d’API échoue, la valeur n’est pas définie.

**Encore**

Champ de sortie qui contient le nombre d’objets créés si l’appel d’API a échoué. Si l’appel d’API échoue, la valeur n’est pas définie.

Le nombre d’objets créés est égal à la somme des colonnes, des tables et des index qui ont été créés avec succès.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_TABLECREATE_W</strong> (Unicode) et <strong>JET_TABLECREATE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Voir aussi

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
