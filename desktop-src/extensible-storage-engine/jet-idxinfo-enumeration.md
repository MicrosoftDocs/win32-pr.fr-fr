---
description: 'En savoir plus sur : énumération JET_IdxInfo'
title: Énumération JET_IdxInfo
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4447e5e1d7a839b27246121145e820a016eba19f4a4e7c88e487c26782bfc607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118075204"
---
# <a name="jet_idxinfo-enumeration"></a>Énumération JET_IdxInfo

Niveaux d’informations pour la récupération des informations d’index avec JetGetIndexInfo. et JetGetTableIndexInfo.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
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
<td>Default</td>
<td>Retourne une structure <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> avec les informations relatives à l’index.</td>
</tr>
<tr class="even">
<td></td>
<td>List</td>
<td>Retourne une structure <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> avec les informations relatives à l’index.</td>
</tr>
<tr class="odd">
<td></td>
<td>SysTabCursor</td>
<td><strong>Obsolète.</strong> SysTabCursor est obsolète.</td>
</tr>
<tr class="even">
<td></td>
<td>OLC</td>
<td><strong>Obsolète.</strong> OLC est obsolète.</td>
</tr>
<tr class="odd">
<td></td>
<td>ResetOLC</td>
<td><strong>Obsolète.</strong> La réinitialisation de OLC est obsolète.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAlloc</td>
<td>Retourne un entier avec l’utilisation de l’espace de l’index.</td>
</tr>
<tr class="odd">
<td></td>
<td>LCID</td>
<td>Retourne un entier avec le LCID de l’index.</td>
</tr>
<tr class="even">
<td></td>
<td>Langid</td>
<td><strong>Obsolète.</strong> Langid est obsolète. Utilisez plutôt LCID.</td>
</tr>
<tr class="odd">
<td></td>
<td>Count</td>
<td>Retourne un entier avec le nombre d’index dans la table.</td>
</tr>
<tr class="even">
<td></td>
<td>VarSegMac</td>
<td>Retourne un UShort avec la valeur de cbVarSegMac avec laquelle l’index a été créé.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexId</td>
<td>Retourne un <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> identifiant l’index.</td>
</tr>
<tr class="even">
<td></td>
<td>La plupart des</td>
<td>introduite dans Windows Vista. Retourne un UShort avec la valeur de cbKeyMost avec laquelle l’index a été créé.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
