---
description: 'En savoir plus sur : énumération OpenDatabaseGrbit'
title: Énumération OpenDatabaseGrbit
TOCTitle: OpenDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opendatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d14fb779ec02137f6a4fce1cfdd92f46dedcb832
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854116"
---
# <a name="opendatabasegrbit-enumeration"></a>Énumération OpenDatabaseGrbit

Options pour [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenDatabaseGrbit
'Usage
Dim instance As OpenDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenDatabaseGrbit
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
<td>Lecture seule</td>
<td>Empêche toute modification de la base de données.</td>
</tr>
<tr class="odd">
<td></td>
<td>Exclusif</td>
<td>Autorise une seule session à attacher une base de données. En règle générale, plusieurs sessions peuvent ouvrir une base de données.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
