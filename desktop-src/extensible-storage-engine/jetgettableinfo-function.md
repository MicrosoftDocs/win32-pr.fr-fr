---
description: 'En savoir plus sur : fonction JetGetTableInfo'
title: Fonction JetGetTableInfo
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3362b5da8c6a79d78782e37920b9761b9888b15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952928"
---
# <a name="jetgettableinfo-function"></a><span data-ttu-id="5fe7b-103">Fonction JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="5fe7b-103">JetGetTableInfo Function</span></span>


<span data-ttu-id="5fe7b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="5fe7b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableinfo-function"></a><span data-ttu-id="5fe7b-105">Fonction JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="5fe7b-105">JetGetTableInfo Function</span></span>

<span data-ttu-id="5fe7b-106">La fonction **JetGetTableInfo** récupère différents éléments d’informations sur une table dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-106">The **JetGetTableInfo** function retrieves various pieces of information about a table in a database.</span></span>

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="5fe7b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fe7b-107">Parameters</span></span>

<span data-ttu-id="5fe7b-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5fe7b-108">*sesid*</span></span>

<span data-ttu-id="5fe7b-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="5fe7b-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="5fe7b-110">*tableid*</span></span>

<span data-ttu-id="5fe7b-111">Table à laquelle les informations s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-111">The table that the information applies to.</span></span>

<span data-ttu-id="5fe7b-112">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="5fe7b-112">*pvResult*</span></span>

<span data-ttu-id="5fe7b-113">Pointeur vers une mémoire tampon qui recevra les informations.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-113">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="5fe7b-114">Le type de la mémoire tampon dépend de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-114">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="5fe7b-115">Il incombe à l’appelant d’aligner la mémoire tampon en conséquence.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-115">It is the responsibility of the caller to align the buffer appropriately.</span></span>

<span data-ttu-id="5fe7b-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="5fe7b-116">*cbMax*</span></span>

<span data-ttu-id="5fe7b-117">Taille, en octets, de la mémoire tampon qui a été passée dans *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-117">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="5fe7b-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="5fe7b-118">*InfoLevel*</span></span>

<span data-ttu-id="5fe7b-119">Type d’information qui sera récupéré pour la table spécifiée par *TableID*.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-119">The type of information that will be retrieved for the table that is specified by *tableid*.</span></span> <span data-ttu-id="5fe7b-120">Le format des données stockées dans *pvResult* dépend de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-120">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="5fe7b-121">Les options suivantes peuvent être définies pour ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="5fe7b-121">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fe7b-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fe7b-122">Value</span></span></p></th>
<th><p><span data-ttu-id="5fe7b-123">Signification</span><span class="sxs-lookup"><span data-stu-id="5fe7b-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-124">JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="5fe7b-124">JET_TblInfo</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-125"><em>pvResult</em> est interprété comme une structure de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="5fe7b-125"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span> <span data-ttu-id="5fe7b-126">Si la méthode est réussie, la structure <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> est renseignée avec les données appropriées.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-126">If the method succeeds, the <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is filled in with the appropriate data.</span></span> <span data-ttu-id="5fe7b-127">En cas d’échec, le contenu n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-127">If it fails, the contents are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-128">JET_TblInfoDbid</span><span class="sxs-lookup"><span data-stu-id="5fe7b-128">JET_TblInfoDbid</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-129"><em>pvResult</em> est traité comme un tableau de deux objets <a href="gg269248(v=exchg.10).md">JET_DBID</a> .</span><span class="sxs-lookup"><span data-stu-id="5fe7b-129"><em>pvResult</em> is treated as an array of two <a href="gg269248(v=exchg.10).md">JET_DBID</a> objects.</span></span> <span data-ttu-id="5fe7b-130">L’identificateur de base de données de la base de données qui possède la table est stocké à deux reprises dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-130">The database identifier of the database that owns the table is stored in this array twice.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-131">JET_TblInfoDumpTable</span><span class="sxs-lookup"><span data-stu-id="5fe7b-131">JET_TblInfoDumpTable</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-132">JET_TblInfoDumpTable est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-132">JET_TblInfoDumpTable is deprecated.</span></span> <span data-ttu-id="5fe7b-133">L’API retourne JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-133">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-134">JET_TblInfoName</span><span class="sxs-lookup"><span data-stu-id="5fe7b-134">JET_TblInfoName</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-135">JET_TblInfoName récupère le nom de la table et le stocke dans <em>pvResult</em>.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-135">JET_TblInfoName retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="5fe7b-136">Si la mémoire tampon est trop petite, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-136">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-137">JET_TblInfoMostMany</span><span class="sxs-lookup"><span data-stu-id="5fe7b-137">JET_TblInfoMostMany</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-138">JET_TblInfoMostMany récupère le nom de la table et le stocke dans <em>pvResult</em>.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-138">JET_TblInfoMostMany retrieves the name of the table and stores it in <em>pvResult</em>.</span></span> <span data-ttu-id="5fe7b-139">Si la mémoire tampon est trop petite, le comportement n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-139">If the buffer is too small, the behavior is undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-140">JET_TblInfoOLC</span><span class="sxs-lookup"><span data-stu-id="5fe7b-140">JET_TblInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-141">JET_TblInfoOLC est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-141">JET_TblInfoOLC is deprecated.</span></span> <span data-ttu-id="5fe7b-142">L’API retourne JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-142">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-143">JET_TblInfoRvt</span><span class="sxs-lookup"><span data-stu-id="5fe7b-143">JET_TblInfoRvt</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-144">JET_TblInfoRvt est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-144">JET_TblInfoRvt is deprecated.</span></span> <span data-ttu-id="5fe7b-145">L’API retourne JET_errQueryNotSupported.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-145">The API will return JET_errQueryNotSupported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-146">JET_TblInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="5fe7b-146">JET_TblInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-147">JET_TblInfoResetOLC est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-147">JET_TblInfoResetOLC is deprecated.</span></span> <span data-ttu-id="5fe7b-148">L’API retourne JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-148">The API will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-149">JET_TblInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="5fe7b-149">JET_TblInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-150"><em>pvResult</em> est interprété comme un tableau de deux ULONGs :</span><span class="sxs-lookup"><span data-stu-id="5fe7b-150"><em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="5fe7b-151">Le premier <strong>ULong</strong> est le nombre de pages dans la table.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-151">The first <strong>ULONG</strong> is the number of pages in the table.</span></span></p></li>
<li><p><span data-ttu-id="5fe7b-152">Le deuxième <strong>ULong</strong> est la densité cible des pages de la table.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-152">The second <strong>ULONG</strong> is the target density of pages for the table.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-153">JET_TblInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="5fe7b-153">JET_TblInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-154"><em>pvResult</em> est interprété comme <strong>ULong</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-154"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="5fe7b-155"><strong>ULong</strong> est la somme du nombre de pages disponibles dans la table, ses index et l’arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-155">The <strong>ULONG</strong> is the sum of the number of pages that are available in the table, its indexes, and the long value tree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-156">JET_TblInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="5fe7b-156">JET_TblInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-157"><em>pvResult</em> est interprété comme <strong>ULong</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-157"><em>pvResult</em> is interpreted as a <strong>ULONG</strong>.</span></span> <span data-ttu-id="5fe7b-158"><strong>ULong</strong> correspond à la somme du nombre de pages appartenant à la table (y compris ses index et à l’arborescence de valeurs longues et à toutes les pages disponibles).</span><span class="sxs-lookup"><span data-stu-id="5fe7b-158">The <strong>ULONG</strong> is the sum of the number of pages that are owned by the table (including its indexes, and the long value tree and any available pages therein).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-159">JET_TblInfoSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="5fe7b-159">JET_TblInfoSpaceUsage</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-160">Le comportement de l’API dépend de la taille de la mémoire tampon qui est transmise à l’API.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-160">The behavior of the API depends on how large the buffer that is passed to the API is.</span></span> <span data-ttu-id="5fe7b-161">Deux valeurs <em>cbMax</em> doivent être au moins (2 \* sizeof (ULONG)).</span><span class="sxs-lookup"><span data-stu-id="5fe7b-161">Two <em>cbMax</em> values must be at least ( 2 \* sizeof( ULONG ) ).</span></span></p>
<ul>
<li><p><span data-ttu-id="5fe7b-162">Si <em>cbMax</em> est (2 \* sizeof (ULONG)), <em>pvResult</em> est interprété comme un tableau de deux ULONGs :</span><span class="sxs-lookup"><span data-stu-id="5fe7b-162">If <em>cbMax</em> is ( 2 \* sizeof( ULONG ) ), <em>pvResult</em> is interpreted as an array of two ULONGs:</span></span></p>
<ul>
<li><p><span data-ttu-id="5fe7b-163">Le premier <strong>ULong</strong> est le nombre d’étendues appartenant à la table.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-163">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="5fe7b-164">Le deuxième <strong>ULong</strong> est le nombre d’étendues disponibles de la table.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-164">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="5fe7b-165"><em>pvResult</em> est interprété comme un tableau de :</span><span class="sxs-lookup"><span data-stu-id="5fe7b-165"><em>pvResult</em> is interpreted as an array of:</span></span></p>
<ul>
<li><p><span data-ttu-id="5fe7b-166">Le premier <strong>ULong</strong> est le nombre d’étendues appartenant à la table.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-166">The first <strong>ULONG</strong> is the number of Owned Extents of the table.</span></span></p></li>
<li><p><span data-ttu-id="5fe7b-167">Le deuxième <strong>ULong</strong> est le nombre d’étendues disponibles de la table.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-167">The second <strong>ULONG</strong> is the number of Available Extents of the table.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-168">JET_TblInfoTemplateTableName</span><span class="sxs-lookup"><span data-stu-id="5fe7b-168">JET_TblInfoTemplateTableName</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-169"><em>pvResult</em> est interprété comme une mémoire tampon de chaîne.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-169"><em>pvResult</em> is interpreted as a string buffer.</span></span> <span data-ttu-id="5fe7b-170">La mémoire tampon doit être au moins JET_cbNameMost + 1, y compris le caractère <strong>null</strong>de fin.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-170">The buffer must be at least JET_cbNameMost + 1, including the terminating <strong>NULL</strong>.</span></span> <span data-ttu-id="5fe7b-171">Si la table est une table dérivée, la mémoire tampon est remplie avec le nom de la table à partir de laquelle la table dérivée a hérité son DDL.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-171">If the table is a derived table, the buffer will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="5fe7b-172">Si la table n’est pas une table dérivée, la mémoire tampon est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-172">If the table is not a derived table, the buffer will an empty string.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5fe7b-173">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5fe7b-173">Return Value</span></span>

<span data-ttu-id="5fe7b-174">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5fe7b-175">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5fe7b-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5fe7b-176">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5fe7b-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="5fe7b-177">Description</span><span class="sxs-lookup"><span data-stu-id="5fe7b-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5fe7b-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-179">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-180">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="5fe7b-180">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-181">La mémoire tampon est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-181">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-182">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="5fe7b-182">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-183">Un <em>InfoLevel</em> déconseillé a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-183">A deprecated <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-184">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="5fe7b-184">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-185">La mémoire tampon n’est pas de la bonne taille.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-185">The buffer was not the right size.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-186">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="5fe7b-186">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-187">La table qui a été transmise était une table temporaire et le <em>InfoLevel</em> demandé ne peut pas être récupéré pour une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-187">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-188">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="5fe7b-188">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-189">La table qui a été transmise était une table temporaire et le <em>InfoLevel</em> demandé ne peut pas être récupéré pour une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-189">The table that was passed in was a temporary table, and the requested <em>InfoLevel</em> cannot be retrieved for a temporary table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-190">JET_errQueryNotSupported</span><span class="sxs-lookup"><span data-stu-id="5fe7b-190">JET_errQueryNotSupported</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-191"><em>InfoLevel</em> n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-191">The <em>InfoLevel</em> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-192">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="5fe7b-192">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-193">La table est utilisée par une autre opération de base de données.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-193">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-194">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="5fe7b-194">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-195">La table est verrouillée par une autre opération de base de données.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-195">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-196">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="5fe7b-196">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="5fe7b-197">La table est utilisée par le système.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-197">The table is being used by the system.</span></span> <span data-ttu-id="5fe7b-198">Cet avertissement n’est pas irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-198">This warning is nonfatal.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="5fe7b-199">Notes</span><span class="sxs-lookup"><span data-stu-id="5fe7b-199">Remarks</span></span>

<span data-ttu-id="5fe7b-200">Certaines informations ne sont pas valides pour les tables temporaires (voir [JetOpenTempTable](./jetopentemptable-function.md)).</span><span class="sxs-lookup"><span data-stu-id="5fe7b-200">Some pieces of information are not valid for temporary tables (See [JetOpenTempTable](./jetopentemptable-function.md)).</span></span>

<span data-ttu-id="5fe7b-201">Les statistiques de table incluent le nombre d’enregistrements et le nombre de pages dans l’index cluster (autrement dit, l’index contenant les données d’enregistrement).</span><span class="sxs-lookup"><span data-stu-id="5fe7b-201">The table statistics include the number of records and the number of pages in the clustered index (that is, the index containing the record data).</span></span> <span data-ttu-id="5fe7b-202">Les statistiques d’index sont accessibles séparément par nom, à l’aide de [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="5fe7b-202">The index statistics are accessed separately by name, using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5fe7b-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fe7b-203">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-204"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5fe7b-204"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5fe7b-205">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-205">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-206"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="5fe7b-206"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5fe7b-207">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-207">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-208"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="5fe7b-208"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5fe7b-209">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-209">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-210"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="5fe7b-210"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5fe7b-211">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-211">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5fe7b-212"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5fe7b-212"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5fe7b-213">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5fe7b-213">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5fe7b-214"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5fe7b-214"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5fe7b-215">Implémenté en tant que <strong>JetGetTableInfoW</strong> (Unicode) et <strong>JetGetTableInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5fe7b-215">Implemented as <strong>JetGetTableInfoW</strong> (Unicode) and <strong>JetGetTableInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5fe7b-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fe7b-216">See Also</span></span>

[<span data-ttu-id="5fe7b-217">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5fe7b-217">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5fe7b-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5fe7b-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5fe7b-219">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5fe7b-219">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5fe7b-220">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5fe7b-220">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5fe7b-221">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="5fe7b-221">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="5fe7b-222">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="5fe7b-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="5fe7b-223">JetGetObjectInfo</span><span class="sxs-lookup"><span data-stu-id="5fe7b-223">JetGetObjectInfo</span></span>](./jetgetobjectinfo-function.md)  
[<span data-ttu-id="5fe7b-224">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="5fe7b-224">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="5fe7b-225">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="5fe7b-225">JetOpenTempTable</span></span>](./jetopentemptable-function.md)
