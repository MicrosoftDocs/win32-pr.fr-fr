---
description: 'En savoir plus sur : structure JET_COLUMNDEF'
title: Structure JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953117"
---
# <a name="jet_columndef-structure"></a>Structure JET_COLUMNDEF


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_columndef-structure"></a>Structure JET_COLUMNDEF

La structure **JET_COLUMNDEF** définit les données qui peuvent être stockées dans une colonne.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure en octets. Elle doit être définie sur sizeof (JET_COLUMNDEF).

**ColumnID**

Réservé. **ColumnID** doit avoir la valeur 0 (zéro).

**coltyp**

Type de la colonne (par exemple, texte, binaire ou numérique). Pour plus d’informations, consultez [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Réservé. **wCountry** doit avoir la valeur 0 (zéro).

**langid**

Obsolète. **LangID** doit avoir la valeur 0 (zéro).

**cp**

Page de codes de la colonne. Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200). La valeur zéro signifie que la valeur par défaut sera utilisée (anglais, 1252). Si la colonne n’est pas une colonne de texte, la page de codes est automatiquement définie sur zéro.

**wCollate**

Réservé. **wCollate** doit avoir la valeur 0 (zéro).

**cbMax**

La longueur maximale, en octets, d’une colonne de longueur variable, ou la longueur d’une colonne de longueur fixe.

**grbit**

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro, une ou plusieurs des valeurs suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitColumnFixed</p></td>
<td><p>La colonne sera fixe. Elle utilise toujours la même quantité d’espace dans une ligne, quelle que soit la quantité de données stockées dans la colonne. JET_bitColumnFixed ne peut pas être utilisé avec JET_bitColumnTagged. Ce bit ne peut pas être utilisé avec des valeurs longues ( <strong>JET_coltypLongText</strong> et <strong>JET_coltypLongBinary</strong>).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>La colonne est balisée. Les colonnes avec balises n’occupent pas d’espace dans la base de données si elles ne contiennent pas de données. Ce bit ne peut pas être utilisé avec JET_bitColumnFixed.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNULL</p></td>
<td><p>La colonne ne doit jamais être définie sur une valeur NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnVersion</p></td>
<td><p>La colonne est une colonne de version qui spécifie la version de la ligne. La valeur de cette colonne commence à zéro et est incrémentée automatiquement pour chaque mise à jour sur la ligne.</p>
<p>Ce bit ne peut être appliqué qu’à des colonnes <strong>JET_coltypLong</strong> . Ce bit ne peut pas être utilisé avec JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate ou JET_bitColumnTagged.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>La colonne est automatiquement incrémentée. Le nombre est un nombre plus important et il est garanti qu’il est unique dans une table. Toutefois, les nombres ne peuvent pas être continus. Par exemple, si cinq lignes sont insérées dans une table, &quot; la &quot; colonne AutoIncrement peut contenir les valeurs {1, 2, 6, 7, 8}. Ce bit ne peut être utilisé que sur des colonnes de type <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong>.</p>
<p><strong>Windows 2000 :  </strong> Dans Windows 2000, ce bit ne peut être utilisé que sur des colonnes de type <strong>JET_coltypLong</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>Ce bit n’est valide que sur les appels à <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>Ce bit n’est valide que sur les appels à <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>Ce bit n’est valide que sur les appels à <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>La colonne peut être à valeurs multiples. Une colonne à valeurs multiples peut avoir zéro, une ou plusieurs valeurs associées. Les différentes valeurs d’une colonne à valeurs multiples sont identifiées par un nombre appelé le membre <strong>itagSequence</strong> , qui appartient à différentes structures, notamment : <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>et <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Les colonnes à valeurs multiples doivent être des colonnes avec balises ; autrement dit, ils ne peuvent pas être de longueur fixe ou de colonnes de longueur variable.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>Spécifie qu’une colonne est une colonne de mise à jour de dépôt. Une colonne de mise à jour de tiers de confiance peut être mise à jour simultanément par différentes sessions avec <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> et assurer la cohérence transactionnelle. Une colonne de mise à jour de dépôt doit également remplir les conditions suivantes :</p>
<ul>
<li><p>Une colonne de mise à jour de dépôt ne peut être créée que si la table est vide.</p></li>
</ul>
<ul>
<li><p>Une colonne de mise à jour de tiers de confiance doit être de type <strong>JET_coltypLong</strong>.</p></li>
</ul>
<ul>
<li><p>Une colonne de mise à jour fiduciaire doit avoir une valeur par défaut ( <strong>cbDefault</strong> doit être positive).</p></li>
</ul>
<ul>
<li><p>JET_bitColumnEscrowUpdate ne peut pas être utilisé conjointement avec JET_bitColumnTagged, JET_bitColumnVersion ou JET_bitColumnAutoincrement.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>La colonne sera créée dans un sans informations sur la version. Cela signifie que les autres transactions qui tentent d’ajouter une colonne portant le même nom échoueront. Ce bit est utile uniquement avec <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Elle ne peut pas être utilisée dans une transaction.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>Réservé pour un usage futur.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>Utilisez JET_bitColumnDeleteOnZero au lieu de JET_bitColumnFinalize. JET_bitColumnFinalize qu’une colonne peut être finalisée. Lorsqu’une colonne qui peut être finalisée a une colonne de mise à jour de dépôt qui atteint zéro, la ligne est supprimée. Les versions ultérieures peuvent appeler une fonction de rappel à la place (pour plus d’informations, consultez <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Une colonne pouvant être finalisée doit être une colonne de mise à jour de tiers de confiance. JET_bitColumnFinalize ne peut pas être utilisé avec JET_bitColumnUserDefinedDefault.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>La valeur par défaut d’une colonne est fournie par une fonction de rappel. Consultez <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Une colonne qui a une valeur par défaut définie par l’utilisateur doit être une colonne avec balises. Si vous spécifiez JET_bitColumnUserDefinedDefault, <strong>pvDefault</strong> doit pointer vers une structure <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> et <strong>cbDefault</strong> doit avoir la valeur sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</p>
<ul>
<li><p>JET_bitColumnUserDefinedDefault ne peut pas être utilisé conjointement avec JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero ou JET_bitColumnMaybeNull.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>La colonne est une colonne de mise à jour de dépôt, et lorsqu’elle atteint zéro, l’enregistrement est supprimé. Une utilisation courante d’une colonne qui peut être finalisée consiste à l’utiliser comme un champ de décompte de références et, lorsque le champ atteint zéro, l’enregistrement est supprimé. JET_bitColumnDeleteOnZero est lié à JET_bitColumnFinalize. Une colonne de suppression sur zéro doit être une colonne de mise à jour de tiers de confiance. JET_bitColumnDeleteOnZero ne peut pas être utilisé avec JET_bitColumnFinalize. JET_bitColumnDeleteOnZero ne peut pas être utilisé avec des colonnes par défaut définies par l’utilisateur.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

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
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetOpenTempTable2](./jetopentemptable2-function.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
