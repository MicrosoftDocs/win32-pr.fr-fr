---
description: 'En savoir plus sur : fonction JetGetDatabaseFileInfo'
title: JetGetDatabaseFileInfo fonction)
TOCTitle: JetGetDatabaseFileInfo Function
ms:assetid: 457079d9-46c9-4da0-a35b-0c11fca7ed5b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269239(v=EXCHG.10)
ms:contentKeyID: 32765541
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetDatabaseFileInfo
- JetGetDatabaseFileInfoW
- JetGetDatabaseFileInfoA
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2ac94dd6f088a82c932aaca5b60ec16f49644f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524732"
---
# <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="2dbc4-103">JetGetDatabaseFileInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="2dbc4-103">JetGetDatabaseFileInfo Function</span></span>


<span data-ttu-id="2dbc4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2dbc4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabasefileinfo-function"></a><span data-ttu-id="2dbc4-105">JetGetDatabaseFileInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="2dbc4-105">JetGetDatabaseFileInfo Function</span></span>

<span data-ttu-id="2dbc4-106">La fonction **JetGetDatabaseFileInfo** récupère différents types d’informations sur la base de données.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-106">The **JetGetDatabaseFileInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="2dbc4-107">Cette API peut être appelée lorsqu’une base de données est attachée ou en ligne (avec [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) ou que la base de données ou le moteur de base de données est hors connexion (avec **JetGetDatabaseFileInfo**).</span><span class="sxs-lookup"><span data-stu-id="2dbc4-107">This API can be called while a database is attached or online (with [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) or while the database or database engine is offline (with **JetGetDatabaseFileInfo**).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseFileInfo(
      __in          const tchar* szDatabaseName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="2dbc4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2dbc4-108">Parameters</span></span>

<span data-ttu-id="2dbc4-109">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="2dbc4-109">*szDatabaseName*</span></span>

<span data-ttu-id="2dbc4-110">Chemin d’accès de la base de données à partir de laquelle récupérer les informations.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-110">The path of the database from which to retrieve the information.</span></span>

<span data-ttu-id="2dbc4-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="2dbc4-111">*pvResult*</span></span>

<span data-ttu-id="2dbc4-112">Pointeur vers une mémoire tampon qui recevra les informations spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-112">Pointer to a buffer that will receive the specified information.</span></span> <span data-ttu-id="2dbc4-113">La taille de la mémoire tampon, en octets, est passée dans *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-113">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="2dbc4-114">Si cette fonction échoue, le contenu de *pvResult* n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-114">If this function fails, the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="2dbc4-115">Les informations stockées dans *pvResult* dépendent de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-115">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="2dbc4-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="2dbc4-116">*cbMax*</span></span>

<span data-ttu-id="2dbc4-117">Taille, en octets, de la mémoire tampon passée dans *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-117">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="2dbc4-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="2dbc4-118">*InfoLevel*</span></span>

<span data-ttu-id="2dbc4-119">*InfoLevel* spécifie le type d’informations à récupérer sur la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-119">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="2dbc4-120">Cela affecte la façon dont *pvResult* est interprété.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-120">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="2dbc4-121">Certains objets *InfoLevel* sont disponibles uniquement dans la version hors connexion (**JetGetDatabaseFileInfo**) ou en ligne ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) de l’API.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-121">Some *InfoLevel* objects are available only in the offline (**JetGetDatabaseFileInfo**) or online ([JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md)) version of the API.</span></span>

<span data-ttu-id="2dbc4-122">Si la mémoire tampon *pvResult* fournie est trop petite, JET_errInvalidBufferSize ou JET_errBufferTooSmall sera retourné, en fonction du *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-122">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned, depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dbc4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2dbc4-123">Value</span></span></p></th>
<th><p><span data-ttu-id="2dbc4-124">Signification</span><span class="sxs-lookup"><span data-stu-id="2dbc4-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-125">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="2dbc4-125">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-126"><em>pvResult</em> sera interprété comme un QWORD (8 octets).</span><span class="sxs-lookup"><span data-stu-id="2dbc4-126"><em>pvResult</em> will be interpreted as a QWORD (8 bytes).</span></span> <span data-ttu-id="2dbc4-127">Retourne la taille de la base de données en octets.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-127">Returns the size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-128">JET_DbInfoUpgrade</span><span class="sxs-lookup"><span data-stu-id="2dbc4-128">JET_DbInfoUpgrade</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-129"><em>pvResult</em> sera interprété comme un <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-129"><em>pvResult</em> will be interpreted as a <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a>.</span></span> <span data-ttu-id="2dbc4-130">La structure <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> sera remplie avec les informations relatives à la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-130">The <a href="gg294114(v=exchg.10).md">JET_DBINFOUPGRADE</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-131">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="2dbc4-131">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-132"><em>pvResult</em> sera interprété comme un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-132"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="2dbc4-133">La structure <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> sera remplie avec les informations relatives à la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-133">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the specified database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-134">JET_DbInfoDBInUse</span><span class="sxs-lookup"><span data-stu-id="2dbc4-134">JET_DbInfoDBInUse</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-135"><em>pvResult</em> sera interprété comme un bool (4 octets).</span><span class="sxs-lookup"><span data-stu-id="2dbc4-135"><em>pvResult</em> will be interpreted as a BOOL (4 bytes).</span></span> <span data-ttu-id="2dbc4-136">Cela indique si le moteur de base de données a actuellement des bases de données ouvertes ou attachées.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-136">This will return whether the database engine currently has any open or attached databases.</span></span></p>
<p><span data-ttu-id="2dbc4-137"><strong>Windows XP :  </strong> Cette valeur est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-137"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-138">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="2dbc4-138">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-139"><em>pvResult</em> sera interprété comme un entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-139"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="2dbc4-140">Cela renverra la taille de page de la base de données en octets.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-140">This will return the page size of the database in bytes.</span></span></p>
<p><span data-ttu-id="2dbc4-141"><strong>Windows XP :  </strong> Cette valeur est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-141"><strong>Windows XP:  </strong>This value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-142">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="2dbc4-142">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-143">Ces <em>InfoLevels</em> ne sont pas encore pris en charge et retournent des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-143">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="2dbc4-144">N’utilisez pas ces <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-144">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-145">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="2dbc4-145">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-146">Ces <em>InfoLevels</em> ne sont pas encore pris en charge et retournent des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-146">These <em>InfoLevels</em> are not yet supported and return default values.</span></span> <span data-ttu-id="2dbc4-147">N’utilisez pas ces <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-147">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-148">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="2dbc4-148">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-149">Identique à JET_DbInfoCp.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-149">Same as JET_DbInfoCp.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-150">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="2dbc4-150">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-151">Ces <em>InfoLevels</em> sont déconseillés et ne sont pas pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-151">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="2dbc4-152">N’utilisez pas ces <em>InfoLevels</em>.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-152">Do not use these <em>InfoLevels</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-153">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="2dbc4-153">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-154">Identique à JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-154">Same as JET_DbInfoIsam.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-155">JET_DbInfoFileType</span><span class="sxs-lookup"><span data-stu-id="2dbc4-155">JET_DbInfoFileType</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-156"><strong>Windows Vista :  </strong> Cette valeur <em>InfoLevel</em> est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-156"><strong>Windows Vista:  </strong>This <em>InfoLevel</em> value is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="2dbc4-157"><em>pvResult</em> sera traité comme un pointeur vers une valeur DWORD.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-157"><em>pvResult</em> will be treated as a pointer to a DWORD.</span></span> <span data-ttu-id="2dbc4-158">Retourne une valeur d’énumération, indiquant le type de fichier que le moteur considère comme étant.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-158">Returns an enumeration value, indicating what kind of file the engine considers this to be.</span></span> <span data-ttu-id="2dbc4-159">Les types de fichiers sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-159">File types are listed in the following table.</span></span> <span data-ttu-id="2dbc4-160">Pour plus d’informations sur ces types de fichiers et leur utilisation pour le moteur, voir <a href="gg294069(v=exchg.10).md">fichiers ESE (Extensible Storage Engine</a>).</span><span class="sxs-lookup"><span data-stu-id="2dbc4-160">For more information about these types of files and their usage to the engine, see <a href="gg294069(v=exchg.10).md">Extensible Storage Engine Files</a>.</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dbc4-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="2dbc4-161">Value</span></span></p></th>
<th><p><span data-ttu-id="2dbc4-162">Signification</span><span class="sxs-lookup"><span data-stu-id="2dbc4-162">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-163">JET_filetypeUnknown</span><span class="sxs-lookup"><span data-stu-id="2dbc4-163">JET_filetypeUnknown</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-164">Le type de fichier est inconnu ou n’est pas un type de fichier ESE.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-164">The type of file is unknown, or not an ESE file type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-165">JET_filetypeDatabase</span><span class="sxs-lookup"><span data-stu-id="2dbc4-165">JET_filetypeDatabase</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-166">Le fichier est un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-166">The file is a database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-167">JET_filetypeLog</span><span class="sxs-lookup"><span data-stu-id="2dbc4-167">JET_filetypeLog</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-168">Le fichier est un fichier journal de transactions.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-168">The file is a transaction log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-169">JET_filetypeCheckpoint</span><span class="sxs-lookup"><span data-stu-id="2dbc4-169">JET_filetypeCheckpoint</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-170">Le fichier est un fichier de point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-170">The file is a checkpoint file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-171">JET_filetypeTempDatabase</span><span class="sxs-lookup"><span data-stu-id="2dbc4-171">JET_filetypeTempDatabase</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-172">Le fichier est un fichier de base de données temporaire.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-172">The file is a temporary database file.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2dbc4-173">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2dbc4-173">Return Value</span></span>

<span data-ttu-id="2dbc4-174">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-174">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2dbc4-175">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2dbc4-175">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dbc4-176">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2dbc4-176">Return code</span></span></p></th>
<th><p><span data-ttu-id="2dbc4-177">Description</span><span class="sxs-lookup"><span data-stu-id="2dbc4-177">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-178">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2dbc4-178">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-179">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-179">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-180">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="2dbc4-180">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-181">Le <em>InfoLevel</em> demandé a été JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-181">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="2dbc4-182">Cela n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-182">This is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-183">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="2dbc4-183">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-184">La mémoire tampon fournie dans <em>cbMax</em> est trop petite pour les informations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-184">The buffer that is given in <em>cbMax</em> is too small for the desired information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-185">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="2dbc4-185">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-186">La mémoire tampon fournie dans <em>cbMax</em> n’est pas la taille correcte pour les informations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-186">The buffer that is given in <em>cbMax</em> is not the correct size for the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-187">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2dbc4-187">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2dbc4-188">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a produit un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-188">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="2dbc4-189">Cette erreur est retournée par <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> lorsque le dbid fourni n’est pas une base de données (attachée) valide.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-189">This error will be returned by <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when the DBID provided is not a valid (attached) database.</span></span> <span data-ttu-id="2dbc4-190">Cette erreur est retournée par <strong>JetGetDatabaseFileInfo</strong> et <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> lorsqu’un <em>InfoLevel</em> demandé n’est pas pris en charge par cette version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-190">This error will be returned by <strong>JetGetDatabaseFileInfo</strong> and <a href="gg294076(v=exchg.10).md">JetGetDatabaseInfo</a> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2dbc4-191">Si cette fonction est réussie, les données demandées sont retournées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-191">If this function succeeds, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="2dbc4-192">Si cette fonction échoue, la mémoire tampon de sortie est dans un État indéfini.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-192">If this function fails, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2dbc4-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dbc4-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-194"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2dbc4-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2dbc4-195">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-196"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2dbc4-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2dbc4-197">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-198"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2dbc4-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2dbc4-199">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-200"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="2dbc4-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2dbc4-201">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dbc4-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2dbc4-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2dbc4-203">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2dbc4-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dbc4-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2dbc4-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2dbc4-205">Implémenté en tant que <strong>JetGetDatabaseFileInfoW</strong> (Unicode) et <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2dbc4-205">Implemented as <strong>JetGetDatabaseFileInfoW</strong> (Unicode) and <strong>JetGetDatabaseFileInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2dbc4-206">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dbc4-206">See Also</span></span>

[<span data-ttu-id="2dbc4-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2dbc4-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2dbc4-208">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="2dbc4-208">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="2dbc4-209">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="2dbc4-209">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="2dbc4-210">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="2dbc4-210">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)
