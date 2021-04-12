---
description: 'En savoir plus sur : fonction JetGetDatabaseInfo'
title: Fonction JetGetDatabaseInfo
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81c414a1dd38f621ba86bf7b1c9ce87710801446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203134"
---
# <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="bb122-103">Fonction JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="bb122-103">JetGetDatabaseInfo Function</span></span>


<span data-ttu-id="bb122-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="bb122-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetdatabaseinfo-function"></a><span data-ttu-id="bb122-105">Fonction JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="bb122-105">JetGetDatabaseInfo Function</span></span>

<span data-ttu-id="bb122-106">La fonction **JetGetDatabaseInfo** récupère différents types d’informations sur la base de données.</span><span class="sxs-lookup"><span data-stu-id="bb122-106">The **JetGetDatabaseInfo** function retrieves various types of information about the database.</span></span> <span data-ttu-id="bb122-107">Cette API peut être appelée lorsqu’une base de données est attachée ou en ligne (avec **JetGetDatabaseInfo**) ou que la base de données ou le moteur de base de données est hors connexion (avec [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="bb122-107">This API can be called while a database is attached or online (with **JetGetDatabaseInfo**) or while the database or database engine is offline (with [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)).</span></span>

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="bb122-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb122-108">Parameters</span></span>

<span data-ttu-id="bb122-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bb122-109">*sesid*</span></span>

<span data-ttu-id="bb122-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="bb122-110">The session to use for this call.</span></span>

<span data-ttu-id="bb122-111">*dbid*</span><span class="sxs-lookup"><span data-stu-id="bb122-111">*dbid*</span></span>

<span data-ttu-id="bb122-112">[JET_DBID](./jet-dbid.md) de la base de données à partir de laquelle récupérer les informations.</span><span class="sxs-lookup"><span data-stu-id="bb122-112">The [JET_DBID](./jet-dbid.md) for the database to retrieve the information from.</span></span>

<span data-ttu-id="bb122-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="bb122-113">*pvResult*</span></span>

<span data-ttu-id="bb122-114">Pointeur vers une mémoire tampon qui recevra les informations spécifiées.</span><span class="sxs-lookup"><span data-stu-id="bb122-114">Pointer to a buffer which will receive the specified information.</span></span> <span data-ttu-id="bb122-115">La taille de la mémoire tampon, en octets, est passée dans *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="bb122-115">The size of the buffer, in bytes, is passed in *cbMax*.</span></span>

<span data-ttu-id="bb122-116">En cas d’échec, le contenu de *pvResult* n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="bb122-116">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="bb122-117">Les informations stockées dans *pvResult* dépendent de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="bb122-117">The information stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="bb122-118">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="bb122-118">*cbMax*</span></span>

<span data-ttu-id="bb122-119">Taille, en octets, de la mémoire tampon qui a été passée dans *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="bb122-119">The size, in bytes, of the buffer that was passed in *pvResult*.</span></span>

<span data-ttu-id="bb122-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="bb122-120">*InfoLevel*</span></span>

<span data-ttu-id="bb122-121">*InfoLevel* spécifie le type d’informations à récupérer sur la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bb122-121">*InfoLevel* specifies which type of information should be retrieved about the specified database.</span></span> <span data-ttu-id="bb122-122">Cela affecte la façon dont *pvResult* est interprété.</span><span class="sxs-lookup"><span data-stu-id="bb122-122">It affects how *pvResult* is interpreted.</span></span> <span data-ttu-id="bb122-123">Certains *InfoLevel* sont disponibles uniquement dans la version hors connexion ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) ou en ligne (**JetGetDatabaseInfo**) de l’API.</span><span class="sxs-lookup"><span data-stu-id="bb122-123">Some *InfoLevel* are available only in the offline ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) or online (**JetGetDatabaseInfo**) version of the API.</span></span>

<span data-ttu-id="bb122-124">Si la mémoire tampon *pvResult* fournie est trop petite, JET_errInvalidBufferSize ou JET_errBufferTooSmall sont retournés en fonction du *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="bb122-124">If the *pvResult* buffer provided is too small, either JET_errInvalidBufferSize or JET_errBufferTooSmall will be returned depending on the *InfoLevel*.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb122-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb122-125">Value</span></span></p></th>
<th><p><span data-ttu-id="bb122-126">Signification</span><span class="sxs-lookup"><span data-stu-id="bb122-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb122-127">JET_DbInfoCollate</span><span class="sxs-lookup"><span data-stu-id="bb122-127">JET_DbInfoCollate</span></span></p></td>
<td><p><span data-ttu-id="bb122-128">Pas encore pris en charge et retournent les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb122-128">Not yet supported and return default values.</span></span> <span data-ttu-id="bb122-129">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="bb122-129">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-130">JET_DbInfoConnect</span><span class="sxs-lookup"><span data-stu-id="bb122-130">JET_DbInfoConnect</span></span></p></td>
<td><p><span data-ttu-id="bb122-131">Ces <em>InfoLevels</em> sont déconseillés et ne sont pas pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="bb122-131">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="bb122-132">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="bb122-132">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-133">JET_DbInfoCountry</span><span class="sxs-lookup"><span data-stu-id="bb122-133">JET_DbInfoCountry</span></span></p></td>
<td><p><span data-ttu-id="bb122-134">Pas encore pris en charge et retournent les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb122-134">Not yet supported and return default values.</span></span> <span data-ttu-id="bb122-135">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="bb122-135">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-136">JET_DbInfoCp</span><span class="sxs-lookup"><span data-stu-id="bb122-136">JET_DbInfoCp</span></span></p></td>
<td><p><span data-ttu-id="bb122-137">Pas encore pris en charge et retournent les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb122-137">Not yet supported and return default values.</span></span> <span data-ttu-id="bb122-138">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="bb122-138">Do not use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-139">JET_DbInfoFilename</span><span class="sxs-lookup"><span data-stu-id="bb122-139">JET_DbInfoFilename</span></span></p></td>
<td><p><span data-ttu-id="bb122-140"><em>pvResult</em> sera interprété comme une mémoire tampon de chaîne (Char \*).</span><span class="sxs-lookup"><span data-stu-id="bb122-140"><em>pvResult</em> will be interpreted as a string buffer (char \*).</span></span> <span data-ttu-id="bb122-141">Une mémoire tampon de MAX_PATH est suggérée, mais pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bb122-141">A MAX_PATH buffer is suggested, however not required.</span></span> <span data-ttu-id="bb122-142">Si la mémoire tampon n’est pas assez longue, JET_errBufferTooSmall est retourné.</span><span class="sxs-lookup"><span data-stu-id="bb122-142">If the buffer is not long enough, JET_errBufferTooSmall will be returned.</span></span> <span data-ttu-id="bb122-143">La chaîne sera remplie avec le chemin d’accès de la base de données pour ce DBID.</span><span class="sxs-lookup"><span data-stu-id="bb122-143">The string will be populated with the path of the database for this DBID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-144">JET_DbInfoFilesize</span><span class="sxs-lookup"><span data-stu-id="bb122-144">JET_DbInfoFilesize</span></span></p></td>
<td><p><span data-ttu-id="bb122-145"><em>pvResult</em> sera interprété comme un DWORD (4 octets).</span><span class="sxs-lookup"><span data-stu-id="bb122-145"><em>pvResult</em> will be interpreted as a DWORD (4 bytes).</span></span> <span data-ttu-id="bb122-146">Retourne la taille de la base de données en pages.</span><span class="sxs-lookup"><span data-stu-id="bb122-146">Returns the size of the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-147">JET_DbInfoIsam</span><span class="sxs-lookup"><span data-stu-id="bb122-147">JET_DbInfoIsam</span></span></p></td>
<td><p><span data-ttu-id="bb122-148">Ces <em>InfoLevels</em> sont déconseillés et ne sont pas pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="bb122-148">These <em>InfoLevels</em> are deprecated and are not currently supported.</span></span> <span data-ttu-id="bb122-149">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="bb122-149">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-150">JET_DbInfoLCID</span><span class="sxs-lookup"><span data-stu-id="bb122-150">JET_DbInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="bb122-151">(Windows XP et versions ultérieures) Ce <em>InfoLevel</em> a été initialement spécifié comme suit : JET_DbInfoLangid (Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="bb122-151">(Windows XP and later) This <em>InfoLevel</em> was originally specified as: JET_DbInfoLangid (Windows 2000)</span></span></p>
<p><span data-ttu-id="bb122-152"><em>pvResult</em> sera interprété comme long.</span><span class="sxs-lookup"><span data-stu-id="bb122-152"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="bb122-153">Cela retourne l’identificateur de paramètres régionaux (LCID) associé à cette base de données.</span><span class="sxs-lookup"><span data-stu-id="bb122-153">This returns the Locale identifier (LCID) associate with this database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-154">JET_DbInfoMisc</span><span class="sxs-lookup"><span data-stu-id="bb122-154">JET_DbInfoMisc</span></span></p></td>
<td><p><span data-ttu-id="bb122-155"><em>pvResult</em> sera interprété comme un <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span><span class="sxs-lookup"><span data-stu-id="bb122-155"><em>pvResult</em> will be interpreted as a <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>.</span></span> <span data-ttu-id="bb122-156">La structure <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> sera remplie avec les informations relatives à la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bb122-156">The <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a> structure will be populated with information pertaining to the database specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-157">JET_DbInfoOptions</span><span class="sxs-lookup"><span data-stu-id="bb122-157">JET_DbInfoOptions</span></span></p></td>
<td><p><span data-ttu-id="bb122-158"><em>pvResult</em> sera interprété comme un <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span><span class="sxs-lookup"><span data-stu-id="bb122-158"><em>pvResult</em> will be interpreted as a <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> (DWORD).</span></span> <span data-ttu-id="bb122-159">Cela indique si la base de données est ouverte en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="bb122-159">This returns whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="bb122-160">Si la base de données est en mode exclusif JET_bitDbExclusive sera définie dans le <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> fourni, sinon zéro est défini.</span><span class="sxs-lookup"><span data-stu-id="bb122-160">If the database is in exclusive mode JET_bitDbExclusive will be set in the <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> provided, otherwise zero is set.</span></span> <span data-ttu-id="bb122-161">Notez que les autres options de base de données <em>Grbit</em> pour <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> et <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> ne sont pas renvoyées.</span><span class="sxs-lookup"><span data-stu-id="bb122-161">Note other database <em>grbit</em> options for <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> and <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a> are not returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-162">JET_DbInfoPageSize</span><span class="sxs-lookup"><span data-stu-id="bb122-162">JET_DbInfoPageSize</span></span></p></td>
<td><p><span data-ttu-id="bb122-163">Disponible uniquement sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bb122-163">Available only on Windows XP and later.</span></span> <span data-ttu-id="bb122-164"><em>pvResult</em> sera interprété comme un entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="bb122-164"><em>pvResult</em> will be interpreted as a unsigned long.</span></span> <span data-ttu-id="bb122-165">Cela renverra la taille de page de la base de données en octets.</span><span class="sxs-lookup"><span data-stu-id="bb122-165">This will return the page size of the database in bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-166">JET_DbInfoSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="bb122-166">JET_DbInfoSpaceAvailable</span></span></p></td>
<td><p><span data-ttu-id="bb122-167"><em>pvResult</em> sera interprété comme un DWORD.</span><span class="sxs-lookup"><span data-stu-id="bb122-167"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="bb122-168">Cela retourne l’espace disponible pour la base de données dans les pages.</span><span class="sxs-lookup"><span data-stu-id="bb122-168">This returns the available space for the database in pages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-169">JET_DbInfoSpaceOwned</span><span class="sxs-lookup"><span data-stu-id="bb122-169">JET_DbInfoSpaceOwned</span></span></p></td>
<td><p><span data-ttu-id="bb122-170"><em>pvResult</em> sera interprété comme un DWORD.</span><span class="sxs-lookup"><span data-stu-id="bb122-170"><em>pvResult</em> will be interpreted as a DWORD.</span></span> <span data-ttu-id="bb122-171">Cela retourne l’espace détenu pour la base de données dans les pages.</span><span class="sxs-lookup"><span data-stu-id="bb122-171">This returns the owned space for the database in pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-172">JET_DbInfoTransactions</span><span class="sxs-lookup"><span data-stu-id="bb122-172">JET_DbInfoTransactions</span></span></p></td>
<td><p><span data-ttu-id="bb122-173"><em>pvResult</em> sera interprété comme long.</span><span class="sxs-lookup"><span data-stu-id="bb122-173"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="bb122-174">Cela retourne une valeur supérieure au niveau maximal dans lequel les transactions peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="bb122-174">This will return one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="bb122-175">Si <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> est appelé (de manière imbriquée, autrement dit, sur la même session, sans validation ou ROLLBACK) autant de fois que cette valeur, sur le dernier appel JET_errTransTooDeep est retourné à partir de <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span><span class="sxs-lookup"><span data-stu-id="bb122-175">If <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call JET_errTransTooDeep will be returned from <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>.</span></span> <span data-ttu-id="bb122-176">Notez que la valeur dans Windows 2000, Windows XP et Windows Server 2003 est 7.</span><span class="sxs-lookup"><span data-stu-id="bb122-176">Note the value in Windows 2000, Windows XP, and Windows Server 2003 is 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-177">JET_DbInfoVersion</span><span class="sxs-lookup"><span data-stu-id="bb122-177">JET_DbInfoVersion</span></span></p></td>
<td><p><span data-ttu-id="bb122-178"><em>pvResult</em> sera interprété comme long.</span><span class="sxs-lookup"><span data-stu-id="bb122-178"><em>pvResult</em> will be interpreted as a long.</span></span> <span data-ttu-id="bb122-179">Cela retourne la version principale native du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="bb122-179">This returns the database engine's native major version.</span></span> <span data-ttu-id="bb122-180">Cette valeur est 0x620 pour Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb122-180">This value is 0x620 for Windows 2000, Windows XP, and Windows Server 2003.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="bb122-181">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb122-181">Return Value</span></span>

<span data-ttu-id="bb122-182">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="bb122-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bb122-183">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bb122-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb122-184">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bb122-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="bb122-185">Description</span><span class="sxs-lookup"><span data-stu-id="bb122-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb122-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bb122-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bb122-187">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bb122-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-188">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="bb122-188">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="bb122-189">La taille de la mémoire tampon donnée dans <em>cbMax</em> est trop petite (ou incorrecte) pour contenir les informations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="bb122-189">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-190">JET_errFeatureNotAvailable</span><span class="sxs-lookup"><span data-stu-id="bb122-190">JET_errFeatureNotAvailable</span></span></p></td>
<td><p><span data-ttu-id="bb122-191">Le <em>InfoLevel</em> demandé a été JET_DbInfoIsam.</span><span class="sxs-lookup"><span data-stu-id="bb122-191">The <em>InfoLevel</em> requested was JET_DbInfoIsam.</span></span> <span data-ttu-id="bb122-192">Cela n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bb122-192">This is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-193">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="bb122-193">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="bb122-194">La taille de la mémoire tampon donnée dans <em>cbMax</em> est trop petite (ou incorrecte) pour contenir les informations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="bb122-194">The size of the buffer given in <em>cbMax</em> was too small (or not correct) to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-195">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="bb122-195">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="bb122-196">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="bb122-196">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="bb122-197">Cette erreur est retournée par <strong>JetGetDatabaseInfo</strong> lorsque le <a href="gg269248(v=exchg.10).md">JET_DBID</a> fourni n’est pas une base de données (attachée) valide.</span><span class="sxs-lookup"><span data-stu-id="bb122-197">This error will be returned by <strong>JetGetDatabaseInfo</strong> when the <a href="gg269248(v=exchg.10).md">JET_DBID</a> provided is not a valid (attached) database.</span></span> <span data-ttu-id="bb122-198">Cette erreur est retournée par <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> et <strong>JetGetDatabaseInfo</strong> lorsqu’un <em>InfoLevel</em> demandé n’est pas pris en charge par cette version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="bb122-198">This error will be returned by <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a> and <strong>JetGetDatabaseInfo</strong> when an <em>InfoLevel</em> requested is not supported by that version of the function.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bb122-199">En cas de réussite, les données demandées sont retournées dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="bb122-199">On success, the requested data will be returned in the output buffer.</span></span>

<span data-ttu-id="bb122-200">En cas d’échec, la mémoire tampon de sortie est dans un État indéfini.</span><span class="sxs-lookup"><span data-stu-id="bb122-200">On failure, the output buffer will be in an undefined state.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bb122-201">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb122-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb122-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bb122-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bb122-203">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="bb122-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-204"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="bb122-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bb122-205">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bb122-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-206"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="bb122-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bb122-207">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="bb122-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-208"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="bb122-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bb122-209">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bb122-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb122-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bb122-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bb122-211">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bb122-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb122-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bb122-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bb122-213">Implémenté en tant que <strong>JetGetDatabaseInfoW</strong> (Unicode) et <strong>JetGetDatabaseInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bb122-213">Implemented as <strong>JetGetDatabaseInfoW</strong> (Unicode) and <strong>JetGetDatabaseInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bb122-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb122-214">See Also</span></span>

[<span data-ttu-id="bb122-215">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="bb122-215">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="bb122-216">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bb122-216">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bb122-217">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bb122-217">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bb122-218">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bb122-218">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bb122-219">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="bb122-219">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)  
[<span data-ttu-id="bb122-220">JET_DBINFOUPGRADE</span><span class="sxs-lookup"><span data-stu-id="bb122-220">JET_DBINFOUPGRADE</span></span>](./jet-dbinfoupgrade-structure.md)  
[<span data-ttu-id="bb122-221">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="bb122-221">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
