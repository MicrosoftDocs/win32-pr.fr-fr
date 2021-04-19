---
description: 'En savoir plus sur : fonction JetCreateTableColumnIndex'
title: JetCreateTableColumnIndex fonction)
TOCTitle: JetCreateTableColumnIndex Function
ms:assetid: 9192614b-20a6-40fb-906a-51fc057e7483
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269343(v=EXCHG.10)
ms:contentKeyID: 32765632
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndexA
- JetCreateTableColumnIndexW
- JetCreateTableColumnIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aea9f79617c35c5a956f0cd5f621c7faadffe668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521873"
---
# <a name="jetcreatetablecolumnindex-function"></a>JetCreateTableColumnIndex fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetcreatetablecolumnindex-function"></a>JetCreateTableColumnIndex fonction)

La fonction **JetCreateTableColumnIndex** crée une table dans une base de données ESE avec un ensemble initial d’index et un ensemble initial de colonnes à partir d’un tableau de structures [JET_TABLECREATE](./jet-tablecreate-structure.md) . Le nom **JetCreateTableColumnIndex** provient de l’ordre de création des objets. Elle crée d’abord une table, des colonnes, puis enfin des index.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE* ptablecreate
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*dbid*

Identificateur de base de données à utiliser pour l’appel d’API.

*ptablecreate*

Pointeur vers une structure [JET_TABLECREATE](./jet-tablecreate-structure.md) qui définit la table à créer. Pour plus d’informations, consultez [JET_TABLECREATE](./jet-tablecreate-structure.md) .

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>La fonction de rappel n’a pas pu être résolue. La DLL n’a peut-être pas été trouvée, ou la fonction dans la DLL n’a peut-être pas été trouvée. Une fois la journalisation suffisante activée, le journal des événements fournit plus de détails.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotIndex</p></td>
<td><p>Une tentative d’indexation sur une colonne de dépôt/mise à jour ou SLV (Notez que les colonnes SLV sont dépréciées) a été tentée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL</p></td>
<td><p>Si ptablecreate- &gt; Grbit spécifie JET_bitTableCreateTemplateTable, mais ptablecreate- &gt; szTemplateTableName a la valeur null.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Une colonne existe déjà.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Une tentative d’indexation sur une colonne inexistante a été effectuée. Toute tentative d’indexation conditionnelle sur une colonne inexistante peut également générer cette erreur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Une tentative d’ajout d’une colonne redondante a été effectuée. Il ne doit y avoir qu’une seule colonne AutoIncrement et pas plus d’une colonne version par table.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Cette erreur est retournée si le membre <strong>ulDensity</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est défini sur un nombre inférieur à 20 ou supérieur à 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Signifie que la table nommée dans le membre <strong>szTemplateTableName</strong> de la structure <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> n’a pas été marquée comme table de modèle (autrement dit, cette table n’avait pas de JET_bitTableCreateTemplateTable définie).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Une tentative de définition de deux index identiques a été effectuée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Une tentative a été effectuée pour spécifier plusieurs index primaires pour une table. Une table doit avoir un seul index primaire. Si aucun index primaire n’est spécifié, le moteur de base de données en crée un en toute transparence.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Une définition d’index non valide a été spécifiée. Voici quelques-unes des raisons possibles de la réception de cette erreur :</p>
<ul>
<li><p>Un index principal est conditionnel (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexPrimary jeu et le membre <strong>cConditionalColumn</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est supérieur à zéro).</p></li>
<li><p>Windows Server 2003 et versions ultérieures. La tentative de création d’un index de tuple avec des limites de tuple, mais sans passer le membre <strong>ptuplelimits</strong> dans la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexTupleLimits défini, mais le pointeur <strong>ptuplelimits</strong> a la valeur null).</p></li>
<li><p>Passage d’une définition de clé non valide dans le membre <strong>szKey</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Pour plus d’informations sur les définitions valides, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></li>
<li><p>La définition du membre <strong>cbVarSegMac</strong> dans <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> est supérieure à JET_cbPrimaryKeyMost (pour un index principal) ou supérieure à JET_cbSecondaryKeyMost (pour un index secondaire).</p></li>
<li><p>Passage d’une combinaison non valide pour un index Unicode défini par l’utilisateur (un qui a le bit JET_bitIndexUnicode défini dans le membre <strong>Grbit</strong> de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Certaines causes courantes incluent le membre <strong>pidxunicode</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a la valeur null, ou le LCID spécifié dans la structure <strong>pidxunicode</strong> n’est pas valide.</p></li>
<li><p>Spécification d’une colonne à valeurs multiples pour un index primaire.</p></li>
<li><p>Tentative d’indexation d’un trop grand nombre de colonnes conditionnelles. Le membre <strong>cConditionalColumn</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas être supérieur à JET_ccolKeyMost.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP et versions ultérieures. Une structure de <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> a été spécifiée et ses limites ne sont pas prises en charge. Consultez la section Notes de la structure <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP et versions ultérieures. Un index de tuple ne peut pas être unique (autrement dit, le membre <em>Grbit</em> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexUnique défini).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP et versions ultérieures. Un index de tuple ne peut être que sur une seule colonne (autrement dit, si le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a JET_bitIndexTuples jeu et que le membre <strong>szKey</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> spécifie plusieurs colonnes).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP et versions ultérieures. Un index de tuple ne peut pas être un index primaire (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ne doit pas avoir JET_bitIndexPrimary et JET_bitIndexTuples défini).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP et versions ultérieures. Un index de tuple ne peut être que sur une colonne de type texte ou Unicode. Toute tentative d’index d’autres colonnes (telles que des colonnes binaires) entraîne JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP et versions ultérieures. Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Une tentative de création d’un index sans informations de version a été effectuée dans une transaction.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Le membre <strong>CP</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur une page de codes valide. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Le membre <strong>coltyp</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> n’a pas été défini sur un type de colonne valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCreateIndex</p></td>
<td><p>Cette erreur peut se produire pour les raisons suivantes :</p>
<ul>
<li><p>Le membre <strong>rgindexcreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</p></li>
<li><p>Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</p></li>
<li><p>Le membre <strong>cbStruct</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a pas été défini sur une valeur valide.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Une combinaison de membres <strong>Grbit</strong> non valide a été spécifiée dans <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</p>
<p>La définition de l’index n’est pas valide, car le membre <strong>Grbit</strong> contient des valeurs incohérentes. Voici quelques raisons possibles :</p>
<ul>
<li><p>Un index primaire a un bit ignore spécifié (autrement dit, JET_bitIndexPrimary a été passé avec JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull ou JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Un index vide n’ignore pas les membres NULL (autrement dit, le membre <strong>Grbit</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a JET_bitIndexEmpty défini, mais n’a pas de JET_bitIndexIgnoreAnyNull défini).</p></li>
<li><p>Passage d’une structure <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> avec un membre <strong>Grbit</strong> non valide.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Un ID de paramètres régionaux (LCID) non valide a été transmis (par le biais du membre <strong>LCID</strong> de la structure <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> qui est référencée par le membre <strong>pidxunicode</strong> dans la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ou par le champ <strong>LCID</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un paramètre non valide a été spécifié. Voici quelques raisons possibles :</p>
<ul>
<li><p>Le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> a la valeur null.</p></li>
<li><p>Le membre <strong>cbStruct</strong> de l’une des structures <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> données dans le membre <strong>rgcolumncreate</strong> de la structure <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> n’a pas la valeur sizeof (JET_COLUMNCREATE).</p></li>
<li><p>Le membre <strong>cbKey</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> a la valeur zéro.</p></li>
<li><p>Le membre <strong>cbStruct</strong> d’une structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> n’a pas la valeur sizeof (JET_INDEXCREATE).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>L’enregistrement est trop volumineux. La somme du membre <strong>cbMax</strong> de la structure <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> pour toutes les colonnes fixes ne doit pas dépasser une certaine valeur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate</p></td>
<td><p>La table existe déjà.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée. Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Une erreur s’est produite lors de la normalisation d’une colonne Unicode. Cela peut être dû à un manque de ressources système.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

L’appel de **JetCreateTableColumnIndex** est identique à l’appel de [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), avec chaque champ de la structure [JET_TABLECREATE2](./jet-tablecreate2-structure.md) contenant la valeur du champ correspondant de [JET_TABLECREATE](./jet-tablecreate-structure.md), avec les exceptions suivantes :

  - JET_TABLECREATE2. cbStruct défini sur sizeof (JET_TABLECREATE2)

  - JET_TABLECREATE2. szCallback défini sur NULL

  - JET_TABLECREATE2. cbtyp défini sur 0

Pour plus d’informations, consultez [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .

Comme [JetOpenTable](./jetopentable-function.md), lorsque l’application est effectuée à l’aide de l' *TableID* retourné, elle doit généralement être fermée avec [JetCloseTable](./jetclosetable-function.md).

#### <a name="requirements"></a>Configuration requise

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
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetCreateTableColumnIndexW</strong> (Unicode) et <strong>JetCreateTableColumnIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex]()  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
