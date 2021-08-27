---
description: 'En savoir plus sur : fonction JetCreateTableColumnIndex3'
title: JetCreateTableColumnIndex3 fonction)
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa165ddc7655ec195f276b96e0e841d52e01e9de
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466636"
---
# <a name="jetcreatetablecolumnindex3-function"></a>JetCreateTableColumnIndex3 fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetcreatetablecolumnindex3-function"></a>JetCreateTableColumnIndex3 fonction)

La fonction **JetCreateTableColumnIndex3** crée une table dans une base de données ESE avec un ensemble initial d’index et un ensemble initial de colonnes à partir d’un tableau de structures [JET_TABLECREATE3](./jet-tablecreate3-structure.md) . La structure [JET_TABLECREATE3](./jet-tablecreate3-structure.md) permet de spécifier une fonction de rappel.

**Windows 7 :** **JetCreateTableColumnIndex3** est introduit dans le système d’exploitation Windows 7.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
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

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>La fonction de rappel n’a pas pu être résolue. La DLL n’a peut-être pas été trouvée, ou la fonction dans la DLL n’a peut-être pas été trouvée. Une fois la journalisation suffisante activée, le journal des événements fournit plus de détails.</p> | 
| <p>JET_errCannotIndex</p> | <p>Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Si ptablecreate- &gt; Grbit spécifie JET_bitTableCreateTemplateTable, mais ptablecreate- &gt; szTemplateTableName a la valeur null.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Une colonne existe déjà.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Une tentative d’indexation sur une colonne inexistante a été effectuée. Toute tentative d’indexation conditionnelle sur une colonne inexistante peut également générer cette erreur.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Une tentative d’ajout d’une colonne redondante a été effectuée. Il ne doit y avoir qu’une seule colonne AutoIncrement et pas plus d’une colonne version par table.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Signifie que la table nommée dans le membre <strong>szTemplateTableName</strong> de la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> n’a pas été marquée comme table de modèle (autrement dit, cette table n’avait pas de JET_bitTableCreateTemplateTable définie).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Une tentative de définition de deux index identiques a été effectuée.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table. Une table doit avoir un seul index primaire. Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Une définition d’index non valide a été spécifiée. Voici quelques-unes des raisons possibles de la réception de cette erreur :</p><ul><li><p>Un index principal est conditionnel (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexPrimary jeu et le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieur à zéro).</p></li><li><p>Windows Le serveur 2003 et les versions ultérieures de Windows. La tentative de création d’un index de tuple avec des limites de tuple, mais sans passer le membre <strong>ptuplelimits</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (autrement dit, le membre <strong>Grbit</strong> de la structure JET_INDEXCREATE2 a JET_bitIndexTupleLimits défini, mais le pointeur <strong>ptuplelimits</strong> a la valeur null).</p></li><li><p>Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Pour plus d’informations sur les définitions valides, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></li><li><p>La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieure à JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à JET_cbSecondaryKeyMost (pour un index secondaire).</p></li><li><p>Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Certaines causes courantes incluent le membre <strong>pidxunicode</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur null, ou le LCID spécifié dans la structure <strong>pidxunicode</strong> n’est pas valide.</p></li><li><p>Spécification d’une colonne à valeurs multiples pour un index primaire.</p></li><li><p>Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles. Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas être supérieur à JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP et versions ultérieures de Windows. Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge. Consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple ne peut pas être unique (autrement dit, le membre <em>Grbit</em> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexUnique défini).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple ne peut être que sur une seule colonne (autrement dit, si le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexTuples jeu et que le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> spécifie plusieurs colonnes).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple ne peut être que sur une colonne de type texte ou Unicode. Toute tentative d’index d’autres colonnes (telles que des colonnes binaires) entraîne JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p> | 
| <p>JET_errInTransaction</p> | <p>Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Le membre <strong>CP</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur une page de codes valide. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Le membre <strong>coltyp</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur un type de colonne valide.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Voici les raisons pour lesquelles cette erreur peut se produire :</p><ul><li><p>Le membre <strong>rgindexcreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</p></li><li><p>Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</p></li><li><p>Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas été défini sur une valeur valide.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>Une combinaison de membres <strong>Grbit</strong> non valide a été spécifiée dans <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>.</p><p>La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> contient des valeurs incohérentes. Voici quelques raisons possibles :</p><ul><li><p>Un index primaire a un bit ignore spécifié (autrement dit, JET_bitIndexPrimary a été passé avec JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un index vide n’ignore pas les membres NULL (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a JET_bitIndexEmpty défini, mais n’a pas de JET_bitIndexIgnoreAnyNull défini).</p></li><li><p>Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Un ID de paramètres régionaux (LCID) non valide a été transmis (par le biais du membre <strong>LCID</strong> de la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> qui est référencée par le membre <strong>pidxunicode</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ou par le champ <strong>LCID</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un paramètre non valide a été spécifié. Voici quelques raisons possibles :</p><ul><li><p>Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> a la valeur null.</p></li><li><p>Le membre <strong>cbStruct</strong> de l’une des structures <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> données dans le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> n’a pas la valeur sizeof (JET_COLUMNCREATE).</p></li><li><p>Le membre <strong>cbKey</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur zéro.</p></li><li><p>Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas la valeur sizeof (JET_INDEXCREATE2).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>L’enregistrement est trop volumineux. La somme du membre <strong>cbMax</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> pour toutes les colonnes fixes ne doit pas dépasser une certaine valeur.</p> | 
| <p>JET_errTableDuplicate</p> | <p>La table existe déjà.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée. Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Une erreur s’est produite lors de la normalisation d’une colonne Unicode. Cela peut être dû à un manque de ressources système.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Un élément de la structure d’indicateurs d’espace JET n’est pas correct ou n’est pas exploitable.</p> | 



#### <a name="remarks"></a>Remarques

Le nom **JetCreateTableColumnIndex3** provient de l’ordre de création des objets : il crée d’abord une table, des colonnes, puis enfin des index. **JetCreateTableColumnIndex3** crée une table avec un ensemble initial de colonnes et d’index. Des colonnes et des index supplémentaires peuvent être ajoutés et supprimés dynamiquement avec [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md)et [JetDeleteIndex](./jetdeleteindex-function.md).

Comme [JetOpenTable](./jetopentable-function.md), lorsque l’application est effectuée à l’aide de l' *TableID* retourné, elle doit généralement être fermée avec [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetCreateTableColumnIndex3W</strong> (Unicode) et <strong>JetCreateTableColumnIndex3A</strong> (ANSI).</p> | 



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
