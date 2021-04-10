---
description: 'En savoir plus sur : énumération CreateTableColumnIndexGrbit'
title: Énumération CreateTableColumnIndexGrbit
TOCTitle: CreateTableColumnIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createtablecolumnindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39516657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72f91c5d41b8262e3b2804159914b0a9ccaaaa7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953033"
---
# <a name="createtablecolumnindexgrbit-enumeration"></a>Énumération CreateTableColumnIndexGrbit

Options pour JetCreateTableColumnIndex.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateTableColumnIndexGrbit
'Usage
Dim instance As CreateTableColumnIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateTableColumnIndexGrbit
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
<td>FixedDDL</td>
<td>Le DDL est fixe.</td>
</tr>
<tr class="odd">
<td></td>
<td>TemplateTable</td>
<td>Le DDL peut être hérité. Implique FixedDDL.</td>
</tr>
<tr class="even">
<td></td>
<td>NoFixedVarColumnsInDerivedTables</td>
<td>Utilisé conjointement avec TemplateTable.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
