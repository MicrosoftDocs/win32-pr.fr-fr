---
description: 'En savoir plus sur : fonction JetGetColumnInfo'
title: Fonction JetGetColumnInfo
TOCTitle: JetGetColumnInfo Function
ms:assetid: 2db024e9-2784-4fb2-84b2-fef7ae518938
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269215(v=EXCHG.10)
ms:contentKeyID: 32765518
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetColumnInfoA
- JetGetColumnInfoW
- JetGetColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d96d5860f4b10f9294ab210e4e41d78cede202f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522104"
---
# <a name="jetgetcolumninfo-function"></a><span data-ttu-id="5a54e-103">Fonction JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="5a54e-103">JetGetColumnInfo Function</span></span>


<span data-ttu-id="5a54e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="5a54e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcolumninfo-function"></a><span data-ttu-id="5a54e-105">Fonction JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="5a54e-105">JetGetColumnInfo Function</span></span>

<span data-ttu-id="5a54e-106">La fonction **JetGetColumnInfo** récupère des informations sur une colonne.</span><span class="sxs-lookup"><span data-stu-id="5a54e-106">The **JetGetColumnInfo** function retrieves information about a column.</span></span>

```cpp
    JET_ERR JET_API JetGetColumnInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szColumnName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="5a54e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a54e-107">Parameters</span></span>

<span data-ttu-id="5a54e-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5a54e-108">*sesid*</span></span>

<span data-ttu-id="5a54e-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="5a54e-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="5a54e-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="5a54e-110">*dbid*</span></span>

<span data-ttu-id="5a54e-111">Identifie, avec *szTableName*, la table qui contient la colonne à partir de laquelle les informations sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="5a54e-111">Identifies, along with *szTableName*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="5a54e-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="5a54e-112">*szTableName*</span></span>

<span data-ttu-id="5a54e-113">Identifie, avec *dbid*, la table qui contient la colonne à partir de laquelle les informations sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="5a54e-113">Identifies, along with *dbid*, the table that contains the column from which the information is retrieved.</span></span>

<span data-ttu-id="5a54e-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="5a54e-114">*szColumnName*</span></span>

<span data-ttu-id="5a54e-115">Nom de la colonne pour laquelle les informations sont extraites.</span><span class="sxs-lookup"><span data-stu-id="5a54e-115">The name of the column that information is fetched for.</span></span>

<span data-ttu-id="5a54e-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="5a54e-116">*pvResult*</span></span>

<span data-ttu-id="5a54e-117">Pointeur vers une mémoire tampon qui recevra les informations.</span><span class="sxs-lookup"><span data-stu-id="5a54e-117">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="5a54e-118">Le type de la mémoire tampon dépend de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="5a54e-118">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="5a54e-119">L’appelant doit être configuré pour aligner la mémoire tampon de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="5a54e-119">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="5a54e-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="5a54e-120">*cbMax*</span></span>

<span data-ttu-id="5a54e-121">Taille, en octets, de la mémoire tampon passée dans *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="5a54e-121">The size, in bytes, of the buffer that is passed in *pvResult*.</span></span>

<span data-ttu-id="5a54e-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="5a54e-122">*InfoLevel*</span></span>

<span data-ttu-id="5a54e-123">Type d’informations à récupérer pour la colonne spécifiée par *szColumnName*.</span><span class="sxs-lookup"><span data-stu-id="5a54e-123">The type of information to retrieve for the column that is specified by *szColumnName*.</span></span> <span data-ttu-id="5a54e-124">Le format des données stockées dans *pvResult* dépend de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="5a54e-124">The format of the data stored in *pvResult* is dependent on this parameter.</span></span> <span data-ttu-id="5a54e-125">Pour obtenir le schéma de la table temporaire, consultez [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="5a54e-125">For the schema of the temporary table, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="5a54e-126">Ces *InfoLevels* sont différenciées par :</span><span class="sxs-lookup"><span data-stu-id="5a54e-126">These *InfoLevels* are differentiated by:</span></span>

  - <span data-ttu-id="5a54e-127">JET_ColInfoListSortColumnid triera la table temporaire par *ColumnID*.</span><span class="sxs-lookup"><span data-stu-id="5a54e-127">JET_ColInfoListSortColumnid will sort the temporary table by *columnid*.</span></span>

  - <span data-ttu-id="5a54e-128">JET_ColInfoListCompact compacte la sortie.</span><span class="sxs-lookup"><span data-stu-id="5a54e-128">JET_ColInfoListCompact will compact the output.</span></span> <span data-ttu-id="5a54e-129">Pour plus d’informations sur la sortie compacte, consultez [JET_COLUMNLIST](./jet-columnlist-structure.md).</span><span class="sxs-lookup"><span data-stu-id="5a54e-129">For more information about the compact output, see [JET_COLUMNLIST](./jet-columnlist-structure.md).</span></span>

<span data-ttu-id="5a54e-130">Les options suivantes peuvent être utilisées avec ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="5a54e-130">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a54e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a54e-131">Value</span></span></p></th>
<th><p><span data-ttu-id="5a54e-132">Signification</span><span class="sxs-lookup"><span data-stu-id="5a54e-132">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-133">JET_ColInfo</span><span class="sxs-lookup"><span data-stu-id="5a54e-133">JET_ColInfo</span></span></p></td>
<td><p><span data-ttu-id="5a54e-134">JET_ColInfo et JET_ColInfoByColid récupérer les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="5a54e-134">JET_ColInfo and JET_ColInfoByColid both retrieve the same information.</span></span> <span data-ttu-id="5a54e-135"><em>pvResult</em> est interprété comme un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>et les champs de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> sont remplis de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="5a54e-135"><em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, and the fields of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure are filled in appropriately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-136">JET_ColInfoBase</span><span class="sxs-lookup"><span data-stu-id="5a54e-136">JET_ColInfoBase</span></span></p></td>
<td><p><span data-ttu-id="5a54e-137"><em>pvResult</em> est interprété comme une structure de <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> .</span><span class="sxs-lookup"><span data-stu-id="5a54e-137"><em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> structure.</span></span> <span data-ttu-id="5a54e-138">Cela est similaire à une structure de <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> .</span><span class="sxs-lookup"><span data-stu-id="5a54e-138">This is similar to a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure.</span></span> <span data-ttu-id="5a54e-139">Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="5a54e-139">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="5a54e-140">Si cette fonction échoue, la structure contient des données non définies.</span><span class="sxs-lookup"><span data-stu-id="5a54e-140">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-141">JET_ColInfoByColid</span><span class="sxs-lookup"><span data-stu-id="5a54e-141">JET_ColInfoByColid</span></span></p></td>
<td><p><span data-ttu-id="5a54e-142">Comme JET_ColInfo, <em>pvResult</em> est interprété comme un <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, sauf que ce <em>InfoLevel</em> indique que la colonne demandée (<em>szColumName</em>) n’est pas le nom de la colonne de chaîne, mais un pointeur vers un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="5a54e-142">Like JET_ColInfo, <em>pvResult</em> is interpreted as a <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>, except this <em>InfoLevel</em> indicates that the requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-143">JET_ColInfoList</span><span class="sxs-lookup"><span data-stu-id="5a54e-143">JET_ColInfoList</span></span></p></td>
<td><p><span data-ttu-id="5a54e-144"><em>pvResult</em> est interprété comme une structure de <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="5a54e-144"><em>pvResult</em> is interpreted as a <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="5a54e-145">Si cette fonction est réussie, la structure est remplie avec les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="5a54e-145">If this function succeeds, the structure is populated with appropriate values.</span></span> <span data-ttu-id="5a54e-146">Une table temporaire est ouverte et identifiée par le membre <strong>TableID</strong> de la structure <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="5a54e-146">A temporary table is opened and is identified by the <strong>tableid</strong> member of the <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> structure.</span></span> <span data-ttu-id="5a54e-147">La table doit être fermée avec <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="5a54e-147">The table must be closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span> <span data-ttu-id="5a54e-148">Si cette fonction échoue, la structure contient des données non définies.</span><span class="sxs-lookup"><span data-stu-id="5a54e-148">If this function fails, the structure contains undefined data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-149">JET_ColInfoListCompact</span><span class="sxs-lookup"><span data-stu-id="5a54e-149">JET_ColInfoListCompact</span></span></p></td>
<td><p><span data-ttu-id="5a54e-150">Identique à JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="5a54e-150">Same as JET_ColInfoList.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-151">JET_ColInfoListSortColumnid</span><span class="sxs-lookup"><span data-stu-id="5a54e-151">JET_ColInfoListSortColumnid</span></span></p></td>
<td><p><span data-ttu-id="5a54e-152">Identique à JET_ColInfoList ; Toutefois, la table résultante est triée par ColumnId, au lieu du nom de colonne.</span><span class="sxs-lookup"><span data-stu-id="5a54e-152">Same as JET_ColInfoList; however the resulting table is sorted by columnid, instead of column name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-153">JET_ColInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="5a54e-153">JET_ColInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="5a54e-154">JET_ColInfoSysTabCursor est déconseillé et son utilisation retourne JET_errFeatureNotAvailable.</span><span class="sxs-lookup"><span data-stu-id="5a54e-154">JET_ColInfoSysTabCursor is deprecated, and use of it will return JET_errFeatureNotAvailable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-155">JET_ColInfoBaseByColId</span><span class="sxs-lookup"><span data-stu-id="5a54e-155">JET_ColInfoBaseByColId</span></span></p></td>
<td><p><span data-ttu-id="5a54e-156">Comme JET_ColInfoBase, <em>pvResult</em> est interprété comme un <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, sauf que ce <em>InfoLevel</em> indique que la colonne demandée (<em>szColumName</em>) n’est pas le nom de la colonne de chaîne, mais un pointeur vers un <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span><span class="sxs-lookup"><span data-stu-id="5a54e-156">Like JET_ColInfoBase, <em>pvResult</em> is interpreted as a <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>, except this <em>InfoLevel</em> indicates that requested column (<em>szColumName</em>) is not the string column name, but a pointer to a <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>.</span></span></p>
<p><span data-ttu-id="5a54e-157"><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a54e-157"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="5a54e-158">JET_ColInfoGrbitNonDerivedColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="5a54e-159">Retourne uniquement les colonnes non dérivées (si la table est dérivée d’un modèle).</span><span class="sxs-lookup"><span data-stu-id="5a54e-159">Only return non-derived columns (if the table is derived from a template).</span></span></p>
<p><span data-ttu-id="5a54e-160">Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="5a54e-160">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="5a54e-161"><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a54e-161"><strong>Windows Vista:  </strong>This value is introduced Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-162">JET_ColInfoGrbitMinimalInfo</span><span class="sxs-lookup"><span data-stu-id="5a54e-162">JET_ColInfoGrbitMinimalInfo</span></span></p></td>
<td><p><span data-ttu-id="5a54e-163">Retourne uniquement le nom de colonne et le ColumnID de chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="5a54e-163">Only return the column name and columnid of each column.</span></span></p>
<p><span data-ttu-id="5a54e-164">Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="5a54e-164">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="5a54e-165"><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a54e-165"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-166">JET_ColInfoGrbitSortByColumnid</span><span class="sxs-lookup"><span data-stu-id="5a54e-166">JET_ColInfoGrbitSortByColumnid</span></span></p></td>
<td><p><span data-ttu-id="5a54e-167">Trie la liste des colonnes retournées par ColumnId (par défaut, trie la liste par nom de colonne).</span><span class="sxs-lookup"><span data-stu-id="5a54e-167">Sort returned column list by columnid (default is to sort list by column name).</span></span></p>
<p><span data-ttu-id="5a54e-168">Cette valeur peut être logiquement ou en <em>InfoLevel</em>, lorsque le <em>InfoLevel</em> de base est JET_ColInfoList.</span><span class="sxs-lookup"><span data-stu-id="5a54e-168">This value can be logically or'd into the <em>InfoLevel</em>, when the base <em>InfoLevel</em> is JET_ColInfoList.</span></span></p>
<p><span data-ttu-id="5a54e-169"><strong>Windows Vista :  </strong> Cette valeur est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a54e-169"><strong>Windows Vista:  </strong>This value is introduced in Windows Vista.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="5a54e-170">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a54e-170">Return Value</span></span>

<span data-ttu-id="5a54e-171">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="5a54e-171">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5a54e-172">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5a54e-172">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a54e-173">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5a54e-173">Return code</span></span></p></th>
<th><p><span data-ttu-id="5a54e-174">Description</span><span class="sxs-lookup"><span data-stu-id="5a54e-174">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-175">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5a54e-175">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5a54e-176">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5a54e-176">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-177">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="5a54e-177">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="5a54e-178">La colonne nommée <em>szColumnName</em> est introuvable dans la table.</span><span class="sxs-lookup"><span data-stu-id="5a54e-178">The column named <em>szColumnName</em> was not found in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-179">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="5a54e-179">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="5a54e-180">Un <em>InfoLevel</em> incorrect a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="5a54e-180">A bad <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-181">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="5a54e-181">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="5a54e-182">Cette erreur peut être retournée dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="5a54e-182">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="5a54e-183">Un nom incorrect a été donné pour <em>szTableName</em> .</span><span class="sxs-lookup"><span data-stu-id="5a54e-183">A bad name for <em>szTableName</em> was given.</span></span></p></li>
<li><p><span data-ttu-id="5a54e-184">Un nom incorrect a été donné pour <em>szColumnName</em> .</span><span class="sxs-lookup"><span data-stu-id="5a54e-184">A bad name for <em>szColumnName</em> was given.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-185">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5a54e-185">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5a54e-186">Cette erreur peut être retournée dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="5a54e-186">This error can be returned if:</span></span></p>
<ul>
<li><p><span data-ttu-id="5a54e-187">Un <em>InfoLevel</em> incorrect a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="5a54e-187">A bad <em>InfoLevel</em> was specified.</span></span></p></li>
<li><p><span data-ttu-id="5a54e-188">Un <em>SZTABLENAME</em> null a été passé.</span><span class="sxs-lookup"><span data-stu-id="5a54e-188">A NULL <em>szTableName</em> was passed in.</span></span></p></li>
<li><p><span data-ttu-id="5a54e-189">La mémoire tampon est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="5a54e-189">The buffer is too small.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="5a54e-190">Notes</span><span class="sxs-lookup"><span data-stu-id="5a54e-190">Remarks</span></span>

<span data-ttu-id="5a54e-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) et **JetGetColumnInfo** récupèrent les informations sur une colonne.</span><span class="sxs-lookup"><span data-stu-id="5a54e-191">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) and **JetGetColumnInfo** both retrieve information about a column.</span></span> <span data-ttu-id="5a54e-192">La différence entre les deux est la manière dont la table est identifiée :</span><span class="sxs-lookup"><span data-stu-id="5a54e-192">The difference between them is how the table is identified:</span></span>

  - <span data-ttu-id="5a54e-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifie une table par *TableID*.</span><span class="sxs-lookup"><span data-stu-id="5a54e-193">[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) identifies a table by *tableid*.</span></span>

  - <span data-ttu-id="5a54e-194">**JetGetColumnInfo** identifie une table par la combinaison *dbid* et *szTableName* .</span><span class="sxs-lookup"><span data-stu-id="5a54e-194">**JetGetColumnInfo** identifies a table by *dbid* and *szTableName* combination.</span></span>

<span data-ttu-id="5a54e-195">Lorsque vous récupérez des données avec JET_ColInfoList, JET_ColInfoListSortColumnid ou JET_ColInfoListCompact, une table temporaire est ouverte.</span><span class="sxs-lookup"><span data-stu-id="5a54e-195">When retrieving data with JET_ColInfoList, JET_ColInfoListSortColumnid, or JET_ColInfoListCompact, a temporary table will be opened.</span></span> <span data-ttu-id="5a54e-196">La table temporaire contient des données et la structure [JET_COLUMNLIST](./jet-columnlist-structure.md) contient des informations suffisantes pour parcourir la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="5a54e-196">The temporary table contains data, and the [JET_COLUMNLIST](./jet-columnlist-structure.md) structure contains sufficient information to traverse the temporary table.</span></span> <span data-ttu-id="5a54e-197">La table temporaire doit être fermée avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="5a54e-197">The temporary table must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="5a54e-198">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a54e-198">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-199"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5a54e-199"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5a54e-200">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="5a54e-200">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-201"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="5a54e-201"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5a54e-202">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5a54e-202">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-203"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="5a54e-203"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5a54e-204">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="5a54e-204">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-205"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="5a54e-205"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5a54e-206">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5a54e-206">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a54e-207"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5a54e-207"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5a54e-208">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5a54e-208">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a54e-209"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5a54e-209"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5a54e-210">Implémenté en tant que <strong>JetGetColumnInfoW</strong> (Unicode) et <strong>JetGetColumnInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5a54e-210">Implemented as <strong>JetGetColumnInfoW</strong> (Unicode) and <strong>JetGetColumnInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5a54e-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a54e-211">See Also</span></span>

[<span data-ttu-id="5a54e-212">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="5a54e-212">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="5a54e-213">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="5a54e-213">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="5a54e-214">JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="5a54e-214">JET_COLUMNBASE</span></span>](./jet-columnbase-structure.md)  
[<span data-ttu-id="5a54e-215">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="5a54e-215">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="5a54e-216">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="5a54e-216">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="5a54e-217">JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="5a54e-217">JET_COLUMNLIST</span></span>](./jet-columnlist-structure.md)  
[<span data-ttu-id="5a54e-218">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5a54e-218">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5a54e-219">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5a54e-219">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5a54e-220">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5a54e-220">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5a54e-221">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="5a54e-221">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="5a54e-222">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="5a54e-222">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="5a54e-223">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="5a54e-223">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
