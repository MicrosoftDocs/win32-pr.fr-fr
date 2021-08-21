---
description: 'En savoir plus sur : fonction JetCreateIndex3'
title: Fonction JetCreateIndex3
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb8e2eec2fe0b60245884b654f99353480833f27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465416"
---
# <a name="jetcreateindex3-function"></a>Fonction JetCreateIndex3


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetcreateindex3-function"></a>Fonction JetCreateIndex3

La fonction **JetCreateIndex3** crée des index sur les données d’une base de données ESE, qui peut être utilisée pour localiser rapidement des données spécifiques.

**Windows 7 : JetCreateIndex3** est introduit dans le système d’exploitation Windows 7.

```cpp
    JET_ERR JET_API JetCreateIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE2* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table sur laquelle l’index sera créé.

*pindexcreate*

Tableau de structures [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , qui définissent chacune un index à créer.

*cIndexCreate*

Nombre d’éléments dans le tableau *pindexcreate* .

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errCannotIndex</p> | <p>Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Une tentative d’indexation sur une colonne inexistante a été effectuée. Toute tentative d’indexation conditionnelle sur une colonne inexistante peut également générer cette erreur.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Une tentative de définition de deux index identiques a été effectuée.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table. Une table doit avoir un seul index primaire. Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Une définition d’index non valide a été spécifiée. Voici quelques raisons possibles pour la réception de cette erreur :</p><ul><li><p>Un index principal est conditionnel (le membre<strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexPrimary défini et le membre <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieur à zéro).</p></li><li><p>Windows Le serveur 2003 et les versions ultérieures de Windows. Tentative de création d’un index de tuple avec des limites de tuple, mais sans passer d’informations dans le membre <strong>ptuplelimits</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (autrement dit, <em>Grbit</em> a JET_bitIndexTupleLimits défini, mais le pointeur <strong>ptuplelimits</strong> est null).</p></li><li><p>Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Pour plus d’informations sur les définitions valides, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></li><li><p>La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieure à JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à JET_cbSecondaryKeyMost (pour un index secondaire).</p></li><li><p>Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Certaines causes courantes peuvent être que le champ pidxunicode de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur null ou que le LCID spécifié dans la structure pidxunicode n’est pas valide.</p></li><li><p>Spécification d’une colonne à valeurs multiples pour un index primaire.</p></li><li><p>Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles. Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas être supérieur à JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP et versions ultérieures de Windows. Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge. Consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple ne peut pas être unique (<em>Grbit</em> ne doit pas avoir à la fois JET_bitIndexTuples et JET_bitIndexUnique défini).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple ne peut être que sur une seule colonne (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a JET_bitIndexTuples jeu et le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> spécifie plusieurs colonnes).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple ne peut être que sur une colonne de type texte ou Unicode. Si vous tentez d’indexer d’autres colonnes (par exemple, des colonnes binaires), JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP et versions ultérieures de Windows. Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p> | 
| <p>JET_errInTransaction</p> | <p>Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contient des valeurs incohérentes. Voici quelques raisons possibles :</p><ul><li><p>Un index principal avait un bit ignore spécifié (JET_bitIndexPrimary a été passé avec l’un des JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li><li><p>Un index vide n’ignore aucun champ NULL (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a JET_bitIndexEmpty défini, mais n’a pas de JET_bitIndexIgnoreAnyNull défini).</p></li><li><p>Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide. Consultez <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>Lors de la création de plusieurs index à la fois (autrement dit, si le paramètre <em>cIndexCreate</em> est supérieur à un), aucun des index ne peut contenir l’un des bits suivants :</p><ul><li><p>JET_bitIndexPrimary</p></li><li><p>JET_bitIndexUnversioned</p></li><li><p>JET_bitIndexEmpty</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Un ID de paramètres régionaux (LCID) non valide a été passé (par le biais du membre <strong>LCID</strong> dans la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que le membre <strong>pidxunicode</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contient un pointeur vers ou via le membre <strong>LCID</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p> | 
| <p>JET_errInvalidName</p> | <p>Un nom d’index non valide a été spécifié. Pour plus d’informations, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un paramètre non valide a été passé dans l’API. Voici quelques raisons pour lesquelles cette erreur peut être retournée :</p><ul><li><p>Le champ <strong>cbKey</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur zéro.</p></li><li><p>Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas la valeur sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Une erreur s’est produite lors de la normalisation d’une colonne Unicode. Cela peut être dû à un manque de ressources système.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Un élément de la structure d’indicateurs d’espace JET n’est pas correct ou n’est pas exploitable.</p> | 



#### <a name="remarks"></a>Remarques

La valeur de retour est JET_errSuccess en cas d’achèvement réussi de tous les index spécifiés.

**JetCreateIndex3** itère au sein des index donnés dans **pindexcreate**, et s’abandonne parfois lors du premier échec. Les index qui suivent le premier index avec une erreur n’ont peut-être pas été tentés, même si le membre **Err** de la structure [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contient des JET_errSuccess.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetCreateIndex3W</strong> (Unicode) et <strong>JetCreateIndex3A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
