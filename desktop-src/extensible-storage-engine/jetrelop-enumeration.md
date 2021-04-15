---
description: 'En savoir plus sur : énumération JetRelop'
title: Énumération JetRelop (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JetRelop enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JetRelop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jetrelop(v=EXCHG.10)
ms:contentKeyID: 55104456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7839e0223eb9dd773ca9a5d10b5210b10b0a944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321142"
---
# <a name="jetrelop-enumeration"></a>Énumération JetRelop

Opération de comparaison pour le filtre défini en tant que [JET_INDEX_COLUMN](./jet-index-column-class.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Enumeration JetRelop
'Usage
Dim instance As JetRelop
```

``` csharp
public enum JetRelop
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
<td>Égal à</td>
<td>Accepte uniquement les lignes dont la valeur de colonne est égale à la valeur donnée.</td>
</tr>
<tr class="even">
<td></td>
<td>PrefixEquals</td>
<td>Accepte uniquement les lignes qui ont des colonnes dont le préfixe correspond à la valeur donnée.</td>
</tr>
<tr class="odd">
<td></td>
<td>NotEquals</td>
<td>Accepte uniquement les lignes dont la valeur de colonne n’est pas égale à la valeur donnée.</td>
</tr>
<tr class="even">
<td></td>
<td>LessThanOrEqual</td>
<td>Accepte uniquement les lignes qui ont une valeur de colonne inférieure ou égale à une valeur donnée.</td>
</tr>
<tr class="odd">
<td></td>
<td>LessThan</td>
<td>Accepte uniquement les lignes dont la valeur de colonne est inférieure à une valeur donnée.</td>
</tr>
<tr class="even">
<td></td>
<td>GreaterThanOrEqual</td>
<td>Accepte uniquement les lignes qui ont une valeur de colonne supérieure ou égale à une valeur donnée.</td>
</tr>
<tr class="odd">
<td></td>
<td>GreaterThan</td>
<td>Accepte uniquement les lignes qui ont une valeur de colonne supérieure à une valeur donnée.</td>
</tr>
<tr class="even">
<td></td>
<td>BitmaskEqualsZero</td>
<td>Accepte uniquement les lignes qui ont une valeur de colonne liés avec un masque de données donné qui produit zéro.</td>
</tr>
<tr class="odd">
<td></td>
<td>BitmaskNotEqualsZero</td>
<td>Accepte uniquement les lignes qui ont une valeur de colonne liés avec un masque de bits donné qui donne une valeur différente de zéro.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
