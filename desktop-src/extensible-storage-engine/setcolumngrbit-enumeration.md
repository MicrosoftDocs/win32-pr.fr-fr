---
description: 'En savoir plus sur : énumération SetColumnGrbit'
title: Énumération SetColumnGrbit
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cfde1fe2bb0cefeb108cd957b043b14fc6b224375ae82b894eab0b9a0cb8865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071475"
---
# <a name="setcolumngrbit-enumeration"></a>Énumération SetColumnGrbit

Options pour JetSetColumn.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
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
<td>AppendLV</td>
<td>Cette option est utilisée pour ajouter des données à une colonne de type JET_coltypLongText ou JET_coltypLongBinary. Le même comportement peut être obtenu en déterminant la taille de la valeur longue existante et en spécifiant ibLongValue dans psetinfo. Toutefois, il est plus simple d’utiliser ce Grbit dans la mesure où la taille de la valeur de colonne existante n’est pas nécessaire.</td>
</tr>
<tr class="odd">
<td></td>
<td>OverwriteLV</td>
<td>Cette option est utilisée pour remplacer la valeur de type long existante par les données qui viennent d’être fournies. Lorsque cette option est utilisée, c’est comme si la valeur long existante ait été définie à 0 (zéro) avant de définir les nouvelles données.</td>
</tr>
<tr class="even">
<td></td>
<td>RevertToDefaultValue</td>
<td>Cette option s’applique uniquement aux colonnes avec balises, éparses ou à valeurs multiples. Elle fait en sorte que la colonne retourne la valeur de colonne par défaut lors des opérations de récupération de colonne suivantes. Toutes les valeurs de colonnes existantes sont supprimées.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeparateLV</td>
<td>Cette option est utilisée pour forcer une valeur longue, les colonnes de type JET_coltyp. LongText ou JET_coltyp. LongBinary, à stocker séparément du reste des données d’enregistrement. Cela se produit normalement lorsque la taille de la valeur long l’empêche d’être stockée avec les données d’enregistrement restantes. Toutefois, cette option peut être utilisée pour forcer le stockage séparé de la valeur de type long. Notez que les valeurs longues de 4 octets de taille inférieure ne peuvent pas être forcées à être séparées. Dans ce cas, l’option est ignorée.</td>
</tr>
<tr class="even">
<td></td>
<td>SizeLV</td>
<td>Cette option est utilisée pour interpréter la mémoire tampon d’entrée comme un nombre entier d’octets à définir comme longueur de la valeur longue décrite par le ColumnID donné et, le cas échéant, le numéro de séquence dans psetinfo- &gt; itagSequence. Si la taille donnée est supérieure à la valeur de colonne existante, la colonne est étendue avec 0. Si la taille est inférieure à la valeur de colonne existante, la valeur sera tronquée.</td>
</tr>
<tr class="odd">
<td></td>
<td>UniqueMultiValues</td>
<td>Cette option permet d’imposer que toutes les valeurs d’une colonne à valeurs multiples soient distinctes. Cette option compare les données de la colonne source, sans aucune transformation, à d’autres valeurs de colonne existantes et une erreur est retournée si un doublon est trouvé. Si cette option est spécifiée, AppendLV, OverwriteLV et SizeLV ne peuvent pas être spécifiés.</td>
</tr>
<tr class="even">
<td></td>
<td>UniqueNormalizedMultiValues</td>
<td>Cette option permet d’imposer que toutes les valeurs d’une colonne à valeurs multiples soient distinctes. Cette option compare la transformation clé normalisée des données de colonne à d’autres valeurs de colonne existantes transformées de façon similaire, et une erreur est retournée si un doublon est trouvé. Si cette option est spécifiée, AppendLV, OverwriteLV et SizeLV ne peuvent pas être spécifiés.</td>
</tr>
<tr class="odd">
<td></td>
<td>ZeroLength</td>
<td>Cette option est utilisée pour définir une valeur de longueur nulle. Normalement, une valeur de colonne est définie sur NULL en passant un cbMax de 0 (zéro). Toutefois, pour certains types, comme JET_coltyp. Texte, une valeur de colonne peut avoir une longueur de 0 (zéro) au lieu de NULL, et cette option est utilisée pour différencier les valeurs NULL et 0 (zéro).</td>
</tr>
<tr class="even">
<td></td>
<td>IntrinsicLV</td>
<td>Essayez de stocker les colonnes de valeur longue dans l’enregistrement, même si elles dépassent la taille de séparation par défaut.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[Compressed](./windows7grbits.compressed-field.md)

[Non compressé](./windows7grbits.uncompressed-field.md)
