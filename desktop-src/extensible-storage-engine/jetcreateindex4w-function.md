---
description: 'En savoir plus sur : fonction JetCreateIndex4W'
title: Fonction JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520059"
---
# <a name="jetcreateindex4w-function"></a>Fonction JetCreateIndex4W


_**S’applique à :** Windows | Serveur Windows_

La fonction **JetCreateIndex4W** crée des index sur des données dans une base de données ESE (Extensible Storage Engine), qui peut être utilisée pour localiser rapidement des données spécifiques.

La fonction **JetCreateIndex4W** a été introduite dans le système d’exploitation Windows 8.

``` c++
JET_ERR JET_API JetCreateIndex4W(
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

### <a name="return-value"></a>Valeur retournée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Code de retour</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotIndex</p></td>
<td><p>Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Une tentative d’indexation sur une colonne inexistante a été effectuée. Une tentative d’index conditionnel sur une colonne inexistante peut également générer cette erreur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Une tentative de définition de deux index identiques a été effectuée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table. Une table doit avoir un seul index primaire. Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Une définition d’index non valide a été spécifiée. Voici quelques raisons possibles pour cette erreur :</p>
<ul>
<li><p>Un index principal est conditionnel (le membre<strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a <strong>JET_bitIndexPrimary</strong> défini et le membre <strong>cConditionalColumn</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieur à zéro).</p></li>
<li><p>S’applique aux versions de Windows à partir de Windows Server 2003. Une tentative de création d’un index de tuple avec des limites de tuple a été effectuée, mais sans passer d’informations dans le membre <strong>ptuplelimits</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (autrement dit, <em>Grbit</em> a <strong>JET_bitIndexTupleLimits</strong> défini, mais le pointeur <strong>ptuplelimits</strong> est null).</p></li>
<li><p>Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Pour plus d’informations sur les définitions valides, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li>
<li><p>La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> est supérieure à <strong>JET_cbPrimaryKeyMost</strong> (pour un index principal) ou supérieure à <strong>JET_cbSecondaryKeyMost</strong> (pour un index secondaire).</p></li>
<li><p>Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit <strong>JET_bitIndexUnicode</strong> défini dans le membre <strong>Grbit</strong> de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Certaines causes courantes peuvent être que le champ pidxunicode de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur null ou que le LCID spécifié dans la structure pidxunicode n’est pas valide.</p></li>
<li><p>Spécification d’une colonne à valeurs multiples pour un index primaire.</p></li>
<li><p>Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles. Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas être supérieur à <strong>JET_ccolKeyMost</strong>.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>S’applique aux versions de Windows à partir de Windows XP. Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge. Pour plus d’informations, consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>S’applique aux versions de Windows à partir de Windows XP. Un index de tuple ne peut pas être unique (<em>Grbit</em> ne doit pas avoir à la fois <strong>JET_bitIndexTuples</strong> et <strong>JET_bitIndexUnique</strong> défini).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>S’applique aux versions de Windows à partir de Windows XP. Un index de tuple ne peut être que sur une seule colonne (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a <strong>JET_bitIndexTuples</strong> jeu et le membre <strong>szKey</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> spécifie plusieurs colonnes).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>S’applique aux versions de Windows à partir de Windows XP. Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ne doit pas avoir <strong>JET_bitIndexPrimary</strong> et <strong>JET_bitIndexTuples</strong> défini).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>S’applique aux versions de Windows à partir de Windows XP. Un index de tuple ne peut être que sur une colonne de type texte ou Unicode. Si vous tentez d’indexer d’autres colonnes (par exemple, des colonnes binaires), <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>S’applique aux versions de Windows à partir de Windows XP. Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contient des valeurs incohérentes. Voici quelques raisons possibles :</p>
<ul>
<li><p>Un index principal avait un bit ignore spécifié (JET_bitIndexPrimary a été passé avec l’un des <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>ou <strong>JET_bitIndexIgnoreFirstNull</strong>).</p></li>
<li><p>Un index vide n’ignore aucun champ null (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a <strong>JET_bitIndexEmpty</strong> défini, mais n’a pas de <strong>JET_bitIndexIgnoreAnyNull</strong> défini).</p></li>
<li><p>Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide. Consultez <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li>
</ul>
<p>Lors de la création de plusieurs index à la fois (autrement dit, si le paramètre <em>cIndexCreate</em> est supérieur à un), aucun des index ne peut contenir l’un des bits suivants :</p>
<ul>
<li><p><strong>JET_bitIndexPrimary</strong></p></li>
<li><p><strong>JET_bitIndexUnversioned</strong></p></li>
<li><p><strong>JET_bitIndexEmpty</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Un ID de paramètres régionaux (LCID) non valide a été passé (par le biais du membre <strong>LCID</strong> dans la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , que le membre <strong>pidxunicode</strong> dans la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> contient un pointeur vers ou via le membre <strong>LCID</strong> de la structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Un nom d’index non valide a été spécifié. Pour plus d’informations, consultez <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un paramètre non valide a été passé dans l’API. Voici quelques raisons pour lesquelles cette erreur peut être retournée :</p>
<ul>
<li><p>Le champ <strong>cbKey</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> a la valeur zéro.</p></li>
<li><p>Le membre <strong>cbStruct</strong> d’une structure <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> n’a pas la valeur sizeof (JET_INDEXCREATE2).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Une erreur s’est produite lors de la normalisation d’une colonne Unicode. Cela peut être dû à un manque de ressources système.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSpaceHintsInvalid</p></td>
<td><p>Un élément de la structure d’indicateurs d’espace JET n’est pas correct ou n’est pas exploitable.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

La fonction **JetCreateIndex4W** itère au sein des index fournis dans le paramètre *pindexcreate* et s’arrête parfois lors du premier échec. Les index qui suivent le premier index avec une erreur n’ont peut-être pas été tentés, même si le membre **Err** de la structure [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) contient des JET_errSuccess.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Requiert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


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
