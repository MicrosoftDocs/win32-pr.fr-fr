---
description: 'En savoir plus sur : fonction JetCreateTable'
title: Fonction JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522224"
---
# <a name="jetcreatetable-function"></a>Fonction JetCreateTable


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetcreatetable-function"></a>Fonction JetCreateTable

La fonction **JetCreateTable** crée une table vide dans une base de données ESE.

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser.

*dbid*

Identificateur de base de données à utiliser.

*szTableName*

Nom de l’index à créer.

Le nom doit être mis en forme conformément aux règles suivantes :

  - Être inférieur à JET_cbNameMost, à l’exclusion de la valeur NULL de fin.

  - Être constitué du jeu de caractères suivant : de 0 à 9, de A à Z, de a à z et de tous les autres signes de ponctuation, à l’exception de « \! » (point d’exclamation), « , » (virgule), « \[ » (crochet ouvrant) et « \] » (crochet fermant), c’est-à-dire les caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c, 0x5d à 0x7F.

  - Ne commence pas par un espace.

  - Être constitué d’au moins un caractère autre qu’un espace.

*lPages*

Nombre initial de pages de base de données à allouer pour la table. La spécification d’un nombre supérieur à un peut réduire la fragmentation si de nombreuses lignes sont insérées dans cette table.

*lDensity*

Densité de la table, en points de pourcentage. Le nombre doit être égal à 0 ou compris entre 20 et 100. Le passage de 0 signifie que la valeur par défaut doit être utilisée. La valeur par défaut est 80.

*pTableID*

En cas de réussite, l’identificateur de table est retourné dans ce champ. La valeur n’est pas définie si l’API ne retourne pas JET_errSuccess.

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
<td><p>Une densité non valide a été transmise dans le membre <em>ulDensity</em> de la structure <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> ou <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Signifie que la table nommée dans le membre <strong>szTemplateTableName</strong> de la structure <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> n’était pas marquée comme table de modèle (autrement dit, cette table n’avait pas de JET_bitTableCreateTemplateTable définie).</p></td>
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
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP et versions ultérieures. Un index de tuple n’autorise pas la définition du membre <strong>cbVarSegMac</strong> de la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP et versions ultérieures. Un index de tuple ne peut être que sur une colonne de type texte ou Unicode. Toute tentative d’index d’autres colonnes (telles que des colonnes binaires) entraîne JET_errIndexTuplesTextColumnsOnly.</p></td>
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

**JetCreateTable** crée une table qui ne contient aucune colonne. Pour ajouter des colonnes, consultez [JetAddColumn](./jetaddcolumn-function.md).

En interne, **JetCreateTable** appelle [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), en remplissant une structure [JET_TABLECREATE2](./jet-tablecreate2-structure.md) avec :

  - JET_TABLECREATE2. cbStruct = sizeof (JET_TABLECREATE2)

  - JET_TABLECREATE2. szTableName = szTableName

  - JET_TABLECREATE2. ulPages = lPage

  - JET_TABLECREATE2. ulDensity = lDensity

  - JET_TABLECREATE2. TableId = JET_tableidNil

Tous les autres champs de la structure interne [JET_TABLECREATE2](./jet-tablecreate2-structure.md) sont définis sur zéro ou null. Lors de la sortie, *pTableID* est défini sur JET_TABLECREATE2. TableId.

Pour plus d’informations, consultez [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .

Comme [JetOpenTable](./jetopentable-function.md), lorsque l’application est effectuée à l’aide du membre **TableID** renvoyé à partir de la structure [JET_TABLECREATE2](./jet-tablecreate2-structure.md) , elle doit généralement être fermée avec [JetCloseTable](./jetclosetable-function.md).

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
<td><p>Implémenté en tant que <strong>JetCreateTableW</strong> (Unicode) et <strong>JetCreateTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
