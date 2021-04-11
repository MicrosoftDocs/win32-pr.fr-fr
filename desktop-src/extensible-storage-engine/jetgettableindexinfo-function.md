---
description: 'En savoir plus sur : fonction JetGetTableIndexInfo'
title: Fonction JetGetTableIndexInfo
TOCTitle: JetGetTableIndexInfo Function
ms:assetid: d250d254-2b10-4fe7-bbb1-72bb967f22dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294102(v=EXCHG.10)
ms:contentKeyID: 32765717
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableIndexInfoW
- JetGetTableIndexInfoA
- JetGetTableIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 904391218fbd073cd273655ce74fdec116b6a22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210836"
---
# <a name="jetgettableindexinfo-function"></a><span data-ttu-id="cb5a4-103">Fonction JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="cb5a4-103">JetGetTableIndexInfo Function</span></span>


<span data-ttu-id="cb5a4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="cb5a4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettableindexinfo-function"></a><span data-ttu-id="cb5a4-105">Fonction JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="cb5a4-105">JetGetTableIndexInfo Function</span></span>

<span data-ttu-id="cb5a4-106">La fonction **JetGetTableIndexInfo** récupère des informations sur un index.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-106">The **JetGetTableIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetTableIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="cb5a4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb5a4-107">Parameters</span></span>

<span data-ttu-id="cb5a4-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="cb5a4-108">*sesid*</span></span>

<span data-ttu-id="cb5a4-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="cb5a4-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="cb5a4-110">*tableid*</span></span>

<span data-ttu-id="cb5a4-111">Table de base de données qui contient l’index qui contient les informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-111">The database table that contains the index that holds the needed information.</span></span>

<span data-ttu-id="cb5a4-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="cb5a4-112">*szIndexName*</span></span>

<span data-ttu-id="cb5a4-113">Nom de l’index qui contient les informations qui seront récupérées.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-113">The name of the index that contains information that will be retrieved.</span></span>

<span data-ttu-id="cb5a4-114">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="cb5a4-114">*pvResult*</span></span>

<span data-ttu-id="cb5a4-115">Pointeur vers une mémoire tampon qui recevra les informations.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-115">Pointer to a buffer which will receive the information.</span></span> <span data-ttu-id="cb5a4-116">La mémoire tampon doit être alignée pour contenir le type requis.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-116">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="cb5a4-117">Le type de la mémoire tampon dépend du paramètre *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="cb5a4-117">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="cb5a4-118">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="cb5a4-118">*cbResult*</span></span>

<span data-ttu-id="cb5a4-119">Taille, en octets, de la mémoire tampon passée dans le paramètre *pvResult* .</span><span class="sxs-lookup"><span data-stu-id="cb5a4-119">The size, in bytes, of the buffer passed in the *pvResult* parameter.</span></span>

<span data-ttu-id="cb5a4-120">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="cb5a4-120">*InfoLevel*</span></span>

<span data-ttu-id="cb5a4-121">Spécifie les informations qui seront stockées dans *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-121">Specifies which information will be stored in *pvResult*.</span></span> <span data-ttu-id="cb5a4-122">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cb5a4-122">The valid values are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb5a4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb5a4-123">Value</span></span></p></th>
<th><p><span data-ttu-id="cb5a4-124">Signification</span><span class="sxs-lookup"><span data-stu-id="cb5a4-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-125">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="cb5a4-125">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-126"><em>pvResult</em> est interprété comme une structure de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="cb5a4-126"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="cb5a4-127">En cas de réussite, la structure <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> reçoit des informations sur l’index.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-127">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="cb5a4-128">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-128">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-129">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="cb5a4-129">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-130"><em>pvResult</em> est interprété comme un LCID.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-130"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="cb5a4-131">En cas de réussite, le LCID contient l’identificateur de paramètres régionaux de l’index.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-131">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="cb5a4-132">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-132">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-133">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="cb5a4-133">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-134"><em>pvResult</em> est interprété comme une structure de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="cb5a4-134"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="cb5a4-135">En cas de réussite, la structure <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> reçoit des informations sur l’index.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-135">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="cb5a4-136">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-136">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-137">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="cb5a4-137">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-138">JET_IdxInfoOLC est obsolète.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-138">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-139">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="cb5a4-139">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-140">JET_IdxInfoResetOLC est obsolète.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-140">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-141">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="cb5a4-141">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-142"><em>pvResult</em> est interprété comme ulong.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-142"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="cb5a4-143">En cas de réussite, ULONG conserve l’utilisation de l’espace de l’index.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-143">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="cb5a4-144">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-144">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-145">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="cb5a4-145">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-146">JET_IdxInfoSysTabCursor est obsolète.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-146">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-147">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="cb5a4-147">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-148">JET_IdxInfoLangid est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-148">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="cb5a4-149">Utilisez à la place JET_IdxInfoLCID et la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</span><span class="sxs-lookup"><span data-stu-id="cb5a4-149">Use JET_IdxInfoLCID instead, and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-150">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="cb5a4-150">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-151"><em>pvResult</em> est interprété comme ulong.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-151"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="cb5a4-152">En cas de réussite, ULONG conserve le nombre d’index sur la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-152">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="cb5a4-153"><em>szIndexName</em> est ignoré.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-153"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="cb5a4-154">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-154">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-155">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="cb5a4-155">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-156"><em>pvResult</em> est interprété comme un UShort.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-156"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="cb5a4-157">En cas de réussite, le USHORT contient la valeur de <em>cbVarSegMac</em> utilisée lors de la création de l’index.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-157">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="cb5a4-158">Consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> pour obtenir une description de <em>cbVarSegMac</em>.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-158">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="cb5a4-159">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-160">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="cb5a4-160">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-161"><em>pvResult</em> est interprété comme un <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-161"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="cb5a4-162">En cas de réussite, la structure <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> reçoit des informations sur l’index.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-162">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="cb5a4-163">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-163">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-164">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="cb5a4-164">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-165"><em>pvResult</em> est interprété comme un UShort.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-165"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="cb5a4-166">En cas de réussite, le USHORT contient la valeur de cbKeyMost utilisée lors de la création de l’index.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-166">On success, the USHORT holds the value of cbKeyMost used when the index was created.</span></span> <span data-ttu-id="cb5a4-167">Consultez la structure <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> pour obtenir une description de cbKeyMost.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-167">See the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure for a description of cbKeyMost.</span></span> <span data-ttu-id="cb5a4-168">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-168">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-169">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="cb5a4-169">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-170"><em>pvResult</em> est interprété comme une structure de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="cb5a4-170"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="cb5a4-171">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="cb5a4-172"><strong>Windows 7 :  </strong> JET_IdxInfoCreateIndex est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-172"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-173">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="cb5a4-173">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-174"><em>pvResult</em> est interprété comme une structure de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="cb5a4-174"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="cb5a4-175">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="cb5a4-176"><strong>Windows 7 :  </strong> JET_IdxInfoCreateIndex2 est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="cb5a4-177">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cb5a4-177">Return Value</span></span>

<span data-ttu-id="cb5a4-178">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-178">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cb5a4-179">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cb5a4-179">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb5a4-180">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cb5a4-180">Return code</span></span></p></th>
<th><p><span data-ttu-id="cb5a4-181">Description</span><span class="sxs-lookup"><span data-stu-id="cb5a4-181">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-182">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cb5a4-182">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-183">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-183">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-184">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="cb5a4-184">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-185">L’index spécifié est introuvable dans la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-185">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-186">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="cb5a4-186">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="cb5a4-187">La mémoire tampon transmise en tant que <em>pvResult</em> est trop petite.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-187">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="cb5a4-188">Le contenu de la mémoire tampon n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-188">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="cb5a4-189">Notes</span><span class="sxs-lookup"><span data-stu-id="cb5a4-189">Remarks</span></span>

<span data-ttu-id="cb5a4-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) et **JetGetTableIndexInfo** récupèrent des informations identiques sur un index.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-190">[JetGetIndexInfo](./jetgetindexinfo-function.md) and **JetGetTableIndexInfo** retrieve identical information about an index.</span></span> <span data-ttu-id="cb5a4-191">La différence réside dans le mode de spécification de la table.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-191">The difference is in how the table is specified.</span></span> <span data-ttu-id="cb5a4-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) attend une base de données (*dbid*) et un nom de table (*szTableName*), tandis que **JetGetTableIndexInfo** attend un identificateur de table (*TableID*).</span><span class="sxs-lookup"><span data-stu-id="cb5a4-192">[JetGetIndexInfo](./jetgetindexinfo-function.md) expects a database (*dbid*) and name of a table (*szTableName*), while **JetGetTableIndexInfo** expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="cb5a4-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb5a4-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-194"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cb5a4-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cb5a4-195">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-195">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-196"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="cb5a4-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cb5a4-197">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-197">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-198"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="cb5a4-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cb5a4-199">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-200"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="cb5a4-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cb5a4-201">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb5a4-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cb5a4-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cb5a4-203">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cb5a4-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb5a4-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="cb5a4-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cb5a4-205">Implémenté en tant que <strong>JetGetTableIndexInfoW</strong> (Unicode) et <strong>JetGetTableIndexInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cb5a4-205">Implemented as <strong>JetGetTableIndexInfoW</strong> (Unicode) and <strong>JetGetTableIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cb5a4-206">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb5a4-206">See Also</span></span>

[<span data-ttu-id="cb5a4-207">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="cb5a4-207">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="cb5a4-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cb5a4-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cb5a4-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cb5a4-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="cb5a4-210">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="cb5a4-210">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="cb5a4-211">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="cb5a4-211">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="cb5a4-212">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="cb5a4-212">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="cb5a4-213">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="cb5a4-213">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="cb5a4-214">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="cb5a4-214">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)
