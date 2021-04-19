---
description: 'En savoir plus sur : énumération JET_TblInfo'
title: Énumération JET_TblInfo
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524275"
---
# <a name="jet_tblinfo-enumeration"></a><span data-ttu-id="f8532-103">Énumération JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="f8532-103">JET_TblInfo enumeration</span></span>

<span data-ttu-id="f8532-104">Niveaux d’informations pour la récupération des informations de table avec JetGetTableInfo.</span><span class="sxs-lookup"><span data-stu-id="f8532-104">Info levels for retrieving table info with JetGetTableInfo.</span></span>

<span data-ttu-id="f8532-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8532-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8532-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8532-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8532-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8532-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
```

## <a name="members"></a><span data-ttu-id="f8532-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f8532-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f8532-109">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="f8532-109">Member name</span></span></th>
<th><span data-ttu-id="f8532-110">Description</span><span class="sxs-lookup"><span data-stu-id="f8532-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f8532-111">Default</span><span class="sxs-lookup"><span data-stu-id="f8532-111">Default</span></span></td>
<td><span data-ttu-id="f8532-112">Option par défaut.</span><span class="sxs-lookup"><span data-stu-id="f8532-112">Default option.</span></span> <span data-ttu-id="f8532-113">Récupère un <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> contenant des informations sur la table.</span><span class="sxs-lookup"><span data-stu-id="f8532-113">Retrieves a <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> containing information about the table.</span></span> <span data-ttu-id="f8532-114">Utilisez cette option avec <a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="f8532-114">Use this option with <a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f8532-115">Nom</span><span class="sxs-lookup"><span data-stu-id="f8532-115">Name</span></span></td>
<td><span data-ttu-id="f8532-116">Récupère le nom de la table.</span><span class="sxs-lookup"><span data-stu-id="f8532-116">Retrieves the name of the table.</span></span> <span data-ttu-id="f8532-117">Utilisez cette option avec <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="f8532-117">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f8532-118">Dbid</span><span class="sxs-lookup"><span data-stu-id="f8532-118">Dbid</span></span></td>
<td><span data-ttu-id="f8532-119">Récupère le <a href="hh596176(v=exchg.10).md">JET_DBID</a> de la base de données contenant la table.</span><span class="sxs-lookup"><span data-stu-id="f8532-119">Retrieves the <a href="hh596176(v=exchg.10).md">JET_DBID</a> of the database containing the table.</span></span> <span data-ttu-id="f8532-120">Utilisez cette option avec <a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="f8532-120">Use this option with <a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f8532-121">SpaceUsage</span><span class="sxs-lookup"><span data-stu-id="f8532-121">SpaceUsage</span></span></td>
<td><span data-ttu-id="f8532-122">Le comportement de la méthode dépend de la taille du tableau qui est passé à la méthode.</span><span class="sxs-lookup"><span data-stu-id="f8532-122">The behavior of the method depends on how large the array that is passed to the method is.</span></span> <span data-ttu-id="f8532-123">Le tableau doit avoir au moins deux entrées.</span><span class="sxs-lookup"><span data-stu-id="f8532-123">The array must have at least two entries.</span></span> <span data-ttu-id="f8532-124">La première entrée contient le nombre d’étendues appartenant à la table.</span><span class="sxs-lookup"><span data-stu-id="f8532-124">The first entry will contain the number of Owned Extents in the table.</span></span> <span data-ttu-id="f8532-125">La deuxième entrée contient le nombre d’étendues disponibles dans la table.</span><span class="sxs-lookup"><span data-stu-id="f8532-125">The second entry will contain the number of Available Extents in the table.</span></span> <span data-ttu-id="f8532-126">Si le tableau contient plus de deux entrées, les octets restants de la mémoire tampon se composent d’un tableau de structures qui représentent une liste d’étendues.</span><span class="sxs-lookup"><span data-stu-id="f8532-126">If the array has more than two entries then the remaining bytes of the buffer will consist of an array of structures that represent a list of extents.</span></span> <span data-ttu-id="f8532-127">Cette structure contient deux membres : le dernier numéro de page dans l’étendue et le nombre de pages dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="f8532-127">This structure contains two members: the last page number in the extent and the number of pages in the extent.</span></span> <span data-ttu-id="f8532-128">Utilisez cette option avec <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="f8532-128">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f8532-129">SpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="f8532-129">SpaceAlloc</span></span></td>
<td><span data-ttu-id="f8532-130">Le tableau passé à JetGetTableInfo doit avoir deux entrées.</span><span class="sxs-lookup"><span data-stu-id="f8532-130">The array passed to JetGetTableInfo must have two entries.</span></span> <span data-ttu-id="f8532-131">La première entrée sera définie sur le nombre de pages dans la table.</span><span class="sxs-lookup"><span data-stu-id="f8532-131">The first entry will be set to the number of pages in the table.</span></span> <span data-ttu-id="f8532-132">La deuxième entrée sera définie sur la densité cible des pages de la table.</span><span class="sxs-lookup"><span data-stu-id="f8532-132">The second entry will be set to the target density of pages for the table.</span></span> <span data-ttu-id="f8532-133">Utilisez cette option avec <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="f8532-133">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f8532-134">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="f8532-134">SpaceOwned</span></span></td>
<td><span data-ttu-id="f8532-135">Obtient le nombre de pages appartenant à la table.</span><span class="sxs-lookup"><span data-stu-id="f8532-135">Gets the number of owned pages in the table.</span></span> <span data-ttu-id="f8532-136">Utilisez cette option avec <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="f8532-136">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f8532-137">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="f8532-137">SpaceAvailable</span></span></td>
<td><span data-ttu-id="f8532-138">Obtient le nombre de pages disponibles dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f8532-138">Gets the number of available pages in the table.</span></span> <span data-ttu-id="f8532-139">Utilisez cette option avec <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="f8532-139">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f8532-140">TemplateTableName</span><span class="sxs-lookup"><span data-stu-id="f8532-140">TemplateTableName</span></span></td>
<td><span data-ttu-id="f8532-141">Si la table est une table dérivée, le résultat est renseigné avec le nom de la table à partir de laquelle la table dérivée a hérité son DDL.</span><span class="sxs-lookup"><span data-stu-id="f8532-141">If the table is a derived table, the result will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="f8532-142">Si la table n’est pas une table dérivée, la mémoire tampon est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="f8532-142">If the table is not a derived table, the buffer will an empty string.</span></span> <span data-ttu-id="f8532-143">Utilisez cette option avec <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="f8532-143">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f8532-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8532-144">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8532-145">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f8532-145">Reference</span></span>

[<span data-ttu-id="f8532-146">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f8532-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
