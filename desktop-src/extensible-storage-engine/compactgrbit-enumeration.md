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
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534379"
---
# <a name="compactgrbit-enumeration"></a><span data-ttu-id="f7cd6-103">Énumération CompactGrbit</span><span class="sxs-lookup"><span data-stu-id="f7cd6-103">CompactGrbit enumeration</span></span>

<span data-ttu-id="f7cd6-104">Options pour [JetCompact (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span><span class="sxs-lookup"><span data-stu-id="f7cd6-104">Options for [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span></span>

<span data-ttu-id="f7cd6-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="f7cd6-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f7cd6-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f7cd6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f7cd6-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f7cd6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7cd6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7cd6-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f7cd6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f7cd6-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f7cd6-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="f7cd6-110">Member name</span></span></th>
<th><span data-ttu-id="f7cd6-111">Description</span><span class="sxs-lookup"><span data-stu-id="f7cd6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f7cd6-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="f7cd6-112">None</span></span></td>
<td><span data-ttu-id="f7cd6-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="f7cd6-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f7cd6-114">Statistiques</span><span class="sxs-lookup"><span data-stu-id="f7cd6-114">Stats</span></span></td>
<td><span data-ttu-id="f7cd6-115">Fait en sorte que JetCompact vide les statistiques de la base de données source vers un fichier nommé DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="f7cd6-115">Causes JetCompact to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="f7cd6-116">Les statistiques incluent le nom de chaque table dans la base de données source, le nombre de lignes dans chaque table, la taille totale en octets de toutes les lignes de chaque table, la taille totale, en octets, de toutes les colonnes de type <a href="hh577895(v=exchg.10).md">LONGTEXT</a> ou <a href="hh577895(v=exchg.10).md">LONGBINARY</a> qui étaient suffisamment volumineuses pour être stockées séparément de l’enregistrement, le nombre de pages de feuilles d’index cluster et le nombre de pages de</span><span class="sxs-lookup"><span data-stu-id="f7cd6-116">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="hh577895(v=exchg.10).md">LongText</a> or <a href="hh577895(v=exchg.10).md">LongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="f7cd6-117">En outre, les statistiques récapitulatives, y compris la taille de la base de données source, la base de données de destination, le temps requis pour le compactage de base de données, l’espace temporaire de la base de données sont également vidées.</span><span class="sxs-lookup"><span data-stu-id="f7cd6-117">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f7cd6-118">Réparation</span><span class="sxs-lookup"><span data-stu-id="f7cd6-118">Repair</span></span></td>
<td><span data-ttu-id="f7cd6-119"><strong>Obsolète.</strong></span><span class="sxs-lookup"><span data-stu-id="f7cd6-119"><strong>Obsolete.</strong></span></span> <span data-ttu-id="f7cd6-120">Utilisé lorsque la base de données source est endommagée.</span><span class="sxs-lookup"><span data-stu-id="f7cd6-120">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="f7cd6-121">Il active un ensemble complet de nouveaux comportements destinés à récupérer autant de données que possible à partir de la base de données source.</span><span class="sxs-lookup"><span data-stu-id="f7cd6-121">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="f7cd6-122">JetCompact avec ce groupe d’options peut retourner une <a href="hh564840(v=exchg.10).md">réussite</a> , mais ne pas copier toutes les données créées dans la base de données source.</span><span class="sxs-lookup"><span data-stu-id="f7cd6-122">JetCompact with this option set may return <a href="hh564840(v=exchg.10).md">Success</a> but not copy all of the data created in the source database.</span></span> <span data-ttu-id="f7cd6-123">Les données qui étaient dans des parties endommagées de la base de données source seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="f7cd6-123">Data that was in damaged portions of the source database will be skipped.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f7cd6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7cd6-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7cd6-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f7cd6-125">Reference</span></span>

[<span data-ttu-id="f7cd6-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f7cd6-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
