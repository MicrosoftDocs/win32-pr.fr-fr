---
description: 'En savoir plus sur : énumération CompactGrbit'
title: Énumération CompactGrbit
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a85f3298e4127a35acd5a39839f788fc404269f80a07463bde1417dc04f7fe16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976539"
---
# <a name="compactgrbit-enumeration"></a>Énumération CompactGrbit

Options pour [JetCompact (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
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
<td>Statistiques</td>
<td>Fait en sorte que JetCompact vide les statistiques de la base de données source vers un fichier nommé DFRGINFO.TXT. Les statistiques incluent le nom de chaque table dans la base de données source, le nombre de lignes dans chaque table, la taille totale en octets de toutes les lignes de chaque table, la taille totale, en octets, de toutes les colonnes de type <a href="hh577895(v=exchg.10).md">LONGTEXT</a> ou <a href="hh577895(v=exchg.10).md">LONGBINARY</a> qui étaient suffisamment volumineuses pour être stockées séparément de l’enregistrement, le nombre de pages de feuilles d’index cluster et le nombre de pages de En outre, les statistiques récapitulatives, y compris la taille de la base de données source, la base de données de destination, le temps requis pour le compactage de base de données, l’espace temporaire de la base de données sont également vidées.</td>
</tr>
<tr class="odd">
<td></td>
<td>Réparation</td>
<td><strong>Obsolète.</strong> Utilisé lorsque la base de données source est endommagée. Il active un ensemble complet de nouveaux comportements destinés à récupérer autant de données que possible à partir de la base de données source. JetCompact avec ce groupe d’options peut retourner une <a href="hh564840(v=exchg.10).md">réussite</a> , mais ne pas copier toutes les données créées dans la base de données source. Les données qui étaient dans des parties endommagées de la base de données source seront ignorées.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
