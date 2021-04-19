---
description: 'En savoir plus sur : énumération JET_coltyp'
title: Énumération JET_coltyp
TOCTitle: JET_coltyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_coltyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_coltyp(v=EXCHG.10)
ms:contentKeyID: 39511169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 616dc80d835e22502b6781355a2eff35a6375e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522181"
---
# <a name="jet_coltyp-enumeration"></a>Énumération JET_coltyp

Types de colonne ESENT.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Enumeration JET_coltyp
'Usage
Dim instance As JET_coltyp
```

``` csharp
public enum JET_coltyp
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
<td>Pli</td>
<td>Type de colonne null. Non valide pour la création de colonne.</td>
</tr>
<tr class="even">
<td></td>
<td>bit</td>
<td>True, false ou NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>UnsignedByte</td>
<td>entier sur 1 octet, non signé.</td>
</tr>
<tr class="even">
<td></td>
<td>Court</td>
<td>entier sur 2 octets, signé.</td>
</tr>
<tr class="odd">
<td></td>
<td>Long</td>
<td>entier sur 4 octets, signé.</td>
</tr>
<tr class="even">
<td></td>
<td>Devise</td>
<td>entier sur 8 octets, signé.</td>
</tr>
<tr class="odd">
<td></td>
<td>IEEESingle</td>
<td>uniprécisions IEEE sur 4 octets.</td>
</tr>
<tr class="even">
<td></td>
<td>IEEEDouble</td>
<td>double précision IEEE sur 8 octets.</td>
</tr>
<tr class="odd">
<td></td>
<td>DateTime</td>
<td>Date entière, temps fractionnaire.</td>
</tr>
<tr class="even">
<td></td>
<td>Binary</td>
<td>Données binaires, jusqu’à 255 octets.</td>
</tr>
<tr class="odd">
<td></td>
<td>Texte</td>
<td>Données texte, jusqu’à 255 octets.</td>
</tr>
<tr class="even">
<td></td>
<td>LongBinary</td>
<td>Données binaires, jusqu’à 2 Go.</td>
</tr>
<tr class="odd">
<td></td>
<td>LongText</td>
<td>Données texte, jusqu’à 2 Go.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
