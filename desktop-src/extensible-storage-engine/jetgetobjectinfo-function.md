---
description: 'En savoir plus sur : fonction JetGetObjectInfo'
title: JetGetObjectInfo, fonction
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf4c3c9806d4dcf898d6daeb903eb6fc4322fee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538899"
---
# <a name="jetgetobjectinfo-function"></a><span data-ttu-id="dc540-103">JetGetObjectInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="dc540-103">JetGetObjectInfo Function</span></span>


<span data-ttu-id="dc540-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="dc540-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetobjectinfo-function"></a><span data-ttu-id="dc540-105">JetGetObjectInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="dc540-105">JetGetObjectInfo Function</span></span>

<span data-ttu-id="dc540-106">La fonction **JetGetObjectInfo** récupère des informations sur les objets de base de données.</span><span class="sxs-lookup"><span data-stu-id="dc540-106">The **JetGetObjectInfo** function retrieves information about database objects.</span></span> <span data-ttu-id="dc540-107">Actuellement, seules les tables sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="dc540-107">Currently, only tables are supported.</span></span> <span data-ttu-id="dc540-108">[JetGetTableInfo](./jetgettableinfo-function.md) peut être utilisé pour extraire plus d’informations que **JetGetObjectInfo**.</span><span class="sxs-lookup"><span data-stu-id="dc540-108">[JetGetTableInfo](./jetgettableinfo-function.md) can be used to fetch more information than **JetGetObjectInfo**.</span></span>

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="dc540-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc540-109">Parameters</span></span>

<span data-ttu-id="dc540-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="dc540-110">*sesid*</span></span>

<span data-ttu-id="dc540-111">Contexte de la session de base de données à utiliser.</span><span class="sxs-lookup"><span data-stu-id="dc540-111">The database session context to use.</span></span>

<span data-ttu-id="dc540-112">*dbid*</span><span class="sxs-lookup"><span data-stu-id="dc540-112">*dbid*</span></span>

<span data-ttu-id="dc540-113">Base de données à partir de laquelle les informations sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="dc540-113">The database from which the information is retrieved.</span></span>

<span data-ttu-id="dc540-114">*objtyp*</span><span class="sxs-lookup"><span data-stu-id="dc540-114">*objtyp*</span></span>

<span data-ttu-id="dc540-115">Objets qui contiennent des informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="dc540-115">The objects that contain information to be retrieved.</span></span> <span data-ttu-id="dc540-116">À l’heure actuelle, seuls les JET_objtypNil et les JET_objtypTable sont pris en charge, tous deux ayant un comportement identique.</span><span class="sxs-lookup"><span data-stu-id="dc540-116">Currently, only JET_objtypNil and JET_objtypTable are supported, both of which behave identically.</span></span> <span data-ttu-id="dc540-117">Seules les tables seront récupérées.</span><span class="sxs-lookup"><span data-stu-id="dc540-117">Only tables will be retrieved.</span></span>

<span data-ttu-id="dc540-118">*szContainerName*</span><span class="sxs-lookup"><span data-stu-id="dc540-118">*szContainerName*</span></span>

<span data-ttu-id="dc540-119">Ce paramètre est réservé pour une utilisation ultérieure et passe la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="dc540-119">This parameter is reserved for future use and passes **NULL**.</span></span> <span data-ttu-id="dc540-120">Nom des types d’objets à propos desquels récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="dc540-120">The name of the types of objects about which to retrieve information.</span></span>

<span data-ttu-id="dc540-121">*szObjectName*</span><span class="sxs-lookup"><span data-stu-id="dc540-121">*szObjectName*</span></span>

<span data-ttu-id="dc540-122">Nom de l’objet qui contient les informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="dc540-122">The name of the object that contains information to retrieve.</span></span> <span data-ttu-id="dc540-123">Quand *InfoLevel* utilise les options JET_ObjInfoList ou JET_ObjInfoListNoStats pour récupérer une liste de tous les objets, cette valeur doit être **null** ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="dc540-123">When *InfoLevel* uses the JET_ObjInfoList or JET_ObjInfoListNoStats options to retrieve a list of all objects, this value should be **NULL** or an empty string.</span></span>

<span data-ttu-id="dc540-124">Seuls les noms de tables sont actuellement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="dc540-124">Only table names are currently supported.</span></span>

<span data-ttu-id="dc540-125">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="dc540-125">*pvResult*</span></span>

<span data-ttu-id="dc540-126">Pointeur vers une mémoire tampon qui reçoit les informations spécifiées.</span><span class="sxs-lookup"><span data-stu-id="dc540-126">Pointer to a buffer which receives the specified information.</span></span>

<span data-ttu-id="dc540-127">La taille de la mémoire tampon, en octets, est passée dans *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="dc540-127">The size of the buffer, in bytes, is passed in *cbMax*.</span></span> <span data-ttu-id="dc540-128">En cas d’échec, le contenu de *pvResult* n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="dc540-128">On failure the contents of *pvResult* are undefined.</span></span>

<span data-ttu-id="dc540-129">Les informations stockées dans *pvResult* dépendent de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="dc540-129">The information that is stored in *pvResult* depends on *InfoLevel*.</span></span>

<span data-ttu-id="dc540-130">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="dc540-130">*cbMax*</span></span>

<span data-ttu-id="dc540-131">Taille, en octets, de la mémoire tampon passée dans *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="dc540-131">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="dc540-132">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="dc540-132">*InfoLevel*</span></span>

<span data-ttu-id="dc540-133">Spécifie le type d’informations à récupérer pour l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="dc540-133">Specifies which type of information to retrieve for the specified object.</span></span> <span data-ttu-id="dc540-134">Cela affecte la façon dont *pvResult* est interprété.</span><span class="sxs-lookup"><span data-stu-id="dc540-134">It affects how *pvResult* is interpreted.</span></span>

<span data-ttu-id="dc540-135">Les options suivantes peuvent être définies pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="dc540-135">The following options are available to set for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc540-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc540-136">Value</span></span></p></th>
<th><p><span data-ttu-id="dc540-137">Signification</span><span class="sxs-lookup"><span data-stu-id="dc540-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc540-138">JET_ObjInfo</span><span class="sxs-lookup"><span data-stu-id="dc540-138">JET_ObjInfo</span></span></p></td>
<td><p><span data-ttu-id="dc540-139"><em>pvResult</em> est interprété comme une structure de <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="dc540-139"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure.</span></span></p>
<p><span data-ttu-id="dc540-140">La structure <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> est remplie avec les informations relatives à l’objet nommé dans <em>szObjectName</em>.</span><span class="sxs-lookup"><span data-stu-id="dc540-140">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure is populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="dc540-141">Si l’appelant ne souhaite pas connaître le nombre d’enregistrements et de pages pour l’objet, envisagez d’utiliser JET_ObjInfoNoStats niveau d’informations, ce qui peut être plus rapide, car les statistiques ne sont pas incluses.</span><span class="sxs-lookup"><span data-stu-id="dc540-141">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoNoStats information level, which might be faster since statistics are not included.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc540-142">JET_ObjInfoList</span><span class="sxs-lookup"><span data-stu-id="dc540-142">JET_ObjInfoList</span></span></p></td>
<td><p><span data-ttu-id="dc540-143"><em>pvResult</em> est interprété comme une structure de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="dc540-143"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="dc540-144">Les informations sur tous les objets sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="dc540-144">Information about all objects is retrieved.</span></span> <span data-ttu-id="dc540-145">Une table temporaire est créée, et les informations nécessaires pour parcourir la table temporaire sont décrites dans la structure <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="dc540-145">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="dc540-146">Pour plus d’informations, consultez <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="dc540-146">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="dc540-147">Si l’appelant ne souhaite pas connaître le nombre d’enregistrements et de pages de l’objet, envisagez d’utiliser JET_ObjInfoListNoStats, ce qui peut être plus rapide.</span><span class="sxs-lookup"><span data-stu-id="dc540-147">If the caller does not want to know the number of records and pages for the object, consider using JET_ObjInfoListNoStats, which might be faster.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc540-148">JET_ObjInfoListACM</span><span class="sxs-lookup"><span data-stu-id="dc540-148">JET_ObjInfoListACM</span></span></p></td>
<td><p><span data-ttu-id="dc540-149">Déconseillé et non pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="dc540-149">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc540-150">JET_ObjInfoListNoStats</span><span class="sxs-lookup"><span data-stu-id="dc540-150">JET_ObjInfoListNoStats</span></span></p></td>
<td><p><span data-ttu-id="dc540-151"><em>pvResult</em> est interprété comme une structure de <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="dc540-151"><em>pvResult</em> is interpreted as a <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="dc540-152">Les informations sur tous les objets sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="dc540-152">Information about all objects is retrieved.</span></span> <span data-ttu-id="dc540-153">Une table temporaire est créée, et les informations nécessaires pour parcourir la table temporaire sont décrites dans la structure <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="dc540-153">A temporary table will be created, and the information that is necessary to traverse the temporary table is described in the <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> structure.</span></span> <span data-ttu-id="dc540-154">Pour plus d’informations, consultez <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span><span class="sxs-lookup"><span data-stu-id="dc540-154">For more information, see <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>.</span></span> <span data-ttu-id="dc540-155">JET_ObjInfoListNoStats est identique à JET_ObjInfoList, sauf que les colonnes qui indiquent le nombre d’enregistrements (<em>columnidcRecord</em>) et les pages (<em>columnidcPage</em>) ne seront pas mises à jour.</span><span class="sxs-lookup"><span data-stu-id="dc540-155">JET_ObjInfoListNoStats is identical to JET_ObjInfoList, except that the columns that report the number of records (<em>columnidcRecord</em>) and pages (<em>columnidcPage</em>) will not be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc540-156">JET_ObjInfoMax</span><span class="sxs-lookup"><span data-stu-id="dc540-156">JET_ObjInfoMax</span></span></p></td>
<td><p><span data-ttu-id="dc540-157"><em>pvResult</em> est interprété comme un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="dc540-157"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="dc540-158">La taille maximale de l’objet est de pages.</span><span class="sxs-lookup"><span data-stu-id="dc540-158">The maximum size of the object is in pages.</span></span> <span data-ttu-id="dc540-159">Actuellement, seules les tables sont retournées.</span><span class="sxs-lookup"><span data-stu-id="dc540-159">Currently only tables will be returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc540-160">JET_ObjInfoNoStats</span><span class="sxs-lookup"><span data-stu-id="dc540-160">JET_ObjInfoNoStats</span></span></p></td>
<td><p><span data-ttu-id="dc540-161"><em>pvResult</em> est interprété comme un <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="dc540-161"><em>pvResult</em> is interpreted as a <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>.</span></span> <span data-ttu-id="dc540-162">Les informations sur l’objet donné dans <em>szObjectName</em> sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="dc540-162">Information about only the object given in <em>szObjectName</em> will be retrieved.</span></span></p>
<p><span data-ttu-id="dc540-163">La structure <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> sera remplie avec les informations relatives à l’objet nommé dans <em>szObjectName</em>.</span><span class="sxs-lookup"><span data-stu-id="dc540-163">The <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> structure will be populated with information pertaining to the object that is named in <em>szObjectName</em>.</span></span></p>
<p><span data-ttu-id="dc540-164">JET_ObjInfoNoStats est identique à JET_ObjInfo, à ceci près que les champs qui indiquent le nombre d’enregistrements et de pages sont définis à zéro.</span><span class="sxs-lookup"><span data-stu-id="dc540-164">JET_ObjInfoNoStats is identical to JET_ObjInfo, except that the fields that report the number of records and pages are set to zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc540-165">JET_ObjInfoRulesLoaded</span><span class="sxs-lookup"><span data-stu-id="dc540-165">JET_ObjInfoRulesLoaded</span></span></p></td>
<td><p><span data-ttu-id="dc540-166">Déconseillé et non pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="dc540-166">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc540-167">JET_ObjInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="dc540-167">JET_ObjInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="dc540-168">Déconseillé et non pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="dc540-168">Deprecated and not currently supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc540-169">JET_ObjInfoSysTabReadOnly</span><span class="sxs-lookup"><span data-stu-id="dc540-169">JET_ObjInfoSysTabReadOnly</span></span></p></td>
<td><p><span data-ttu-id="dc540-170">Déconseillé et non pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="dc540-170">Deprecated and not currently supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="dc540-171">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dc540-171">Return Value</span></span>

<span data-ttu-id="dc540-172">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="dc540-172">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="dc540-173">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="dc540-173">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc540-174">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dc540-174">Return code</span></span></p></th>
<th><p><span data-ttu-id="dc540-175">Description</span><span class="sxs-lookup"><span data-stu-id="dc540-175">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc540-176">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="dc540-176">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="dc540-177">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="dc540-177">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc540-178">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="dc540-178">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="dc540-179">La taille de la mémoire tampon donnée dans <em>cbMax</em> est trop petite pour contenir les informations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="dc540-179">The size of the buffer given in <em>cbMax</em> was too small to hold the desired information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc540-180">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="dc540-180">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="dc540-181">Un nom non valide a été spécifié dans <em>szObjectName</em> ou <em>szContainerName</em>.</span><span class="sxs-lookup"><span data-stu-id="dc540-181">An invalid name was given in <em>szObjectName</em> or <em>szContainerName</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc540-182">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="dc540-182">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="dc540-183">Un paramètre incorrect a été donné.</span><span class="sxs-lookup"><span data-stu-id="dc540-183">A bad parameter was given.</span></span> <span data-ttu-id="dc540-184">Il est possible qu’un niveau incorrect a été passé à <em>InfoLevel</em>.</span><span class="sxs-lookup"><span data-stu-id="dc540-184">It is possible that a bad level was passed in to <em>InfoLevel</em>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="dc540-185">Notes</span><span class="sxs-lookup"><span data-stu-id="dc540-185">Remarks</span></span>

<span data-ttu-id="dc540-186">Si **JetGetObjectInfo** crée avec succès une table temporaire (par exemple, JET_ObjInfoList ou JET_ObjInfoNoStats), l’appelant est responsable de la fermeture de la table temporaire avec [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="dc540-186">If **JetGetObjectInfo** successfully creates a temporary table (for example, JET_ObjInfoList or JET_ObjInfoNoStats), the caller is responsible for closing the temporary table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="dc540-187">Actuellement, **JetGetObjectInfo** prend uniquement en charge la récupération d’informations sur les tables.</span><span class="sxs-lookup"><span data-stu-id="dc540-187">**JetGetObjectInfo** currently only supports retrieving information about tables.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dc540-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc540-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc540-189"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="dc540-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dc540-190">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="dc540-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc540-191"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="dc540-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dc540-192">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="dc540-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc540-193"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="dc540-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dc540-194">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="dc540-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc540-195"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="dc540-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dc540-196">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dc540-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc540-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="dc540-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dc540-198">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dc540-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc540-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="dc540-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="dc540-200">Implémenté en tant que <strong>JetGetObjectInfoW</strong> (Unicode) et <strong>JetGetObjectInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="dc540-200">Implemented as <strong>JetGetObjectInfoW</strong> (Unicode) and <strong>JetGetObjectInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dc540-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc540-201">See Also</span></span>

[<span data-ttu-id="dc540-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dc540-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dc540-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="dc540-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="dc540-204">JET_OBJTYP</span><span class="sxs-lookup"><span data-stu-id="dc540-204">JET_OBJTYP</span></span>](./jet-objtyp.md)  
[<span data-ttu-id="dc540-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dc540-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dc540-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="dc540-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="dc540-207">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="dc540-207">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="dc540-208">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="dc540-208">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="dc540-209">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="dc540-209">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="dc540-210">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="dc540-210">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)
