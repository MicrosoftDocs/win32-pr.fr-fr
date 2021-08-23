---
description: 'En savoir plus sur : énumération ColumndefGrbit'
title: Énumération ColumndefGrbit
TOCTitle: ColumndefGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumndefGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columndefgrbit(v=EXCHG.10)
ms:contentKeyID: 39513005
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f2bd26a3dac291d78b101aa56f186d9b31f7a927b1eca3e29febc7773e3c0939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042457"
---
# <a name="columndefgrbit-enumeration"></a>Énumération ColumndefGrbit

Options de la structure JET_COLUMNDEF.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ColumndefGrbit
'Usage
Dim instance As ColumndefGrbit
```

``` csharp
[FlagsAttribute]
public enum ColumndefGrbit
```

## <a name="members"></a>Membres

<table>
<thead>
<tr class="header">
<th></th>
<th>Nom du membre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>None</td>
<td>Options par défaut.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnFixed</td>
<td>La colonne sera fixe. Elle utilise toujours la même quantité d’espace dans une ligne, quelle que soit la quantité de données stockées dans la colonne. ColumnFixed ne peut pas être utilisé avec ColumnTagged. Ce bit ne peut pas être utilisé avec des valeurs longues (c’est-à-dire JET_coltyp. LongText et JET_coltyp. LongBinary).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnTagged</td>
<td>La colonne est balisée. Les colonnes avec balises n’occupent pas d’espace dans la base de données si elles ne contiennent pas de données. Ce bit ne peut pas être utilisé avec ColumnFixed.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnNotNULL</td>
<td>La colonne ne doit jamais être définie sur une valeur NULL. sur Windows XP, cela ne peut s’appliquer qu’aux colonnes fixes (bit, byte, integer, etc.).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnVersion</td>
<td>La colonne est une colonne de version qui spécifie la version de la ligne. La valeur de cette colonne commence à zéro et est incrémentée automatiquement pour chaque mise à jour sur la ligne. Cette option ne peut être appliquée qu’à JET_coltyp. Colonnes de type long. Cette option ne peut pas être utilisée avec ColumnAutoincrement, ColumnEscrowUpdate ou ColumnTagged.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnAutoincrement</td>
<td>La colonne est automatiquement incrémentée. Le nombre est un nombre plus important et il est garanti qu’il est unique dans une table. Toutefois, les nombres ne peuvent pas être continus. Par exemple, si cinq lignes sont insérées dans une table, &quot; la &quot; colonne AutoIncrement peut contenir les valeurs {1, 2, 6, 7, 8}. Ce bit ne peut être utilisé que sur des colonnes de type JET_coltyp. Long ou JET_coltyp. Accès.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnMultiValued</td>
<td>La colonne peut être à valeurs multiples. Une colonne à valeurs multiples peut avoir zéro, une ou plusieurs valeurs associées. Les différentes valeurs d’une colonne à valeurs multiples sont identifiées par un nombre appelé le membre itagSequence, qui appartient à différentes structures, notamment : JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN et JET_ENUMCOLUMNVALUE. Les colonnes à valeurs multiples doivent être des colonnes avec balises ; autrement dit, ils ne peuvent pas être de longueur fixe ou de colonnes de longueur variable.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnEscrowUpdate</td>
<td>Spécifie qu’une colonne est une colonne de mise à jour de dépôt. Une colonne de mise à jour de tiers de confiance peut être mise à jour simultanément par différentes sessions avec JetEscrowUpdate et assurer la cohérence transactionnelle. Une colonne de mise à jour de dépôt doit également remplir les conditions suivantes : une colonne de mise à jour de dépôt ne peut être créée que lorsque la table est vide. Une colonne de mise à jour de tiers de confiance doit être de type JET_coltypLong. Une colonne de mise à jour fiduciaire doit avoir une valeur par défaut. JET_bitColumnEscrowUpdate ne peut pas être utilisé conjointement avec ColumnTagged, ColumnVersion ou ColumnAutoincrement.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUnversioned</td>
<td>La colonne sera créée dans un sans informations sur la version. Cela signifie que les autres transactions qui tentent d’ajouter une colonne portant le même nom échoueront. Ce bit est utile uniquement avec JetAddColumn. Elle ne peut pas être utilisée dans une transaction.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMaybeNull</td>
<td>Lors d’une jointure externe, l’opération de récupération de colonne peut ne pas avoir de correspondance de la table interne.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUserDefinedDefault</td>
<td>La valeur par défaut d’une colonne est fournie par une fonction de rappel. Une colonne qui a une valeur par défaut définie par l’utilisateur doit être une colonne avec balises. Si vous spécifiez JET_bitColumnUserDefinedDefault, pvDefault doit pointer vers une structure JET_USERDEFINEDDEFAULT et cbDefault doit avoir la valeur sizeof (JET_USERDEFINEDDEFAULT).</td>
</tr>
<tr class="even">
<td></td>
<td>TTKey</td>
<td>La colonne est une colonne clé pour la table temporaire. L’ordre des définitions de colonne avec cette option spécifiée dans le tableau d’entrée détermine la précédence de chaque colonne clé pour la table temporaire. La première définition de colonne dans le tableau qui a cette option est définie sur la colonne clé la plus significative, et ainsi de suite. Si le moteur de base de données demande plus de colonnes clés que ce qui peut être pris en charge par le moteur de base de données, cette option est ignorée pour les colonnes clés non prises en charge.</td>
</tr>
<tr class="odd">
<td></td>
<td>TTDescending</td>
<td>L’ordre de tri de la colonne clé pour la table temporaire doit être décroissant plutôt que croissant. Si cette option est spécifiée sans TTKey, cette option est ignorée.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[ColumnCompressed](./windows7grbits.columncompressed-field.md)
