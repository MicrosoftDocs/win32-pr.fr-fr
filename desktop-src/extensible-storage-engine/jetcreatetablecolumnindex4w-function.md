---
description: 'En savoir plus sur : fonction JetCreateTableColumnIndex4W'
title: JetCreateTableColumnIndex4W fonction)
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab3561ba51f2086f6af186ff5954e512d41e78f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985002"
---
# <a name="jetcreatetablecolumnindex4w-function"></a>JetCreateTableColumnIndex4W fonction)


_**S’applique à :** Windows | Windows Serveurs_

la fonction **JetCreateTableColumnIndex4W** crée une table dans un moteur ese (Extensible Stockage Engine) (base de données avec un ensemble initial d’index et un ensemble initial de colonnes à partir d’un tableau de structures [JET_TABLECREATE3](./jet-tablecreate3-structure.md) . La structure [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permet de spécifier une fonction de rappel.

la fonction **JetCreateTableColumnIndex4W** a été introduite dans le système d’exploitation Windows 8.

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*dbid*

Identificateur de base de données à utiliser pour l’appel d’API.

*ptablecreate*

Pointeur vers une structure [JET_TABLECREATE3](./jet-tablecreate3-structure.md) qui définit la table à créer. Pour plus d’informations, consultez [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .

### <a name="return-value"></a>Valeur retournée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. pour plus d’informations sur les erreurs ese (extensible Stockage Enginge) possibles, consultez [erreurs du moteur de Stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>La fonction de rappel n’a pas pu être résolue. La DLL n’a peut-être pas été trouvée, ou la fonction dans la DLL n’a peut-être pas été trouvée. Une fois la journalisation suffisante activée, le journal des événements fournit plus de détails.</p> | 
| <p>JET_errCannotIndex</p> | <p>Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Retournée si le paramètre <em>ptablecreate- &gt; Grbit</em> spécifie la valeur JET_bitTableCreateTemplateTable, mais que le paramètre <em>ptablecreate- &gt; szTemplateTableName</em> est défini sur null.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Une colonne existe déjà.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Une tentative d’indexation sur une colonne inexistante a été effectuée. Une tentative d’index conditionnel sur une colonne inexistante peut également générer cette erreur.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Une tentative d’ajout d’une colonne redondante a été effectuée. Il ne doit exister qu’une seule colonne AutoIncrement, et une seule colonne de version doit exister par table.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Signifie que la table nommée dans le membre <strong>szTemplateTableName</strong> de la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> n’a pas été marquée comme table de modèle (autrement dit, cette table n’a pas la valeur de paramètre JET_bitTableCreateTemplateTable définie).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Une tentative de définition de deux index identiques a été effectuée.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table. Une table doit avoir un seul index primaire. Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Une définition d’index non valide a été spécifiée. Voici quelques-unes des raisons possibles de cette erreur :</p><ul><li><p>Un index principal est conditionnel (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur JET_bitIndexPrimary définie et le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieur à zéro).</p></li><li><p>s’applique aux versions du système d’exploitation Windows server à partir de Windows server 2003. Une tentative de création d’un index de tuple avec des limites de tuple, mais sans passer le membre <strong>ptuplelimits</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (autrement dit, le membre <strong>Grbit</strong> de la structure <strong>JET_INDEXCREATE2</strong> a JET_bitIndexTupleLimits valeur définie, mais le pointeur <strong>ptuplelimits</strong> est null).</p></li><li><p>Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Pour plus d’informations sur les définitions valides, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li><li><p>La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieure à la valeur JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à la valeur JET_cbSecondaryKeyMost (pour un index secondaire).</p></li><li><p>Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit de valeur JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ). Certaines causes courantes incluent le membre <strong>pidxunicode</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur null, ou le LCID spécifié dans la structure <strong>pidxunicode</strong> n’est pas valide.</p></li><li><p>Spécification d’une colonne à valeurs multiples pour un index primaire.</p></li><li><p>Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles. Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas être supérieur à <strong>JET_ccolKeyMost</strong>.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>s’applique aux versions de Windows à partir de Windows XP. Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge. Pour plus d’informations, consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>s’applique aux versions de Windows à partir de Windows XP. Un index de tuple ne peut pas être unique (autrement dit, le membre <em>Grbit</em> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir les valeurs JET_bitIndexPrimary et JET_bitIndexUnique définies).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>s’applique aux versions de Windows à partir de Windows XP. Un index de tuple ne peut être que sur une seule colonne (autrement dit, si le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexTuples valeur définie et que le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> spécifie plusieurs colonnes).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>s’applique aux versions de Windows à partir de Windows XP. Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>s’applique aux versions de Windows à partir de Windows XP. Un index de tuple ne peut être que sur une colonne de type texte ou Unicode. Si vous tentez d’indexer d’autres colonnes (telles que des colonnes binaires), vous obtiendrez un code de réponse JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>s’applique aux versions de Windows à partir de Windows XP. Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p> | 
| <p>JET_errInTransaction</p> | <p>Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Le membre <strong>CP</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur une page de codes valide. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Le membre <strong>coltyp</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur un type de colonne valide.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Voici les raisons pour lesquelles cette erreur peut se produire :</p><ul><li><p>Le membre <strong>rgindexcreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</p></li><li><p>Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</p></li><li><p>Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas été défini sur une valeur valide.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Une combinaison de membres <strong>Grbit</strong> non valide a été spécifiée dans la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> .</p><p>La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> contient des valeurs incohérentes. Voici quelques raisons possibles :</p><ul><li><p>Un index primaire a un bit ignore spécifié (autrement dit, JET_bitIndexPrimary valeur a été passée avec les valeurs JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un index vide n’ignore aucun membre null (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur JET_bitIndexEmpty définie, mais aucune valeur JET_bitIndexIgnoreAnyNull n’est définie).</p></li><li><p>Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Un ID de paramètres régionaux (LCID) non valide a été passé (par le biais du membre <strong>LCID</strong> de la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> dans laquelle le membre <strong>pidxunicode</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> pointe, ou via le champ <strong>LCID</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un paramètre non valide a été spécifié. Voici quelques raisons possibles :</p><ul><li><p>Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> a la valeur null.</p></li><li><p>Le membre <strong>cbStruct</strong> de l’une des structures <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> données dans le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> n’a pas la valeur sizeof (JET_COLUMNCREATE).</p></li><li><p>Le membre <strong>cbKey</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur zéro.</p></li><li><p>Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas la valeur sizeof (JET_INDEXCREATE2).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>L’enregistrement est trop volumineux. La somme du membre <strong>cbMax</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> pour toutes les colonnes fixes ne doit pas dépasser une certaine valeur.</p> | 
| <p>JET_errTableDuplicate</p> | <p>La table existe déjà.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée. Une table ne peut pas comporter plus de <strong>JET_ccolFixedMost</strong> colonnes fixes, ni plus de <strong>JET_ccolVarMost</strong> colonnes de longueur variable, ni plus de <strong>JET_ccolTaggedMost</strong> colonnes avec balises.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Une erreur s’est produite lors d’une tentative de normalisation d’une colonne Unicode. Cela peut être dû à un manque de ressources système.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Un élément de la structure d’indicateurs d’espace JET n’est pas correct ou n’est pas exploitable.</p> | 



#### <a name="remarks"></a>Remarques

La fonction **JetCreateTableColumnIndex4W** crée une table avec un ensemble initial de colonnes et d’index. Des colonnes et des index supplémentaires peuvent être ajoutés et supprimés dynamiquement au moyen des fonctions [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)et [JetDeleteIndex](./jetdeleteindex-function.md) .

Comme avec la fonction [JetOpenTable](./jetopentable-function.md) , lorsque l’application est effectuée à l’aide de l' *TableID* retourné, la fonction [JetCloseTable](./jetclosetable-function.md) doit fermer l’application.

#### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Requiert Windows 8.</p> | 
| <p><strong>Serveur</strong></p> | <p>Requiert Windows Server 2012.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateIndex3](./jetcreateindex3-function.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
