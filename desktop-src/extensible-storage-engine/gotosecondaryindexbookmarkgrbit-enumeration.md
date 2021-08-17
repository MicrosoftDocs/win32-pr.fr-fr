---
description: 'En savoir plus sur : énumération GotoSecondaryIndexBookmarkGrbit'
title: Énumération GotoSecondaryIndexBookmarkGrbit
TOCTitle: GotoSecondaryIndexBookmarkGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.gotosecondaryindexbookmarkgrbit(v=EXCHG.10)
ms:contentKeyID: 39515224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.BookmarkPermitVirtualCurrency
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit
- Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 733647a8cf53fa93c9779674890005de4ead1aa57f15853c255c5ac5a8e13904
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487979"
---
# <a name="gotosecondaryindexbookmarkgrbit-enumeration"></a>Énumération GotoSecondaryIndexBookmarkGrbit

Options pour [JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GotoSecondaryIndexBookmarkGrbit)](./api.jetgotosecondaryindexbookmark-method.md).

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GotoSecondaryIndexBookmarkGrbit
'Usage
Dim instance As GotoSecondaryIndexBookmarkGrbit
```

``` csharp
[FlagsAttribute]
public enum GotoSecondaryIndexBookmarkGrbit
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
<td>BookmarkPermitVirtualCurrency</td>
<td>Dans le cas où l’entrée d’index ne peut plus être trouvée, le curseur est placé à gauche de l’emplacement où cette entrée d’index a été trouvée précédemment. L’opération échouera toujours avec JET_errRecordDeleted ; Toutefois, il est possible de passer à l’entrée d’index suivante ou précédente relative à l’entrée d’index manquante.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
