---
description: 'En savoir plus sur : énumération MakeKeyGrbit'
title: Énumération MakeKeyGrbit
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112510"
---
# <a name="makekeygrbit-enumeration"></a>Énumération MakeKeyGrbit

Options pour JetMakeKey.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
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
<td>Aucune</td>
<td>Options par défaut.</td>
</tr>
<tr class="even">
<td></td>
<td>NewKey</td>
<td>Une nouvelle clé de recherche doit être construite. Toute clé de recherche existante est ignorée.</td>
</tr>
<tr class="odd">
<td></td>
<td>NormalizedKey</td>
<td>Quand cette option est spécifiée, toutes les autres options sont ignorées, toute clé de recherche précédemment existante est ignorée et le contenu de la mémoire tampon d’entrée est chargé en tant que nouvelle clé de recherche.</td>
</tr>
<tr class="even">
<td></td>
<td>KeyDataZeroLength</td>
<td>Si la taille de la mémoire tampon d’entrée est égale à zéro et que la colonne clé actuelle est une colonne de longueur variable, cette option indique que la mémoire tampon d’entrée contient une valeur de longueur égale à zéro. Dans le cas contraire, une taille de mémoire tampon d’entrée égale à zéro indiquerait une valeur NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>StrLimit</td>
<td>Cette option indique que la clé de recherche doit être construite de telle sorte que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</td>
</tr>
<tr class="even">
<td></td>
<td>SubStrLimit</td>
<td>Cette option indique que la clé de recherche doit être construite de manière à ce que la colonne clé actuelle soit considérée comme un caractère générique de préfixe et que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</td>
</tr>
<tr class="odd">
<td></td>
<td>FullColumnStartLimit</td>
<td>La clé de recherche doit être construite de telle sorte que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</td>
</tr>
<tr class="even">
<td></td>
<td>FullColumnEndLimit</td>
<td>La clé de recherche doit être construite de telle sorte que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</td>
</tr>
<tr class="odd">
<td></td>
<td>PartialColumnStartLimit</td>
<td>La clé de recherche doit être construite de telle sorte que la colonne clé actuelle soit considérée comme un caractère générique de préfixe et que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</td>
</tr>
<tr class="even">
<td></td>
<td>PartialColumnEndLimit</td>
<td>La clé de recherche doit être construite de telle sorte que la colonne clé actuelle soit considérée comme un caractère générique de préfixe et que toutes les colonnes clés qui viennent après la colonne clé actuelle soient considérées comme des caractères génériques.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
