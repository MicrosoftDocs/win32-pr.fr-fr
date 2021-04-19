---
description: 'En savoir plus sur : énumération JET_DbInfo'
title: Énumération JET_DbInfo
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516869"
---
# <a name="jet_dbinfo-enumeration"></a>Énumération JET_DbInfo

Niveaux d’informations pour la récupération des informations de base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
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
<td>Nom de fichier</td>
<td>Retourne le chemin d’accès au fichier de base de données (String).</td>
</tr>
<tr class="even">
<td></td>
<td>LCID</td>
<td>Retourne l’identificateur de paramètres régionaux (LCID) associé à cette base de données (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Options</td>
<td>Retourne un <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>. Cela indique si la base de données est ouverte en mode exclusif. Si la base de données est en mode exclusif, alors <a href="hh579532(v=exchg.10).md">exclusive</a> est retourné ; sinon, la valeur zéro est retournée. Les autres options de Grbit de base de données pour JetAttachDatabase et JetOpenDatabase ne sont pas retournées.</td>
</tr>
<tr class="even">
<td></td>
<td>Transactions</td>
<td>Retourne un nombre d’une valeur supérieure au niveau maximal auquel les transactions peuvent être imbriquées. Si <a href="dn292105(v=exchg.10).md">JetBeginTransaction (JET_SESID)</a> est appelé (de manière imbriquée, autrement dit, sur la même session, sans validation ou ROLLBACK) autant de fois que cette valeur, sur le dernier appel, <a href="hh564840(v=exchg.10).md">TransTooDeep</a> est retourné (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Version</td>
<td>Retourne la version principale du moteur de base de données (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>Taille</td>
<td>Retourne la taille de la base de données, en pages (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>SpaceOwned</td>
<td>Retourne l’espace détenu de la base de données, en pages (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceAvailable</td>
<td>Retourne l’espace disponible dans la base de données, en pages (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Divers</td>
<td>Retourne un objet <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> .</td>
</tr>
<tr class="even">
<td></td>
<td>DBInUse</td>
<td>Retourne une valeur booléenne indiquant si la base de données est attachée (booléenne).</td>
</tr>
<tr class="odd">
<td></td>
<td>PageSize</td>
<td>Retourne la taille de page de la base de données (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>FileType</td>
<td>Retourne le type de la base de données (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
