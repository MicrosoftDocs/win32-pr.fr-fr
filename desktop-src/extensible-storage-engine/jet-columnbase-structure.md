---
description: 'En savoir plus sur : structure JET_COLUMNBASE'
title: Structure JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 603025166eed7c92d98148a43d26046308235777
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236699"
---
# <a name="jet_columnbase-structure"></a>Structure JET_COLUMNBASE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_columnbase-structure"></a>Structure JET_COLUMNBASE

La structure **JET_COLUMNBASE** décrit les paramètres d’une colonne de base. Les fonctions [JetGetColumnInfo](./jetgetcolumninfo-function.md) et [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) utilisent la structure **JET_COLUMNBASE** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de cette structure, en octets. Affectez à **cbStruct** la valeur sizeof (JET_COLUMNBASE).

**ColumnID**

Réservé. Affectez à **ColumnID** la valeur 0 (zéro).

**coltyp**

Type de la colonne (par exemple, texte, binaire ou numérique). Pour plus d’informations, consultez [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Réservé. Défini sur 0 (zéro).

**langid**

Réservé. Défini sur 0 (zéro).

**cp**

Page de codes de la colonne. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur zéro signifie que la valeur par défaut sera utilisée (anglais, 1252). Si la colonne n’est pas une colonne de texte, la page de codes est automatiquement définie sur zéro.

**wFiller**

Réservé. Défini sur 0 (zéro).

**cbMax**

Longueur maximale, en octets, d’une colonne de longueur variable, ou longueur réelle, en octets, d’une colonne de longueur fixe.

**grbit**

Options de la colonne, y compris zéro, une ou plusieurs des valeurs suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>La colonne est fixe et occupe la même quantité d’espace dans une ligne, quelle que soit la quantité de données qu’elle contient. JET_bitColumnFixed ne peut pas être combiné avec JET_bitColumnTagged et ne peut pas être utilisé lorsque le membre <strong>coltyp</strong> a la valeur <strong>JET_coltypLongText</strong> ou <strong>JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>La colonne est balisée et occupe de l’espace dans la base de données uniquement si elle contient des données. JET_bitColumnTagged ne peut pas être combiné avec JET_bitColumnFixed, JET_bitColumnVersion ou JET_bitColumnEscrowUpdate.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>La colonne ne doit pas être définie sur une valeur <strong>null</strong> .</p><p>JET_bitColumnNotNULL ne peut pas être combiné avec JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnVersion</p> | <p>La colonne est une colonne de version qui spécifie la version de la ligne. La valeur de cette colonne commence à zéro et est incrémentée automatiquement pour chaque mise à jour de la ligne.</p><p>JET_bitColumnVersion peut être utilisé uniquement lorsque le membre <strong>coltyp</strong> est défini sur <strong>JET_coltypLong</strong> et ne peut pas être combiné avec JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged ou JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>La colonne est incrémentée automatiquement. Le nombre est un nombre plus important et il est garanti qu’il est unique dans une table. Toutefois, les nombres ne peuvent pas être séquentiels. Par exemple, si cinq lignes sont insérées dans une table, la colonne incrémentée automatiquement peut contenir les valeurs {1, 2, 6, 7, 8}.</p><p>JET_bitColumnAutoincrement peut être utilisé uniquement lorsque le membre <strong>coltyp</strong> est défini sur <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong> et ne peut pas être combiné avec JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault ou JET_bitColumnVersion.</p><p><strong>Windows 2000 :</strong> JET_bitColumnVersion peut être utilisé uniquement lorsque le membre <strong>coltyp</strong> est défini sur <strong>JET_coltypLong</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Valide uniquement pour les appels à <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>. JET_bitColumnUpdatable ne peut pas être combiné avec JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Valide uniquement sur les appels à <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Valide uniquement sur les appels à <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>La colonne peut être à valeurs multiples. Une colonne à valeurs multiples peut avoir zéro, une ou plusieurs valeurs associées. Les différentes valeurs d’une colonne à valeurs multiples sont identifiées par un nombre dans le membre <strong>itagSequence</strong> de différentes structures, par exemple, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Les colonnes à valeurs multiples doivent être des colonnes avec balises ; autrement dit, ils ne peuvent pas être de longueur fixe ou de colonnes de longueur variable.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Spécifie qu’une colonne est une colonne de mise à jour de dépôt qui peut être mise à jour simultanément par différentes sessions avec <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> et qui aura une cohérence transactionnelle.</p><ul><li><p>Une colonne de mise à jour de dépôt ne peut être créée que si la table est vide.</p></li></ul><ul><li><p>Pour une colonne de mise à jour de dépôt, le membre <strong>coltyp</strong> doit être défini sur <strong>JET_coltypLong.</strong></p></li></ul><ul><li><p>Une colonne de mise à jour fiduciaire doit avoir une valeur par défaut ( <strong>cbDefault</strong> doit être positive).</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate ne peut pas être combiné avec JET_bitColumnTagged, JET_bitColumnVersion ou JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>La colonne est créée sans numéro de version. Cela signifie que les autres transactions tentant d’ajouter une colonne portant le même nom échoueront. JET_bitColumnUnversioned est utilisé uniquement avec <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Elle ne peut pas être utilisée dans une transaction.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Réservé pour un usage futur.</p><p>JET_bitColumnMaybeNull ne peut pas être combiné avec JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Ne pas utiliser. Utilisez à la place JET_bitColumnDeleteOnZero.</p><p>La colonne peut être finalisée. Une colonne qui peut être finalisée est une colonne de mise à jour de dépôt qui provoque la suppression de la ligne lorsque la colonne atteint zéro. Les versions ultérieures peuvent appeler une fonction de rappel à la place (voir <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Une colonne pouvant être finalisée doit être une colonne de mise à jour de tiers de confiance. JET_bitColumnFinalize ne peut pas être combiné avec JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>La valeur par défaut d’une colonne est fournie par une fonction de rappel. Consultez <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Une colonne qui a une valeur par défaut définie par l’utilisateur doit être une colonne avec balises. Si JET_bitColumnUserDefinedDefault est spécifié, <strong>pvDefault</strong> doit pointer vers une structure <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> et <strong>cbDefault</strong> doit avoir la valeur sizeof (JET_USERDEFINEDDEFAULT).</p><p>JET_bitColumnUserDefinedDefault ne peut pas être combiné avec JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero ou JET_bitColumnMaybeNull.</p> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>La colonne est une colonne de mise à jour de dépôt et lorsqu’elle atteint zéro, l’enregistrement est supprimé. Les champs de décompte de références sont couramment utilisés pour les colonnes de suppression sur zéro. Lorsque le nombre de références est égal à zéro, l’enregistrement est supprimé. Une colonne de suppression sur zéro doit être une colonne de mise à jour de tiers de confiance.</p><p>JET_bitColumnDeleteOnZero remplace JET_bitColumnFinalize.</p><p>JET_bitColumnDeleteOnZero ne peut pas être combiné avec JET_bitColumnFinalize ou JET_bitColumnUserDefinedDefault, et ne peut pas être utilisé avec des colonnes par défaut définies par l’utilisateur.</p> | 



**szBaseTableName**

Table à partir de laquelle la table actuelle hérite de son DDL.

**szBaseColumnName**

Nom de la colonne dans la table de modèle.

### <a name="remarks"></a>Notes

**JET_COLUMNBASE** contient une grande partie des mêmes informations que [JET_COLUMNDEF](./jet-columndef-structure.md), mais il ajoute des champs de chaîne pour décrire la table de base (si une DDL hiérarchique a été utilisée).

### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_COLUMNBASE_W</strong> (Unicode) et <strong>JET_COLUMNBASE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Voir aussi

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
