---
description: 'En savoir plus sur : énumération CreateIndexGrbit'
title: Énumération CreateIndexGrbit
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536661"
---
# <a name="createindexgrbit-enumeration"></a><span data-ttu-id="952cf-103">Énumération CreateIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="952cf-103">CreateIndexGrbit enumeration</span></span>

<span data-ttu-id="952cf-104">Options pour JetCreateIndex.</span><span class="sxs-lookup"><span data-stu-id="952cf-104">Options for JetCreateIndex.</span></span>

<span data-ttu-id="952cf-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="952cf-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="952cf-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="952cf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="952cf-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="952cf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="952cf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="952cf-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
```

## <a name="members"></a><span data-ttu-id="952cf-109">Membres</span><span class="sxs-lookup"><span data-stu-id="952cf-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="952cf-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="952cf-110">Member name</span></span></th>
<th><span data-ttu-id="952cf-111">Description</span><span class="sxs-lookup"><span data-stu-id="952cf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="952cf-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="952cf-112">None</span></span></td>
<td><span data-ttu-id="952cf-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="952cf-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="952cf-114">IndexUnique</span><span class="sxs-lookup"><span data-stu-id="952cf-114">IndexUnique</span></span></td>
<td><span data-ttu-id="952cf-115">Les entrées d’index en double (clés) ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="952cf-115">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="952cf-116">Cette méthode est appliquée quand JetUpdate est appelé, et non lorsque JetSetColumn est appelé.</span><span class="sxs-lookup"><span data-stu-id="952cf-116">This is enforced when JetUpdate is called, not when JetSetColumn is called.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="952cf-117">IndexPrimary</span><span class="sxs-lookup"><span data-stu-id="952cf-117">IndexPrimary</span></span></td>
<td><span data-ttu-id="952cf-118">L’index est un index principal (cluster).</span><span class="sxs-lookup"><span data-stu-id="952cf-118">The index is a primary (clustered) index.</span></span> <span data-ttu-id="952cf-119">Chaque table doit avoir un seul index primaire.</span><span class="sxs-lookup"><span data-stu-id="952cf-119">Every table must have exactly one primary index.</span></span> <span data-ttu-id="952cf-120">Si aucun index primaire n’est défini explicitement sur une table, le moteur de base de données crée son propre index primaire.</span><span class="sxs-lookup"><span data-stu-id="952cf-120">If no primary index is explicitly defined over a table, then the database engine will create its own primary index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="952cf-121">IndexDisallowNull</span><span class="sxs-lookup"><span data-stu-id="952cf-121">IndexDisallowNull</span></span></td>
<td><span data-ttu-id="952cf-122">Aucune des colonnes sur lesquelles l’index est créé ne peut contenir une valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="952cf-122">None of the columns over which the index is created may contain a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="952cf-123">IndexIgnoreNull</span><span class="sxs-lookup"><span data-stu-id="952cf-123">IndexIgnoreNull</span></span></td>
<td><span data-ttu-id="952cf-124">N’ajoutez pas d’entrée d’index pour une ligne si toutes les colonnes indexées ont la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="952cf-124">Do not add an index entry for a row if all of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="952cf-125">IndexIgnoreAnyNull</span><span class="sxs-lookup"><span data-stu-id="952cf-125">IndexIgnoreAnyNull</span></span></td>
<td><span data-ttu-id="952cf-126">N’ajoutez pas d’entrée d’index pour une ligne si l’une des colonnes indexées a la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="952cf-126">Do not add an index entry for a row if any of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="952cf-127">IndexIgnoreFirstNull</span><span class="sxs-lookup"><span data-stu-id="952cf-127">IndexIgnoreFirstNull</span></span></td>
<td><span data-ttu-id="952cf-128">N’ajoutez pas d’entrée d’index pour une ligne si la première colonne indexée a la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="952cf-128">Do not add an index entry for a row if the first column being indexed is NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="952cf-129">IndexLazyFlush</span><span class="sxs-lookup"><span data-stu-id="952cf-129">IndexLazyFlush</span></span></td>
<td><span data-ttu-id="952cf-130">Spécifie que les opérations d’index seront journalisées tardivement.</span><span class="sxs-lookup"><span data-stu-id="952cf-130">Specifies that the index operations will be logged lazily.</span></span> <span data-ttu-id="952cf-131">JET_bitIndexLazyFlush n’affecte pas le paresse des mises à jour de données.</span><span class="sxs-lookup"><span data-stu-id="952cf-131">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="952cf-132">Si les opérations d’indexation sont interrompues par l’arrêt du processus, la récupération logicielle peut toujours être en mesure d’obtenir la base de données à un état cohérent, mais l’index n’est peut-être pas présent.</span><span class="sxs-lookup"><span data-stu-id="952cf-132">If the indexing operations is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="952cf-133">IndexEmpty</span><span class="sxs-lookup"><span data-stu-id="952cf-133">IndexEmpty</span></span></td>
<td><span data-ttu-id="952cf-134">N’essayez pas de créer l’index, car toutes les entrées ont la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="952cf-134">Do not attempt to build the index, because all entries would evaluate to NULL.</span></span> <span data-ttu-id="952cf-135">Grbit doit également spécifier JET_bitIgnoreAnyNull lorsque JET_bitIndexEmpty est passé.</span><span class="sxs-lookup"><span data-stu-id="952cf-135">grbit MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="952cf-136">Il s’agit d’une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="952cf-136">This is a performance enhancement.</span></span> <span data-ttu-id="952cf-137">Par exemple, si une nouvelle colonne est ajoutée à une table, un index est créé sur cette colonne nouvellement ajoutée, tous les enregistrements de la table sont analysés même s’ils ne sont jamais ajoutés à l’index.</span><span class="sxs-lookup"><span data-stu-id="952cf-137">For example if a new column is added to a table, then an index is created over this newly added column, all of the records in the table would be scanned even though they would never get added to the index anyway.</span></span> <span data-ttu-id="952cf-138">La spécification de JET_bitIndexEmpty ignore l’analyse de la table, ce qui peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="952cf-138">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="952cf-139">IndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="952cf-139">IndexUnversioned</span></span></td>
<td><span data-ttu-id="952cf-140">Rend la création d’index visible pour les autres transactions.</span><span class="sxs-lookup"><span data-stu-id="952cf-140">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="952cf-141">Normalement, une session dans une transaction ne peut pas voir une opération de création d’index dans une autre session.</span><span class="sxs-lookup"><span data-stu-id="952cf-141">Normally a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="952cf-142">Cet indicateur peut être utile si une autre transaction est susceptible de créer le même index, de sorte que la deuxième index-Create échoue simplement au lieu de provoquer potentiellement des opérations de base de données inutiles.</span><span class="sxs-lookup"><span data-stu-id="952cf-142">This flag can be useful if another transaction is likely to create the same index, so that the second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="952cf-143">La deuxième transaction peut ne pas être en mesure d’utiliser l’index immédiatement.</span><span class="sxs-lookup"><span data-stu-id="952cf-143">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="952cf-144">L’opération de création d’index doit être terminée pour pouvoir être utilisée.</span><span class="sxs-lookup"><span data-stu-id="952cf-144">The index creation operation needs to complete before it is usable.</span></span> <span data-ttu-id="952cf-145">La session ne doit pas être actuellement dans une transaction pour créer un index sans informations de version.</span><span class="sxs-lookup"><span data-stu-id="952cf-145">The session must not currently be in a transaction to create an index without version information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="952cf-146">IndexSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="952cf-146">IndexSortNullsHigh</span></span></td>
<td><span data-ttu-id="952cf-147">Si vous spécifiez cet indicateur, les valeurs NULL sont triées après les données de toutes les colonnes de l’index.</span><span class="sxs-lookup"><span data-stu-id="952cf-147">Specifying this flag causes NULL values to be sorted after data for all columns in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="952cf-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="952cf-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="952cf-149">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="952cf-149">Reference</span></span>

[<span data-ttu-id="952cf-150">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="952cf-150">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
