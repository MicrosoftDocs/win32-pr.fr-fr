---
description: 'En savoir plus sur : fonction JetGetTableColumnInfo'
title: JetGetTableColumnInfo fonction)
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c7b073ca9be90e89a1c6b99c010707e6405323
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104211987"
---
# <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="00ba3-103">JetGetTableColumnInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="00ba3-103">JetGetTableColumnInfo Function</span></span>


<span data-ttu-id="00ba3-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="00ba3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettablecolumninfo-function"></a><span data-ttu-id="00ba3-105">JetGetTableColumnInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="00ba3-105">JetGetTableColumnInfo Function</span></span>

<span data-ttu-id="00ba3-106">La fonction **JetGetTableColumnInfo** récupère des informations sur une colonne de table.</span><span class="sxs-lookup"><span data-stu-id="00ba3-106">The **JetGetTableColumnInfo** function retrieves information about a table column.</span></span>

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a><span data-ttu-id="00ba3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00ba3-107">Parameters</span></span>

<span data-ttu-id="00ba3-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="00ba3-108">*sesid*</span></span>

<span data-ttu-id="00ba3-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="00ba3-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="00ba3-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="00ba3-110">*tableid*</span></span>

<span data-ttu-id="00ba3-111">Table qui contient la colonne pour laquelle extraire des informations.</span><span class="sxs-lookup"><span data-stu-id="00ba3-111">The table that contains the column to fetch information for.</span></span>

<span data-ttu-id="00ba3-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="00ba3-112">*szColumnName*</span></span>

<span data-ttu-id="00ba3-113">Nom de la colonne dont les informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="00ba3-113">The name of the column to fetch information for.</span></span>

<span data-ttu-id="00ba3-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="00ba3-114">*pvResult*</span></span>

<span data-ttu-id="00ba3-115">Pointeur vers une mémoire tampon qui recevra les informations.</span><span class="sxs-lookup"><span data-stu-id="00ba3-115">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="00ba3-116">Le type de la mémoire tampon dépend de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="00ba3-116">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="00ba3-117">L’appelant doit être configuré pour aligner la mémoire tampon de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="00ba3-117">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="00ba3-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="00ba3-118">*cbMax*</span></span>

<span data-ttu-id="00ba3-119">Taille, en octets, de la mémoire tampon qui a été passée dans *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="00ba3-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="00ba3-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="00ba3-120">*InfoLevel*</span></span>

<span data-ttu-id="00ba3-121">Type des informations qui seront récupérées pour la colonne spécifiée par *szColumnName*.</span><span class="sxs-lookup"><span data-stu-id="00ba3-121">The type of information that will be retrieved for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="00ba3-122">Le format des données stockées dans *pvResult* dépend de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="00ba3-122">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span> <span data-ttu-id="00ba3-123">Pour obtenir le schéma de la table temporaire, consultez [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="00ba3-123">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

  - <span data-ttu-id="00ba3-124">JET_ColInfoListSortColumnid triera la table temporaire par *ColumnID*.</span><span class="sxs-lookup"><span data-stu-id="00ba3-124">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="00ba3-125">JET_ColInfoListCompact compacte la sortie.</span><span class="sxs-lookup"><span data-stu-id="00ba3-125">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="00ba3-126">Pour plus d’informations sur la sortie compacte, consultez [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="00ba3-126">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="00ba3-127">Les options suivantes peuvent être définies pour ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="00ba3-127">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00ba3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="00ba3-128">Value</span></span></p></th>
<th><p><span data-ttu-id="00ba3-129">Signification</span><span class="sxs-lookup"><span data-stu-id="00ba3-129">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-130">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="00ba3-130">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="00ba3-131"><em>pvResult</em> est interprété comme un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>et les champs de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> sont remplis de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="00ba3-131"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span> <span data-ttu-id="00ba3-132">JET_ColInfo et JET_ColInfoByColid récupérer les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="00ba3-132">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-133">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="00ba3-133">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="00ba3-134"><em>pvResult</em> est interprété comme une structure de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="00ba3-134"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="00ba3-135">Cela est similaire à une structure de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="00ba3-135">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="00ba3-136">Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="00ba3-136">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="00ba3-137">Si cette fonction échoue, la structure contient des données non définies.</span><span class="sxs-lookup"><span data-stu-id="00ba3-137">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-138">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="00ba3-138">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="00ba3-139"><em>pvResult</em> est interprété comme un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, sauf que ce <em>InfoLevel</em> indique que la colonne demandée (<em>szColumName</em>) n’est pas le nom de la colonne de chaîne, mais un pointeur vers une <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="00ba3-139"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span> <span data-ttu-id="00ba3-140">JET_ColInfo et JET_ColInfoByColid récupérer les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="00ba3-140">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-141">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="00ba3-141">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="00ba3-142"><em>pvResult</em> est interprété comme une structure de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="00ba3-142"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="00ba3-143">Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="00ba3-143">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="00ba3-144">Une table temporaire est ouverte et identifiée par le membre <em>TableID</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="00ba3-144">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="00ba3-145">La table doit être fermée avec <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="00ba3-145">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="00ba3-146">Si cette fonction échoue, la structure contient des données non définies.</span><span class="sxs-lookup"><span data-stu-id="00ba3-146">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-147">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="00ba3-147">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="00ba3-148"><em>pvResult</em> est interprété comme une structure de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="00ba3-148"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="00ba3-149">Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="00ba3-149">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="00ba3-150">Une table temporaire est ouverte et identifiée par le membre <em>TableID</em> de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="00ba3-150">A temporary table is opened and is identified by the <em>tableid</em> member of <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>.</span></span> <span data-ttu-id="00ba3-151">La table doit être fermée avec <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="00ba3-151">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="00ba3-152">Si cette fonction échoue, la structure contient des données non définies.</span><span class="sxs-lookup"><span data-stu-id="00ba3-152">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-153">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="00ba3-153">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="00ba3-154">Comme JET_ColInfoList, toutefois, la table résultante est triée par <em>ColumnID</em>, et non par nom de colonne.</span><span class="sxs-lookup"><span data-stu-id="00ba3-154">Same as JET_ColInfoList, however the resulting table is sorted by <em>columnid</em>, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-155">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="00ba3-155">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="00ba3-156">JET_ColInfoSysTabCursor est déconseillé et son utilisation retourne JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="00ba3-156">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-157">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="00ba3-157">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="00ba3-158">Comme JET_ColInfoBase, <em>pvResult</em> est interprété comme un <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, sauf que ce <em>InfoLevel</em> indique que la colonne demandée (<em>szColumName</em>) n’est pas le nom de la colonne de chaîne, mais un pointeur vers un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="00ba3-158">Same as JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="00ba3-159"><strong>Windows Vista :  </strong> Cette version est disponible dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="00ba3-159"><strong>Windows Vista:  </strong>This is available in Windows Vista and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="00ba3-160">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="00ba3-161">Retourne uniquement les colonnes non dérivées (si la table est dérivée d’un modèle).</span><span class="sxs-lookup"><span data-stu-id="00ba3-161">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="00ba3-162">Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="00ba3-162">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="00ba3-163"><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="00ba3-163"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-164">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="00ba3-164">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="00ba3-165">Retourne uniquement le nom de colonne et le ColumnID de chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="00ba3-165">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="00ba3-166">Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="00ba3-166">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="00ba3-167"><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="00ba3-167"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-168">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="00ba3-168">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="00ba3-169">Trie la liste des colonnes retournées par ColumnId (par défaut, trie la liste par nom de colonne).</span><span class="sxs-lookup"><span data-stu-id="00ba3-169">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="00ba3-170">Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="00ba3-170">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="00ba3-171"><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="00ba3-171"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="00ba3-172">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="00ba3-172">Return Value</span></span>

<span data-ttu-id="00ba3-173">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="00ba3-173">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="00ba3-174">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="00ba3-174">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00ba3-175">Code de retour</span><span class="sxs-lookup"><span data-stu-id="00ba3-175">Return code</span></span></p></th>
<th><p><span data-ttu-id="00ba3-176">Description</span><span class="sxs-lookup"><span data-stu-id="00ba3-176">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-177">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="00ba3-177">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="00ba3-178">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="00ba3-178">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-179">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="00ba3-179">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="00ba3-180">La colonne nommée <em>szColumnName</em> est introuvable dans la table.</span><span class="sxs-lookup"><span data-stu-id="00ba3-180">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-181">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="00ba3-181">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="00ba3-182">Un <em>InfoLevel</em> incorrect a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="00ba3-182">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-183">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="00ba3-183">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="00ba3-184">Cette erreur peut être retournée dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="00ba3-184">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="00ba3-185">Un nom incorrect a été donné pour <em>szTableName</em> .</span><span class="sxs-lookup"><span data-stu-id="00ba3-185">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="00ba3-186">Un nom incorrect a été donné pour <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="00ba3-186">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="00ba3-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="00ba3-188">Cette erreur peut être retournée dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="00ba3-188">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="00ba3-189">Un <em>InfoLevel</em> incorrect a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="00ba3-189">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="00ba3-190">Un <em>SZTABLENAME</em> null a été passé.</span><span class="sxs-lookup"><span data-stu-id="00ba3-190">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="00ba3-191">La mémoire tampon est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="00ba3-191">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="00ba3-192">Notes</span><span class="sxs-lookup"><span data-stu-id="00ba3-192">Remarks</span></span>

<span data-ttu-id="00ba3-193">**JetGetTableColumnInfo** et [JetGetColumnInfo](./jetgetcolumninfo-function.md) récupèrent les informations sur une colonne.</span><span class="sxs-lookup"><span data-stu-id="00ba3-193">**JetGetTableColumnInfo** and [JetGetColumnInfo](./jetgetcolumninfo-function.md) both retrieve information about a column.</span></span> <span data-ttu-id="00ba3-194">La différence entre les deux est la manière dont la table est identifiée :</span><span class="sxs-lookup"><span data-stu-id="00ba3-194">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="00ba3-195">**JetGetTableColumnInfo** identifie une table par *TableID*.</span><span class="sxs-lookup"><span data-stu-id="00ba3-195">**JetGetTableColumnInfo** identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="00ba3-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifie une table par la combinaison *dbid* et *szTableName* .</span><span class="sxs-lookup"><span data-stu-id="00ba3-196">[JetGetColumnInfo](./jetgetcolumninfo-function.md) identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="00ba3-197">Lorsque vous récupérez des données avec JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, une table temporaire est ouverte.</span><span class="sxs-lookup"><span data-stu-id="00ba3-197">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="00ba3-198">La table temporaire contient des données et la structure [JET_COLUMNLIST](./jet-columnlist-structure.md) contient des informations suffisantes pour parcourir la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="00ba3-198">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="00ba3-199">La table temporaire doit être fermée avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="00ba3-199">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="00ba3-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00ba3-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="00ba3-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="00ba3-202">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="00ba3-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-203"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="00ba3-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="00ba3-204">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="00ba3-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-205"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="00ba3-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="00ba3-206">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="00ba3-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-207"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="00ba3-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="00ba3-208">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="00ba3-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00ba3-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="00ba3-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="00ba3-210">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="00ba3-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00ba3-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="00ba3-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="00ba3-212">Implémenté en tant que <strong>JetGetTableColumnInfoW</strong> (Unicode) et <strong>JetGetTableColumnInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="00ba3-212">Implemented as <strong>JetGetTableColumnInfoW</strong> (Unicode) and <strong>JetGetTableColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="00ba3-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00ba3-213">See Also</span></span>

[<span data-ttu-id="00ba3-214">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="00ba3-214">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="00ba3-215">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="00ba3-215">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="00ba3-216">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="00ba3-216">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="00ba3-217">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="00ba3-217">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="00ba3-218">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="00ba3-218">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="00ba3-219">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="00ba3-219">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="00ba3-220">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="00ba3-220">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="00ba3-221">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="00ba3-221">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="00ba3-222">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="00ba3-222">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="00ba3-223">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="00ba3-223">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="00ba3-224">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="00ba3-224">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="00ba3-225">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="00ba3-225">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="00ba3-226">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="00ba3-226">JetGetTableColumnInfo</span></span>]()
