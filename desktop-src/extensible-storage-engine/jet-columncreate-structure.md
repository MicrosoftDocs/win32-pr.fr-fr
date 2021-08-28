---
description: 'En savoir plus sur : structure JET_COLUMNCREATE'
title: Structure JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ffe79dde0f24e82aa7ca9457604ea76b587e9b29
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984022"
---
# <a name="jet_columncreate-structure"></a>Structure JET_COLUMNCREATE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_columncreate-structure"></a>Structure JET_COLUMNCREATE

La structure **JET_COLUMNCREATE** décrit une colonne à créer dans une base de données.

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure en octets. Ce champ doit être initialisé à **sizeof (JET_COLUMNCREATE)**.

**szColumnName**

Nom de la colonne à créer. Le nom doit respecter les critères suivants :

  - Sa longueur doit être inférieure à JET_cbNameMost caractères, à l’exclusion de la valeur NULL de fin.

<!-- end list -->

  - Il ne doit contenir que des caractères provenant des jeux suivants : de 0 à 9, de A à Z, de a à z et toutes les autres signes de ponctuation, à l’exception du point d’exclamation ( \! ), de la virgule (,), du crochet ouvrant ( \[ ) et du crochet fermant ( \] ), c’est-À-dire des caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c,

<!-- end list -->

  - Il ne peut pas commencer par un espace.

<!-- end list -->

  - Il doit contenir au moins un caractère autre qu’un espace.

**coltyp**

Type de la colonne (par exemple, texte, binaire ou numérique). Pour plus d’informations, consultez [JET_COLTYP](./jet-coltyp.md).

**cbMax**

Longueur maximale, en octets, d’une colonne de longueur variable. Longueur de la colonne pour les colonnes de longueur fixe.

**grbit**

Groupe de bits qui contiennent les options pour cette structure, et qui incluent zéro, une ou plusieurs des valeurs suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>La colonne est fixe. Elle utilise toujours la même quantité d’espace dans une ligne, quelle que soit la quantité de données stockées dans la colonne. JET_bitColumnFixed ne peut pas être utilisé avec JET_bitColumnTagged. Ce bit ne peut pas être utilisé avec des valeurs longues, telles que <strong>JET_coltypLongText</strong> et <strong>JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>La colonne est balisée. Les colonnes avec balises n’occupent pas d’espace dans la base de données si elles ne contiennent pas de données. Ce bit ne peut pas être utilisé avec JET_bitColumnFixed.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>La colonne ne doit jamais être définie sur une valeur NULL.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>La colonne est incrémentée automatiquement. Le nombre est un nombre plus important et il est garanti qu’il est unique dans une table. Toutefois, le nombre ne peut pas être continu. Par exemple, si cinq lignes sont insérées dans une table, la colonne AutoIncrement peut contenir les valeurs {1, 2, 6, 7, 8}.</p><p><strong>Windows 2000 :</strong> Ce bit ne peut être utilisé que sur des colonnes de type <strong>JET_coltypLong</strong>.</p><p><strong>Windows Server 2003 et versions ultérieures :</strong> Ce bit ne peut être utilisé que sur des colonnes de type <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Ce bit n’est valide que sur les appels à <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Ce bit n’est valide que sur les appels à <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Ce bit n’est valide que sur les appels à <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>La colonne peut être à valeurs multiples. Une colonne à valeurs multiples peut avoir zéro, une ou plusieurs valeurs associées. Les différentes valeurs d’une colonne à valeurs multiples sont identifiées par le membre <strong>itagSequence</strong> de différentes structures, par exemple, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Les colonnes à valeurs multiples doivent être des colonnes avec balises ; autrement dit, ils ne peuvent pas être de longueur fixe ou de colonnes de longueur variable.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>La colonne est une colonne de mise à jour du tiers de confiance. Une colonne de mise à jour de tiers de confiance peut être mise à jour simultanément par différentes sessions avec <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> et maintenir la cohérence transactionnelle.</p><ul><li><p>Une colonne de mise à jour de dépôt ne peut être créée que si la table est vide.</p></li><li><p>Une colonne de mise à jour de tiers de confiance doit être de type <strong>JET_coltypLong.</strong></p></li><li><p>Une colonne de mise à jour fiduciaire doit avoir une valeur par défaut ( <strong>cbDefault</strong> doit être positive).</p></li><li><p>JET_bitColumnEscrowUpdate ne peut pas être utilisé conjointement avec les constantes suivantes :</p><ul><li><p>JET_bitColumnTagged</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li></ul></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>La colonne est créée sans version. Les autres transactions tentant d’ajouter une colonne portant le même nom échouent. Ce bit est utile uniquement avec <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Elle ne peut pas être utilisée dans une transaction.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Réservé pour un usage futur.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Utilisez JET_bitColumnDeleteOnZero au lieu de JET_bitColumnFinalize. JET_bitColumnFinalize spécifie qu’une colonne peut être finalisée. Lorsqu’une colonne qui peut être finalisée a une colonne de mise à jour de dépôt qui atteint zéro, la ligne est supprimée. Les versions ultérieures peuvent appeler une fonction de rappel à la place. Pour plus d’informations, consultez <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Une colonne pouvant être finalisée doit être une colonne de mise à jour de tiers de confiance. JET_bitColumnFinalize ne peut pas être utilisé avec JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>La valeur par défaut d’une colonne est fournie par la fonction de rappel, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Une colonne qui a une valeur par défaut définie par l’utilisateur doit être une colonne avec balises. <strong>pvDefault</strong> doit pointer vers une structure <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> et <strong>cbDefault</strong> doit avoir la valeur sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p><p>JET_bitColumnUserDefinedDefault ne peut pas être utilisé conjointement avec les constantes suivantes :</p><ul><li><p>JET_bitColumnFixed</p></li><li><p>JET_bitColumnNotNULL</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li><li><p>JET_bitColumnUpdatable</p></li><li><p>JET_bitColumnEscrowUpdate</p></li><li><p>JET_bitColumnFinalize</p></li><li><p>JET_bitColumnDeleteOnZero</p></li><li><p>JET_bitColumnMaybeNull</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>La colonne est une colonne de mise à jour de dépôt, et lorsqu’elle atteint zéro, l’enregistrement est supprimé. Une utilisation courante d’une colonne qui peut être finalisée consiste à l’utiliser comme un champ de décompte de références et, lorsque le champ atteint zéro, l’enregistrement est supprimé. JET_bitColumnDeleteOnZero est lié à JET_bitColumnFinalize. Une colonne de suppression sur zéro doit être une colonne de mise à jour de tiers de confiance. JET_bitColumnDeleteOnZero ne peut pas être utilisé avec JET_bitColumnFinalize. JET_bitColumnDeleteOnZero ne peut pas être utilisé avec des colonnes par défaut définies par l’utilisateur.</p> | 



**pvDefault**

Pointe vers une mémoire tampon qui sera la valeur par défaut pour une colonne. La longueur de la mémoire tampon est **cbDefault**. S’il n’existe pas de valeur par défaut, **pvDefault** doit avoir la valeur null et **cbDefault** doit avoir la valeur zéro. Si *Grbit* a JET_bitColumnUserDefinedDefault défini, **pvDefault** est interprété comme un pointeur vers une structure JET_USERDEFINEDDEFAULT. Les valeurs par défaut ne peuvent pas dépasser 255 octets. Si une valeur par défaut est supérieure à 255 octets, elle est tronquée en mode silencieux.

**cbDefault**

Taille, en octets, de la mémoire tampon spécifiée par **pvDefault**.

**cp**

Page de codes de la colonne. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur zéro signifie que la valeur par défaut sera utilisée (anglais, 1252). Si la colonne n’est pas une colonne de texte, la page de codes est automatiquement définie sur zéro.

**ColumnID**

En cas de réussite, l’identificateur de colonne de la colonne qui vient d’être créée est renvoyé dans ce champ. En cas d’échec, la valeur n’est pas définie.

**Raise**

Le champ **Err** contient l’état de la création de cette colonne. Pour obtenir la liste des valeurs de retour probables, consultez [JetAddColumn](./jetaddcolumn-function.md) .

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_COLUMNCREATE_W</strong> (Unicode) et <strong>JET_COLUMNCREATE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Voir aussi

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
