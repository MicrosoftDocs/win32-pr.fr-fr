---
description: 'En savoir plus sur : fonction JetGetIndexInfo'
title: Fonction JetGetIndexInfo
TOCTitle: JetGetIndexInfo Function
ms:assetid: c6235281-e208-4966-bc66-ec1ab27333c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294084(v=EXCHG.10)
ms:contentKeyID: 32765699
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetIndexInfoW
- JetGetIndexInfoA
- JetGetIndexInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0fd506390ba9f228c115d0b9142baffdbe1587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520044"
---
# <a name="jetgetindexinfo-function"></a><span data-ttu-id="f66d6-103">Fonction JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f66d6-103">JetGetIndexInfo Function</span></span>


<span data-ttu-id="f66d6-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f66d6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetindexinfo-function"></a><span data-ttu-id="f66d6-105">Fonction JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f66d6-105">JetGetIndexInfo Function</span></span>

<span data-ttu-id="f66d6-106">La fonction **JetGetIndexInfo** récupère des informations sur un index.</span><span class="sxs-lookup"><span data-stu-id="f66d6-106">The **JetGetIndexInfo** function retrieves information about an index.</span></span>

```cpp
    JET_ERR JET_API JetGetIndexInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          const tchar* szIndexName,
      __out         void* pvResult,
      __in          unsigned long cbResult,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="f66d6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f66d6-107">Parameters</span></span>

<span data-ttu-id="f66d6-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f66d6-108">*sesid*</span></span>

<span data-ttu-id="f66d6-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="f66d6-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="f66d6-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="f66d6-110">*dbid*</span></span>

<span data-ttu-id="f66d6-111">Identificateur de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="f66d6-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="f66d6-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="f66d6-112">*szTableName*</span></span>

<span data-ttu-id="f66d6-113">Nom de la table contenant l’index avec les informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f66d6-113">The name of the table containing the index with the information to retrieve.</span></span>

<span data-ttu-id="f66d6-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="f66d6-114">*szIndexName*</span></span>

<span data-ttu-id="f66d6-115">Nom de l’index avec les informations à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f66d6-115">The name of the index with the information to retrieve.</span></span>

<span data-ttu-id="f66d6-116">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="f66d6-116">*pvResult*</span></span>

<span data-ttu-id="f66d6-117">Pointeur vers une mémoire tampon qui recevra les informations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="f66d6-117">Pointer to a buffer that will receive the desired information.</span></span> <span data-ttu-id="f66d6-118">La mémoire tampon doit être alignée pour contenir le type requis.</span><span class="sxs-lookup"><span data-stu-id="f66d6-118">The buffer should be aligned to hold the type required.</span></span> <span data-ttu-id="f66d6-119">Le type de la mémoire tampon dépend du paramètre *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="f66d6-119">The type of the buffer is dependent on the *InfoLevel* parameter.</span></span>

<span data-ttu-id="f66d6-120">*cbResult*</span><span class="sxs-lookup"><span data-stu-id="f66d6-120">*cbResult*</span></span>

<span data-ttu-id="f66d6-121">Taille, en octets, de la mémoire tampon transmise en tant que *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="f66d6-121">The size, in bytes, of the buffer passed as *pvResult*.</span></span>

<span data-ttu-id="f66d6-122">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="f66d6-122">*InfoLevel*</span></span>

<span data-ttu-id="f66d6-123">Informations qui seront stockées dans *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="f66d6-123">The information that will be stored in *pvResult*.</span></span> <span data-ttu-id="f66d6-124">Les options suivantes peuvent être utilisées pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f66d6-124">The following options can be used for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f66d6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f66d6-125">Value</span></span></p></th>
<th><p><span data-ttu-id="f66d6-126">Signification</span><span class="sxs-lookup"><span data-stu-id="f66d6-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-127">JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="f66d6-127">JET_IdxInfo</span></span></p></td>
<td><p><span data-ttu-id="f66d6-128"><em>pvResult</em> est interprété comme une structure de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="f66d6-128"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="f66d6-129">En cas de réussite, la structure <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> reçoit des informations sur l’index.</span><span class="sxs-lookup"><span data-stu-id="f66d6-129">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="f66d6-130">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-130">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-131">JET_IdxInfoCount</span><span class="sxs-lookup"><span data-stu-id="f66d6-131">JET_IdxInfoCount</span></span></p></td>
<td><p><span data-ttu-id="f66d6-132"><em>pvResult</em> est interprété comme ulong.</span><span class="sxs-lookup"><span data-stu-id="f66d6-132"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="f66d6-133">En cas de réussite, ULONG conserve le nombre d’index sur la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f66d6-133">On success, the ULONG holds the count of indexes on the specified table.</span></span> <span data-ttu-id="f66d6-134"><em>szIndexName</em> est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f66d6-134"><em>szIndexName</em> is ignored.</span></span> <span data-ttu-id="f66d6-135">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-135">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-136">JET_IdxInfoIndexId</span><span class="sxs-lookup"><span data-stu-id="f66d6-136">JET_IdxInfoIndexId</span></span></p></td>
<td><p><span data-ttu-id="f66d6-137"><em>pvResult</em> est interprété comme un <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span><span class="sxs-lookup"><span data-stu-id="f66d6-137"><em>pvResult</em> is interpreted as a <a href="gg269327(v=exchg.10).md">JET_INDEXID</a>.</span></span> <span data-ttu-id="f66d6-138">En cas de réussite, la structure <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> reçoit des informations sur l’index.</span><span class="sxs-lookup"><span data-stu-id="f66d6-138">On success, the <a href="gg269327(v=exchg.10).md">JET_INDEXID</a> structure receives information about the index.</span></span> <span data-ttu-id="f66d6-139">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-139">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-140">JET_IdxInfoLangid</span><span class="sxs-lookup"><span data-stu-id="f66d6-140">JET_IdxInfoLangid</span></span></p></td>
<td><p><span data-ttu-id="f66d6-141">JET_IdxInfoLangid est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="f66d6-141">JET_IdxInfoLangid is deprecated.</span></span> <span data-ttu-id="f66d6-142">Utilisez à la place JET_IdxInfoLCID et la macro <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> .</span><span class="sxs-lookup"><span data-stu-id="f66d6-142">Use JET_IdxInfoLCID and the <a href="/windows/win32/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a> macro instead.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-143">JET_IdxInfoLCID</span><span class="sxs-lookup"><span data-stu-id="f66d6-143">JET_IdxInfoLCID</span></span></p></td>
<td><p><span data-ttu-id="f66d6-144"><em>pvResult</em> est interprété comme un LCID.</span><span class="sxs-lookup"><span data-stu-id="f66d6-144"><em>pvResult</em> is interpreted as an LCID.</span></span> <span data-ttu-id="f66d6-145">En cas de réussite, le LCID contient l’identificateur de paramètres régionaux de l’index.</span><span class="sxs-lookup"><span data-stu-id="f66d6-145">On success, the LCID holds the Locale Identifier of the index.</span></span> <span data-ttu-id="f66d6-146">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-146">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="f66d6-147"><strong>Windows XP :  </strong> JET_IdxInfoLCID est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f66d6-147"><strong>Windows XP:  </strong>JET_IdxInfoLCID is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-148">JET_IdxInfoList</span><span class="sxs-lookup"><span data-stu-id="f66d6-148">JET_IdxInfoList</span></span></p></td>
<td><p><span data-ttu-id="f66d6-149"><em>pvResult</em> est interprété comme une structure de <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> .</span><span class="sxs-lookup"><span data-stu-id="f66d6-149"><em>pvResult</em> is interpreted as a <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure.</span></span> <span data-ttu-id="f66d6-150">En cas de réussite, la structure <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> reçoit des informations sur l’index.</span><span class="sxs-lookup"><span data-stu-id="f66d6-150">On success, the <a href="gg269185(v=exchg.10).md">JET_INDEXLIST</a> structure receives information about the index.</span></span> <span data-ttu-id="f66d6-151">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-151">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-152">JET_IdxInfoOLC</span><span class="sxs-lookup"><span data-stu-id="f66d6-152">JET_IdxInfoOLC</span></span></p></td>
<td><p><span data-ttu-id="f66d6-153">JET_IdxInfoOLC est obsolète.</span><span class="sxs-lookup"><span data-stu-id="f66d6-153">JET_IdxInfoOLC is obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-154">JET_IdxInfoResetOLC</span><span class="sxs-lookup"><span data-stu-id="f66d6-154">JET_IdxInfoResetOLC</span></span></p></td>
<td><p><span data-ttu-id="f66d6-155">JET_IdxInfoResetOLC est obsolète.</span><span class="sxs-lookup"><span data-stu-id="f66d6-155">JET_IdxInfoResetOLC is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-156">JET_IdxInfoSpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="f66d6-156">JET_IdxInfoSpaceAlloc</span></span></p></td>
<td><p><span data-ttu-id="f66d6-157"><em>pvResult</em> est interprété comme ulong.</span><span class="sxs-lookup"><span data-stu-id="f66d6-157"><em>pvResult</em> is interpreted as a ULONG.</span></span> <span data-ttu-id="f66d6-158">En cas de réussite, ULONG conserve l’utilisation de l’espace de l’index.</span><span class="sxs-lookup"><span data-stu-id="f66d6-158">On success, the ULONG holds the space usage of the index.</span></span> <span data-ttu-id="f66d6-159">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-159">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-160">JET_IdxInfoSysTabCursor</span><span class="sxs-lookup"><span data-stu-id="f66d6-160">JET_IdxInfoSysTabCursor</span></span></p></td>
<td><p><span data-ttu-id="f66d6-161">JET_IdxInfoSysTabCursor est obsolète.</span><span class="sxs-lookup"><span data-stu-id="f66d6-161">JET_IdxInfoSysTabCursor is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-162">JET_IdxInfoVarSegMac</span><span class="sxs-lookup"><span data-stu-id="f66d6-162">JET_IdxInfoVarSegMac</span></span></p></td>
<td><p><span data-ttu-id="f66d6-163"><em>pvResult</em> est interprété comme un UShort.</span><span class="sxs-lookup"><span data-stu-id="f66d6-163"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="f66d6-164">En cas de réussite, le USHORT contient la valeur de <em>cbVarSegMac</em> utilisée lors de la création de l’index.</span><span class="sxs-lookup"><span data-stu-id="f66d6-164">On success, the USHORT holds the value of <em>cbVarSegMac</em> used when the index was created.</span></span> <span data-ttu-id="f66d6-165">Consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> pour obtenir une description de <em>cbVarSegMac</em>.</span><span class="sxs-lookup"><span data-stu-id="f66d6-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbVarSegMac</em>.</span></span> <span data-ttu-id="f66d6-166">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-166">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-167">JET_IdxInfoKeyMost</span><span class="sxs-lookup"><span data-stu-id="f66d6-167">JET_IdxInfoKeyMost</span></span></p></td>
<td><p><span data-ttu-id="f66d6-168"><em>pvResult</em> est interprété comme un UShort.</span><span class="sxs-lookup"><span data-stu-id="f66d6-168"><em>pvResult</em> is interpreted as a USHORT.</span></span> <span data-ttu-id="f66d6-169">En cas de réussite, le USHORT contient la valeur de <em>cbKeyMost</em> utilisée lors de la création de l’index.</span><span class="sxs-lookup"><span data-stu-id="f66d6-169">On success, the USHORT holds the value of <em>cbKeyMost</em> used when the index was created.</span></span> <span data-ttu-id="f66d6-170">Consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> pour obtenir une description de <em>cbKeyMost</em>.</span><span class="sxs-lookup"><span data-stu-id="f66d6-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a description of <em>cbKeyMost</em>.</span></span> <span data-ttu-id="f66d6-171">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-171">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="f66d6-172"><strong>Windows Vista :  </strong> JET_IdxInfoKeyMost est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f66d6-172"><strong>Windows Vista:  </strong>JET_IdxInfoKeyMost is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-173">JET_IdxInfoCreateIndex</span><span class="sxs-lookup"><span data-stu-id="f66d6-173">JET_IdxInfoCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="f66d6-174"><em>pvResult</em> est interprété comme une structure de <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="f66d6-174"><em>pvResult</em> is interpreted as a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="f66d6-175">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-175">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="f66d6-176"><strong>Windows 7 :  </strong> JET_IdxInfoCreateIndex est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f66d6-176"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-177">JET_IdxInfoCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="f66d6-177">JET_IdxInfoCreateIndex2</span></span></p></td>
<td><p><span data-ttu-id="f66d6-178"><em>pvResult</em> est interprété comme une structure de <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</span><span class="sxs-lookup"><span data-stu-id="f66d6-178"><em>pvResult</em> is interpreted as a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="f66d6-179">En cas d’échec, le contenu de <em>pvBuffer</em> n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-179">On failure, the contents of <em>pvBuffer</em> are undefined.</span></span></p>
<p><span data-ttu-id="f66d6-180"><strong>Windows 7 :  </strong> JET_IdxInfoCreateIndex2 est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f66d6-180"><strong>Windows 7:  </strong>JET_IdxInfoCreateIndex2 is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f66d6-181">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f66d6-181">Return Value</span></span>

<span data-ttu-id="f66d6-182">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="f66d6-182">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f66d6-183">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f66d6-183">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f66d6-184">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f66d6-184">Return code</span></span></p></th>
<th><p><span data-ttu-id="f66d6-185">Description</span><span class="sxs-lookup"><span data-stu-id="f66d6-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-186">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f66d6-186">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f66d6-187">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f66d6-187">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-188">JET_errIndexNotFound</span><span class="sxs-lookup"><span data-stu-id="f66d6-188">JET_errIndexNotFound</span></span></p></td>
<td><p><span data-ttu-id="f66d6-189">L’index spécifié est introuvable dans la table spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f66d6-189">The specified index cannot be found in the specified table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-190">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="f66d6-190">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="f66d6-191">La mémoire tampon transmise en tant que <em>pvResult</em> est trop petite.</span><span class="sxs-lookup"><span data-stu-id="f66d6-191">The buffer passed in as <em>pvResult</em> was too small.</span></span> <span data-ttu-id="f66d6-192">Le contenu de la mémoire tampon n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f66d6-192">The contents of the buffer are undefined.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="f66d6-193">Notes</span><span class="sxs-lookup"><span data-stu-id="f66d6-193">Remarks</span></span>

<span data-ttu-id="f66d6-194">**JetGetIndexInfo** et [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) récupèrent des informations identiques sur un index.</span><span class="sxs-lookup"><span data-stu-id="f66d6-194">**JetGetIndexInfo** and [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) retrieve identical information about an index.</span></span> <span data-ttu-id="f66d6-195">La différence réside dans le mode de spécification de la table.</span><span class="sxs-lookup"><span data-stu-id="f66d6-195">The difference is in how the table is specified.</span></span> <span data-ttu-id="f66d6-196">**JetGetIndexInfo** attend une base de données (*dbid*) et un nom de table (*szTableName*), tandis que [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) attend un identificateur de table (*TableID*).</span><span class="sxs-lookup"><span data-stu-id="f66d6-196">**JetGetIndexInfo** expects a database (*dbid*) and name of a table (*szTableName*), while [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) expects a table identifier (*tableid*).</span></span>

#### <a name="requirements"></a><span data-ttu-id="f66d6-197">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f66d6-197">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-198"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f66d6-198"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f66d6-199">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f66d6-199">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-200"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f66d6-200"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f66d6-201">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f66d6-201">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-202"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f66d6-202"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f66d6-203">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f66d6-203">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-204"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="f66d6-204"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f66d6-205">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f66d6-205">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f66d6-206"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f66d6-206"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f66d6-207">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f66d6-207">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f66d6-208"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f66d6-208"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f66d6-209">Implémenté en tant que <strong>JetGetIndexInfoW</strong> (Unicode) et <strong>JetGetIndexInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f66d6-209">Implemented as <strong>JetGetIndexInfoW</strong> (Unicode) and <strong>JetGetIndexInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f66d6-210">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f66d6-210">See Also</span></span>

[<span data-ttu-id="f66d6-211">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="f66d6-211">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="f66d6-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f66d6-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f66d6-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f66d6-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f66d6-214">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="f66d6-214">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="f66d6-215">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="f66d6-215">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="f66d6-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f66d6-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f66d6-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f66d6-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f66d6-218">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="f66d6-218">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
