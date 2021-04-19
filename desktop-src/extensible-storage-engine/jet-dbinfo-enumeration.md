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
# <a name="jet_dbinfo-enumeration"></a><span data-ttu-id="ce830-103">Énumération JET_DbInfo</span><span class="sxs-lookup"><span data-stu-id="ce830-103">JET_DbInfo enumeration</span></span>

<span data-ttu-id="ce830-104">Niveaux d’informations pour la récupération des informations de base de données.</span><span class="sxs-lookup"><span data-stu-id="ce830-104">Info levels for retrieving database info.</span></span>

<span data-ttu-id="ce830-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ce830-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ce830-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ce830-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ce830-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce830-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a><span data-ttu-id="ce830-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ce830-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ce830-109">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="ce830-109">Member name</span></span></th>
<th><span data-ttu-id="ce830-110">Description</span><span class="sxs-lookup"><span data-stu-id="ce830-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ce830-111">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="ce830-111">Filename</span></span></td>
<td><span data-ttu-id="ce830-112">Retourne le chemin d’accès au fichier de base de données (String).</span><span class="sxs-lookup"><span data-stu-id="ce830-112">Returns the path to the database file (string).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ce830-113">LCID</span><span class="sxs-lookup"><span data-stu-id="ce830-113">LCID</span></span></td>
<td><span data-ttu-id="ce830-114">Retourne l’identificateur de paramètres régionaux (LCID) associé à cette base de données (Int32).</span><span class="sxs-lookup"><span data-stu-id="ce830-114">Returns the locale identifier (LCID) associated with this database (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ce830-115">Options</span><span class="sxs-lookup"><span data-stu-id="ce830-115">Options</span></span></td>
<td><span data-ttu-id="ce830-116">Retourne un <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="ce830-116">Returns a <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span></span> <span data-ttu-id="ce830-117">Cela indique si la base de données est ouverte en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="ce830-117">This indicates whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="ce830-118">Si la base de données est en mode exclusif, alors <a href="hh579532(v=exchg.10).md">exclusive</a> est retourné ; sinon, la valeur zéro est retournée.</span><span class="sxs-lookup"><span data-stu-id="ce830-118">If the database is in exclusive mode then <a href="hh579532(v=exchg.10).md">Exclusive</a> will be returned, otherwise zero is returned.</span></span> <span data-ttu-id="ce830-119">Les autres options de Grbit de base de données pour JetAttachDatabase et JetOpenDatabase ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="ce830-119">Other database grbit options for JetAttachDatabase and JetOpenDatabase are not returned.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ce830-120">Transactions</span><span class="sxs-lookup"><span data-stu-id="ce830-120">Transactions</span></span></td>
<td><span data-ttu-id="ce830-121">Retourne un nombre d’une valeur supérieure au niveau maximal auquel les transactions peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="ce830-121">Returns a number one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="ce830-122">Si <a href="dn292105(v=exchg.10).md">JetBeginTransaction (JET_SESID)</a> est appelé (de manière imbriquée, autrement dit, sur la même session, sans validation ou ROLLBACK) autant de fois que cette valeur, sur le dernier appel, <a href="hh564840(v=exchg.10).md">TransTooDeep</a> est retourné (Int32).</span><span class="sxs-lookup"><span data-stu-id="ce830-122">If <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call <a href="hh564840(v=exchg.10).md">TransTooDeep</a> will be returned (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ce830-123">Version</span><span class="sxs-lookup"><span data-stu-id="ce830-123">Version</span></span></td>
<td><span data-ttu-id="ce830-124">Retourne la version principale du moteur de base de données (Int32).</span><span class="sxs-lookup"><span data-stu-id="ce830-124">Returns the major version of the database engine (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ce830-125">Taille</span><span class="sxs-lookup"><span data-stu-id="ce830-125">Filesize</span></span></td>
<td><span data-ttu-id="ce830-126">Retourne la taille de la base de données, en pages (Int32).</span><span class="sxs-lookup"><span data-stu-id="ce830-126">Returns the filesize of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ce830-127">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="ce830-127">SpaceOwned</span></span></td>
<td><span data-ttu-id="ce830-128">Retourne l’espace détenu de la base de données, en pages (Int32).</span><span class="sxs-lookup"><span data-stu-id="ce830-128">Returns the owned space of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ce830-129">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="ce830-129">SpaceAvailable</span></span></td>
<td><span data-ttu-id="ce830-130">Retourne l’espace disponible dans la base de données, en pages (Int32).</span><span class="sxs-lookup"><span data-stu-id="ce830-130">Returns the available space in the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ce830-131">Divers</span><span class="sxs-lookup"><span data-stu-id="ce830-131">Misc</span></span></td>
<td><span data-ttu-id="ce830-132">Retourne un objet <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> .</span><span class="sxs-lookup"><span data-stu-id="ce830-132">Returns a <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> object.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ce830-133">DBInUse</span><span class="sxs-lookup"><span data-stu-id="ce830-133">DBInUse</span></span></td>
<td><span data-ttu-id="ce830-134">Retourne une valeur booléenne indiquant si la base de données est attachée (booléenne).</span><span class="sxs-lookup"><span data-stu-id="ce830-134">Returns a boolean indicating whether the database is attached (boolean).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ce830-135">PageSize</span><span class="sxs-lookup"><span data-stu-id="ce830-135">PageSize</span></span></td>
<td><span data-ttu-id="ce830-136">Retourne la taille de page de la base de données (Int32).</span><span class="sxs-lookup"><span data-stu-id="ce830-136">Returns the page size of the database (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ce830-137">FileType</span><span class="sxs-lookup"><span data-stu-id="ce830-137">FileType</span></span></td>
<td><span data-ttu-id="ce830-138">Retourne le type de la base de données (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span><span class="sxs-lookup"><span data-stu-id="ce830-138">Returns the type of the database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ce830-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce830-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ce830-140">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ce830-140">Reference</span></span>

[<span data-ttu-id="ce830-141">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ce830-141">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
