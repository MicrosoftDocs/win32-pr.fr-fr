---
description: 'En savoir plus sur : fonction JetAddColumn'
title: Fonction JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c735fb077816fc555b28e4b81b93798898efd92e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530009"
---
# <a name="jetaddcolumn-function"></a>Fonction JetAddColumn


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetaddcolumn-function"></a>Fonction JetAddColumn

La fonction **JetAddColumn** ajoute une nouvelle colonne à une table existante dans une base de données ESE.

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour l’appel d’API.

*TableID*

Table à laquelle ajouter la colonne.

*szColumnName*

Nom de la colonne à ajouter. Le nom doit respecter les critères suivants :

  - Sa longueur doit être inférieure à JET_cbNameMost caractères, à l’exclusion de la **valeur null** de fin.

  - Il ne doit contenir que des caractères issus des jeux suivants : de 0 à 9, de A à Z, de a à z et toutes les autres signes de ponctuation, à l’exception du point d’exclamation ( \! ), de la virgule (,), du crochet ouvrant () et du \[ crochet fermant ( \] ).

  - Il ne peut pas commencer par un espace.

  - Il doit contenir au moins un caractère autre qu’un espace.

*pcolumndef*

Pointeur vers une structure [JET_COLUMNDEF](./jet-columndef-structure.md) , qui définit les données qui peuvent être stockées dans une colonne.

*pvDefault*

Pointeur vers une mémoire tampon qui contient la valeur par défaut de la colonne. La longueur de la mémoire tampon est **cbDefault**. S’il n’y a pas de valeur par défaut, affectez la valeur **null** à **pvDefault** et **cbDefault** à zéro. Les valeurs par défaut ne peuvent pas être supérieures à JET_cbColumnMost octets pour les colonnes fixes ou les octets JET_cbLVDefaultValueMost pour les valeurs longues. Si une valeur par défaut est supérieure à celle-ci, elle sera tronquée en mode silencieux.

Si *Grbit* a JET_bitColumnUserDefinedDefault défini, **pvDefault** est interprété comme un pointeur vers une structure [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .

*cbDefault*

Taille, en octets, de la mémoire tampon spécifiée dans **pvDefault**.

*pColumnID*

Pointeur vers une structure [JET_COLUMNID](./jet-columnid.md) , qui, en cas de réussite, reçoit l’identificateur de la colonne qui vient d’être créée. En cas d’échec, la valeur n’est pas définie.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L'opération a réussi.</p> | 
| <p>JET_errFixedDDL</p> | <p>Une tentative de modification de la définition des données d’une table DDL fixe a été effectuée. Une table de modèle est un exemple de table avec une DDL fixe.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Un paramètre non valide a été passé dans l’API. Voici quelques exemples de paramètres non valides :</p><ul><li><p>Passage de la taille incorrecte de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> dans son membre <em>cbStruct</em> .</p></li><li><p>Le passage de JET_bitColumnUserDefinedDefault, mais pas la définition de <strong>cbDefault</strong> sur sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li></ul> | 
| <p>JET_errInTransaction</p> | <p>Une tentative a été effectuée pour ajouter une colonne avec le bit JET_bitColumnUnversioned défini, mais la session est actuellement dans une transaction.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Une colonne existe déjà. Une tentative d’ajout d’une colonne sans informations de version a été effectuée et cette colonne existe déjà.</p> | 
| <p>JET_errTableNotEmpty</p> | <p>La table contient des données. Une colonne de mise à jour de tiers de confiance ne peut être ajoutée qu’à une table vide.</p> | 
| <p>JET_errRecordTooBig</p> | <p>L’enregistrement est trop volumineux. La somme du paramètre <strong>cbMax</strong> pour les colonnes fixes ne doit pas dépasser une certaine valeur.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée. Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Une tentative d’ajout d’une colonne redondante a été effectuée. Il ne doit y avoir qu’une seule colonne AutoIncrement et pas plus d’une colonne version par table.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>La fonction de rappel n’a pas pu être résolue. La DLL n’a peut-être pas été trouvée, ou la fonction dans la DLL n’a peut-être pas été trouvée. Le journal des événements fournit plus de détails si la journalisation suffisante est activée.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Un avertissement indiquant que la longueur maximale (<strong>cbMax</strong>) d’une colonne fixe ou variable était supérieure à JET_cbColumnMost. Cette limite ne s’applique pas aux valeurs longues ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> et <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 
| <p>JET_errInvalidName</p> | <p>Un nom non valide a été passé en tant que <strong>szColumnName</strong>. Pour plus d’informations sur les restrictions, consultez les critères pour <strong>szColumnName</strong>.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Le champ <strong>coltyp</strong> n’est pas défini sur un type de colonne valide.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Le paramètre <strong>CP</strong> de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</p> | 
| <p>JET_errTaggedNotNULL</p> | <p>JET_bitColumnNotNULL ne peut pas être utilisé avec des colonnes avec balises, de valeurs longues ou SLV.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Une combinaison non valide de <em>grbits</em> a été spécifiée. Voici quelques-unes des raisons de cette erreur :</p><ul><li><p>JET_bitColumnFixed a été utilisé sur une colonne avec balises, une valeur longue ou une colonne SLV.</p></li><li><p>JET_bitColumnEscrowUpdate a été utilisé sur une colonne qui n’était pas de type <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li><li><p>JET_bitColumnEscrowUpdate a été utilisé sur une colonne de version (JET_bitColumnVersion).</p></li><li><p>JET_bitColumnEscrowUpdate a été utilisé sur une colonne AutoIncrememnt (JET_bitColumnAutoincrement).</p></li><li><p>JET_bitColumnEscrowUpdate a été utilisé sur une colonne qui n’a pas de valeur par défaut (<strong>cbDefault</strong> était égal à zéro).</p></li><li><p>JET_bitColumnFinalize a été utilisé sur une colonne qui n’est pas une colonne de mise à jour de dépôt (JET_bitColumnEscrowUpdate n’a pas été définie).</p></li><li><p>JET_bitColumnDeleteOnZero a été utilisé sur une colonne qui n’est pas une colonne de mise à jour de dépôt (JET_bitColumnEscrowUpdate n’a pas été définie).</p></li><li><p>JET_bitColumnAutoincrement a été utilisé sur une colonne qui n’a pas été <a href="gg269213(v=exchg.10).md">JET_coltypLonge</a>.</p><p><strong>Windows 2000 :</strong> cette raison du code d’erreur est utilisée uniquement dans Windows 2000.</p><p>JET_bitColumnAutoincrement a été utilisé sur une colonne qui n’était ni <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> ni <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</p><p><strong>Windows XP :</strong> cette raison du code d’erreur est utilisée dans les systèmes d’exploitation Windows XP et versions ultérieures.</p></li><li><p>JET_bitColumnVersion a été utilisé sur une colonne qui n’a pas été <a href="gg269213(v=exchg.10).md">JET_coltypLonge</a>.</p></li><li><p>JET_bitColumnVersion a été utilisé sur une colonne AutoIncrement.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnFixed.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnNotNULL.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnVersion.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnAutoincrement.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnUpdatable.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnEscrowUpdate.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnFinalize.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnDeleteOnZero.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnMaybeNull.</p></li><li><p>JET_bitColumnUserDefinedDefault a été utilisé sur une colonne non balisée (qui est fixe ou variable).</p></li></ul> | 
| <p>JET_errMultiValuedColumnMustBeTagged</p> | <p>Une colonne à valeurs multiples (JET_bitColumnMultiValued) peut uniquement être utilisée sur une colonne avec balises ou de valeurs longues (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 
| <p>JET_errCannotBeTagged</p> | <p>Une tentative d’utilisation d’une colonne avec balises a été effectuée lorsque la colonne n’est peut-être pas référencée. Voici quelques-unes des contraintes pour interdire les colonnes avec balises :</p><ul><li><p>Une colonne de mise à jour de dépôt (JET_bitColumnEscrowUpdate) ne peut pas être utilisée sur une colonne avec balises ou de valeurs longues (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></li><li><p>Une colonne AutoIncrement ne peut pas être référencée.</p></li><li><p>Une colonne de version n’est peut-être pas référencée.</p></li></ul> | 
| <p>JET_errExclusiveTableLockRequired</p> | <p>Un verrou exclusif sur la table était requis pour cette opération.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>Un avertissement indiquant que la longueur maximale (<em>cbMax</em>) d’une colonne fixe ou variable était supérieure à JET_cbColumnMost. Cette limite ne s’applique pas aux valeurs longues ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> et <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p> | 



#### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetAddColumnW</strong> (Unicode) et <strong>JetAddColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
