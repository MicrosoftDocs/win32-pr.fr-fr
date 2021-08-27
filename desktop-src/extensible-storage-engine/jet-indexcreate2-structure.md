---
description: 'En savoir plus sur : structure JET_INDEXCREATE2'
title: Structure JET_INDEXCREATE2
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
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
ms.openlocfilehash: 00d5a788113b7427fb96a4f270478c1dd7572d54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473205"
---
# <a name="jet_indexcreate2-structure"></a>Structure JET_INDEXCREATE2


_**S’applique à :** Windows | Windows Serveurs_

la structure **JET_INDEXCREATE2** contient les informations nécessaires à la création d’un index sur des données dans une base de données ESE (Extensible Stockage Engine). La structure est utilisée par des fonctions telles que [JetCreateIndex2](./jetcreateindex2-function.md)et dans des structures telles que [JET_TABLECREATE](./jet-tablecreate-structure.md) et [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

la structure **JET_INDEXCREATE2** a été introduite dans le système d’exploitation Windows 7.

```cpp
typedef struct tagJET_INDEXCREATE2 {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
    unsigned long cbKeyMost;
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a>Membres

**cbStruct**

Taille, en octets, de cette structure. Affectez à ce membre la valeur sizeof (JET_INDEXCREATE2).

**szIndexName**

Nom de l’index à créer.

Le nom doit remplir les conditions suivantes :

  - Elle doit être inférieure à JET_cbNameMost, à l’exclusion de la valeur null de fin.

  - Il doit se composer du jeu de caractères suivant : 0 (zéro) à 9, A à Z, a à z et toutes les autres signes de ponctuation, à l’exception de « \! » (point d’exclamation), « , » (virgule), « \[ » (crochet ouvrant) et « \] » (crochet fermant), c’est-à-dire les caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c et 0x5d à 0x7F.

  - Il ne doit pas commencer par un espace.

  - Il doit contenir au moins un caractère autre qu’un espace.

**szKey**

Pointeur vers une chaîne se terminant par un caractère null et des jetons délimités par un caractère null.

Chaque jeton se présente sous la forme « \<direction-specifier\> \<column-name\> », où direction-Specification est « + » ou « - ». Par exemple, un **szKey** de « + ABC \\ 0-Def \\ 0 + GHI \\ 0 » sera indexé sur les trois colonnes « ABC » (dans l’ordre croissant), « def » (dans l’ordre décroissant) et « GHI » (dans l’ordre croissant). Dans le langage C, les littéraux de chaîne ont un terminateur **null** implicite, de sorte que la chaîne ci-dessus se termine par une valeur double null.

Le nombre de colonnes spécifié dans **szKey** ne doit pas dépasser JET_ccolKeyMost (une constante dépendante de la version).

Au moins une colonne doit être nommée dans **szKey**.

Comportement obsolète : après le terminateur double-NULL, il est possible de spécifier un ID de langue (un mot qui est passé dans MAKELCID (langid, SORT_DEFAULT)) pour spécifier le LCID de l’index. Il n’est pas conforme de spécifier à la fois un ID de langue dans **szKey** et un LCID dans [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (en définissant JET_bitIndexUnicode dans *Grbit*).

Déconseillé : après l’ID de langue, il est possible de passer **cbVarSegMac** comme type de données **UShort** . Le comportement n’est pas défini si le USHORT est défini à la fois dans **szKey** et si **cbVarSegMac** est défini dans la structure.

**cbKey**

Longueur, en octets, de **szKey**, y compris les deux valeurs null de fin.

**grbit**

Groupe de bits qui contiennent zéro, une ou plusieurs des options de valeur répertoriées dans le tableau suivant.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>Les entrées d’index en double (clés) ne sont pas autorisées. Cette méthode est appliquée quand <a href="gg269288(v=exchg.10).md">JetUpdate</a> est appelé, et non lorsque <a href="gg294137(v=exchg.10).md">JetSetColumn</a> est appelé.</p> | 
| <p>JET_bitIndexPrimary</p> | <p>L’index est un index principal (cluster). Chaque table doit avoir un seul index primaire. Si aucun index primaire n’est défini explicitement sur une table, le moteur de base de données crée son propre index primaire.</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>Aucune des colonnes sur lesquelles l’index est créé ne peut contenir une valeur <strong>null</strong> .</p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>N’ajoutez pas d’entrée d’index pour une ligne si toutes les colonnes indexées ont la <strong>valeur null</strong>.</p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>N’ajoutez pas d’entrée d’index pour une ligne si l’une des colonnes indexées a la <strong>valeur null</strong>.</p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>N’ajoutez pas d’entrée d’index pour une ligne si la première colonne indexée a la <strong>valeur null</strong>.</p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>Spécifie que les opérations d’index seront journalisées tardivement.</p><p>JET_bitIndexLazyFlush n’affecte pas le paresse des mises à jour de données. Si l’opération d’indexation est interrompue par un arrêt de processus, la récupération logicielle peut toujours être en mesure d’obtenir la base de données à un état cohérent, mais l’index peut ne pas être présent.</p> | 
| <p>JET_bitIndexEmpty</p> | <p>N’essayez pas de générer l’index, car toutes les entrées ont la <strong>valeur null</strong>. <strong>Grbit</strong> DOIT également spécifier JET_bitIgnoreAnyNull lorsque JET_bitIndexEmpty est passé. Il s’agit d’une amélioration des performances. Par exemple, si une nouvelle colonne est ajoutée à une table, puis qu’un index est créé sur cette colonne nouvellement ajoutée, tous les enregistrements de la table sont analysés même s’ils ne sont pas ajoutés à l’index. La spécification de JET_bitIndexEmpty ignore l’analyse de la table, ce qui peut prendre un certain temps.</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>JET_bitIndexUnversioned entraîne la visibilité de la création d’index pour d’autres transactions. En règle générale, une session dans une transaction ne peut pas voir une opération de création d’index dans une autre session. Cet indicateur peut être utile si une autre transaction est susceptible de créer le même index. Le second index-Create échoue simplement au lieu de provoquer potentiellement des opérations de base de données inutiles. La deuxième transaction peut ne pas être en mesure d’utiliser l’index immédiatement. L’opération de création d’index doit être terminée pour pouvoir être utilisée. La session ne doit pas être actuellement dans une transaction pour créer un index sans informations de version.</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>Si vous spécifiez cet indicateur, les valeurs <strong>null</strong> sont triées après les données de toutes les colonnes de l’index.</p> | 
| <p>JET_bitIndexUnicode</p> | <p>La spécification de cet indicateur affecte l’interprétation du champ LCID/pidxunicde Union dans la structure. La définition du bit signifie que le champ pidxunicode pointe en fait vers une structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> . JET_bitIndexUnicode n’est pas nécessaire pour indexer les données Unicode. Elle n’est nécessaire que pour personnaliser la normalisation des données Unicode.</p> | 
| <p>JET_bitIndexTuples</p> | <p>Spécifie que l’index est un index de Tuple. Pour obtenir une description d’un index de tuple, consultez <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p><p>la valeur JET_bitIndexTuples a été introduite dans le système d’exploitation Windows XP.</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>La spécification de cet indicateur affecte l’interprétation du champ <strong>cbVarSegMac/ptuplelimits</strong> Union dans la structure. Le fait de définir ce bit signifie que le champ <strong>ptuplelimits</strong> pointe vers une structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> pour autoriser les limites d’index de tuple personnalisées (implique JET_bitIndexTuples).</p><p>la valeur <strong>JET_bitIndexTupleLimits</strong> a été introduite dans le système d’exploitation Windows Server 2003.</p> | 
| <p>JET_bitIndexCrossProduct<br />0x00004000</p> | <p>La spécification de cet indicateur pour un index qui a plusieurs colonnes clés qui est une colonne à valeurs multiples entraîne la création d’une entrée d’index pour chaque résultat d’un produit croisé de toutes les valeurs dans ces colonnes clés. Dans le cas contraire, l’index comporterait une seule entrée pour chaque valeur multiple dans la colonne clé la plus significative qui est une colonne à valeurs multiples et chacune de ces entrées d’index utiliserait la première valeur multiple de toutes les autres colonnes clés qui sont des colonnes à valeurs multiples.</p><p>Par exemple, si vous avez spécifié cet indicateur pour un index sur la colonne a qui a les valeurs « Red » et « Blue » et sur la colonne B qui ont les valeurs « 1 » et « 2 », les entrées d’index suivantes sont créées : « Red », « 1 »; « Red », « 2 »; "Blue", "1"; « Blue », « 2 ». Dans le cas contraire, les entrées d’index suivantes sont créées : « Red », « 1 »; « Blue », « 1 ».</p><p>la valeur <strong>JET_bitIndexCrossProduct</strong> a été introduite dans Windows Vista.</p> | 
| <p>JET_bitIndexKeyMost<br />0x00008000</p> | <p>La spécification de cet indicateur entraîne l’utilisation par l’index de la taille de clé maximale spécifiée dans le champ <strong>cbKeyMost</strong> de la structure. Dans le cas contraire, l’index utilise JET_cbKeyMost (255) comme taille de clé maximale.</p><p>la valeur <strong>JET_bitIndexKeyMost</strong> a été introduite dans Windows Vista.</p> | 
| <p>JET_bitIndexDisallowTruncation<br />0x00010000</p> | <p>Si vous spécifiez cet indicateur, toute mise à jour de l’index entraînant l’échec d’une clé tronquée avec le code de réponse JET_errKeyTruncated. Dans le cas contraire, les clés sont tronquées en mode silencieux. Pour plus d’informations sur la troncation des clés, consultez <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</p><p>la valeur <strong>JET_bitIndexDisallowTruncation</strong> a été introduite dans Windows Vista.</p> | 



**ulDensity**

Densité de pourcentage de l’index initial B +. La spécification d’un nombre inférieur à 100 utilise plus d’espace pour créer initialement l’index, mais permet la croissance future de l’index, évitant ainsi la fragmentation interne.

**lcid**

Identificateur de paramètres régionaux (LCID) à utiliser lors de la normalisation des données lorsque la valeur JET_bitIndexUnicode n’est pas spécifiée dans le paramètre *Grbit* . Le LCID affecte la normalisation si l’index se trouve sur des colonnes Unicode.

**pidxunicode**

Pointeur vers une structure [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) si la valeur JET_bitIndexUnicode est spécifiée dans le paramètre *Grbit* . Cela permet à l’utilisateur de spécifier des indicateurs personnalisés qui sont passés à la fonction [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) pendant la normalisation Unicode.

**cbVarSegMac**

Longueur maximale, en octets, de chaque colonne à stocker dans l’index lorsque la valeur de JET_bitIndexTupleLimits n’est pas spécifiée dans le paramètre *Grbit* .

La spécification de la valeur 0 (zéro) pour ce champ équivaut à ce qui suit :

  - Spécification de JET_cbPrimaryKeyMost pour un index primaire.

  - Spécification de JET_cbSecondaryKeyMost pour un index secondaire.

**ptuplelimits**

Pointeur vers une structure [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) si la valeur JET_bitIndexTupleLimits est spécifiée dans le paramètre *Grbit* .

**ptuplelimits** a été introduite dans Windows Server 2003.

**rgconditionalcolumn**

Paramètre facultatif d’un tableau de structures de [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , qui sont utilisées pour spécifier les colonnes conditionnelles dans l’index.

**cConditionalColumn**

Nombre de structures dans le tableau **rgconditionalcolumn** .

**Raise**

Contient le code de retour pour la création de cet index.

**cbKeyMost**

Spécifie la taille maximale autorisée, en octets, pour les clés dans l’index. Ce paramètre est ignoré si JET_bitIndexKeyMost n’est pas spécifié dans le paramètre *Grbit* . Si ce paramètre a la valeur zéro et que JET_bitIndexKeyMost est spécifié dans le membre *Grbit* , la fonction appelante échoue avec JET_err_InvalidDef.

La taille de clé maximale prise en charge minimale est JET_cbKeyMostMin (255), qui est la taille de clé maximale héritée.

La taille de clé maximale dépend de la taille de page de la base de données (JET_paramDatabasePageSize) comme suit :

  - Si JET_paramDatabasePageSize = 2048, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500)

  - Si JET_paramDatabasePageSize = 4096, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000)

  - Si JET_paramDatabasePageSize = 8192, JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000)

La taille maximale de clé maximale prise en charge pour l’instance peut également être lue à partir du paramètre système JET_paramKeyMost.

**cbKeyMost** a été introduit dans Windows Vista.

**pSpacehints**

Pointeur vers une structure [JET_SPACEHINTS](./jet-spacehints-structure.md) .

**pSpacehints** a été introduite dans Windows 7.

### <a name="remarks"></a>Remarques

Le moteur ESE prend en charge l’indexation sur des colonnes clés contenant plusieurs valeurs. Pour utiliser cette fonctionnalité, la colonne doit être un type de colonne avec balises (JET_bitColumnTagged), et elle doit être marquée pour que ses multiples valeurs soient indexées avec JET_bitColumnMultiValued. dans les versions de Windows antérieures à Windows Vista, seule la première colonne clé à valeurs multiples de l’index aura ses valeurs développées dans l’index. Toutes les autres colonnes à valeurs multiples et balises auront uniquement leurs premières valeurs développées dans l’index.

En supposant que les lignes suivantes existent dans une table (la colonne alpha n’est pas à valeurs multiples, tandis que les colonnes Beta, gamma et Delta sont à valeurs multiples) et qu’un index est créé en tant que « + alpha \\ 0 + bêta \\ 0 + gamma \\ 0 + Delta \\ 0 \\ 0 » :


| <p>Alpha</p> | <p>Bêta</p> | <p>Gamma</p> | <p>Delta</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />PQR<br />STU</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>LA</p> | <p>PLUIE<br />ESPAGNE</p> | <p>IN<br />FAIT</p> | 



Les tuples d’index suivants seront stockés :

{1, ABC, MNO, VWX}  
{1, GHI, MNO, VWX}  
{1, JKL, MNO, VWX}  
{2, THE, PLUIE, IN}

Notez que {2, l’Espagne, IN} n’est pas stocké, même si la colonne alpha de la deuxième ligne contient une seule valeur multivaleur.

dans les versions de Windows à partir de Windows Vista, toutes les colonnes à valeurs multiples peuvent être développées dans l’index en spécifiant JET_bitIndexCrossProduct.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_ INDEXCREATE2_W</strong> (Unicode) et <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
