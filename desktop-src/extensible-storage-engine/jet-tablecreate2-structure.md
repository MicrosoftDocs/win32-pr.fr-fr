---
description: 'En savoir plus sur : structure JET_TABLECREATE2'
title: Structure JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: 95e4d60ba80317624004fa7c9335005aa16a9300
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476465"
---
# <a name="jet_tablecreate2-structure"></a>Structure JET_TABLECREATE2


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_tablecreate2-structure"></a>Structure JET_TABLECREATE2

La structure **JET_TABLECREATE2** contient les informations nécessaires pour créer une table remplie avec des colonnes et des index dans une base de données ESE, et qui désigne une fonction de rappel. La structure **JET_TABLECREATE2** est utilisée par [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).

**Windows XP :** la structure **JET_TABLECREATE2** est introduite dans Windows XP.

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de cette structure en octets (pour une extension future). Elle doit être définie sur sizeof (JET_TABLECREATE2) en octets.

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

nombre d’éléments [JET_COLUMNCREATE](./jet-columncreate-structure.md) dans **rgcolumncreate**.

**rgindexcreate**

Tableau de structures de [JET_INDEXCREATE](./jet-indexcreate-structure.md) , chacune d’elles correspondant à un index à créer dans la nouvelle table.

**cIndexes**

Nombre d’éléments [JET_INDEXCREATE](./jet-indexcreate-structure.md) dans **rgindexcreate**.

**szCallback**

Fonction qui est appelée pendant certains événements. **cbtyp** détermine le moment où la fonction de rappel sera appelée.

Le format de **szCallback** doit être « fonction de module \! », par exemple, « alpha \! bêta » fait référence à la fonction bêta dans le module nommé « alpha ». Le prototype de la fonction doit correspondre à [JET_CALLBACK](./jet-callback-callback-function.md). Pour plus d’informations, consultez [JET_CALLBACK](./jet-callback-callback-function.md).

**cbtyp**

Décrit le type de fonction de rappel désigné par **szCallback**. Pour plus d’informations, consultez [JET_CBTYP](./jet-cbtyp.md). Ce champ de bits est composé d’un ou plusieurs des bits suivants.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_cbtypFinalize</p> | <p>La fonction de rappel est appelée lorsqu’une colonne qui peut être finalisée est passée à zéro.</p> | 
| <p>JET_cbtypBeforeInsert</p> | <p>La fonction de rappel sera appelée avant l’insertion de l’enregistrement.</p> | 
| <p>JET_cbtypAfterInsert</p> | <p>La fonction de rappel est appelée une fois que le moteur de base de données a terminé l’insertion d’un enregistrement.</p> | 
| <p>JET_cbtypBeforeReplace</p> | <p>La fonction de rappel sera appelée avant la modification d’un enregistrement.</p> | 
| <p>JET_cbtypAfterReplace</p> | <p>La fonction de rappel sera appelée à la fin de la modification d’un enregistrement.</p> | 
| <p>JET_cbtypBeforeDelete</p> | <p>La fonction de rappel sera appelée avant la suppression d’un enregistrement.</p> | 
| <p>JET_cbtypAfterDelete</p> | <p>La fonction de rappel est appelée après la suppression d’un enregistrement.</p> | 
| <p>JET_cbtypUserDefinedDefaultValue</p> | <p>La fonction de rappel sera appelée pour calculer une valeur par défaut définie par l’utilisateur.</p> | 
| <p>JET_cbtypOnlineDefragCompleted</p> | <p>La fonction de rappel est appelée après l’exécution d’un appel à <a href="gg294095(v=exchg.10).md">JetDefragment2</a> .</p> | 
| <p>JET_cbtypFreeCursorLS</p> | <p>La fonction de rappel sera appelée lorsque le stockage local qui est associé à un curseur doit être libéré.</p> | 
| <p>JET_cbtypFreeTableLS</p> | <p>La fonction de rappel sera appelée lorsque le stockage local qui est associé à une table doit être libéré.</p> | 



**grbit**

Groupe de bits qui contiennent les options pour cet appel, qui incluent zéro, une ou plusieurs des valeurs suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitTableCreateFixedDDL</p> | <p>La définition de JET_bitTableCreateFixedDDL empêche les opérations DDL sur la table (telles que l’ajout ou la suppression de colonnes).</p> | 
| <p>JET_bitTableCreateTemplateTable</p> | <p>La définition de JET_bitTableCreateTemplateTable fait que la table est une table de modèle. Les nouvelles tables peuvent ensuite spécifier le nom de cette table comme table de modèle. La définition de JET_bitTableCreateTemplateTable implique JET_bitTableCreateFixedDDL.</p> | 
| <p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p> | <p>Doit être utilisé conjointement avec JET_bitTableCreateTemplateTable. Obsolète. Ne pas utiliser.</p> | 



**TableID**

Champ de sortie qui contient le [JET_TABLEID](./jet-tableid.md) de la nouvelle table si l’appel d’API a échoué. Si l’appel d’API échoue, la valeur n’est pas définie.

**Encore**

Champ de sortie qui contient le nombre d’objets qui sont créés si l’appel d’API a échoué. Si l’appel d’API échoue, la valeur n’est pas définie.

Le nombre d’objets créés est égal à la somme des colonnes, des tables et des index qui ont été créés avec succès.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_TABLECREATE2_W</strong> (Unicode) et <strong>JET_TABLECREATE2_A</strong> (ANSI).</p> | 



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
