---
description: 'En savoir plus sur : énumération PrereadIndexRangesGrbit'
title: Énumération PrereadIndexRangesGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: PrereadIndexRangesGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.prereadindexrangesgrbit(v=EXCHG.10)
ms:contentKeyID: 55104328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4bc1b9877d4548a68aa71ea4def536af09d9693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534303"
---
# <a name="prereadindexrangesgrbit-enumeration"></a>Énumération PrereadIndexRangesGrbit

Options pour [JetPrereadIndexRanges (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, Int32, \[ \] , PrereadIndexRangesGrbit)](./windows8api.jetprereadindexranges-method.md).

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration PrereadIndexRangesGrbit
'Usage
Dim instance As PrereadIndexRangesGrbit
```

``` csharp
[FlagsAttribute]
public enum PrereadIndexRangesGrbit
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
<td>Transférer</td>
<td>Lecture anticipée.</td>
</tr>
<tr class="even">
<td></td>
<td>Vers l'arrière</td>
<td>Lire en arrière.</td>
</tr>
<tr class="odd">
<td></td>
<td>FirstPageOnly</td>
<td>Prélecture seule de la première page d’une colonne longue.</td>
</tr>
<tr class="even">
<td></td>
<td>NormalizedKey</td>
<td>Clé/signet normalisé fourni à la place de la valeur de colonne.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
