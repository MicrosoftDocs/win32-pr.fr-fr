---
description: 'En savoir plus sur : fonction JetGetErrorInfoW'
title: JetGetErrorInfoW fonction)
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104116319"
---
# <a name="jetgeterrorinfow-function"></a><span data-ttu-id="e8f9e-103">JetGetErrorInfoW fonction)</span><span class="sxs-lookup"><span data-stu-id="e8f9e-103">JetGetErrorInfoW Function</span></span>


<span data-ttu-id="e8f9e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="e8f9e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgeterrorinfow-function"></a><span data-ttu-id="e8f9e-105">JetGetErrorInfoW fonction)</span><span class="sxs-lookup"><span data-stu-id="e8f9e-105">JetGetErrorInfoW Function</span></span>

<span data-ttu-id="e8f9e-106">BAS_ fonction **JetGetErrorInfoW** du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-106">The **JetGetErrorInfoW** function BAS_ of the database engine.</span></span>

<span data-ttu-id="e8f9e-107">Remarque : cette documentation est basée sur une version préliminaire du moteur de stockage extensible.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="e8f9e-108">Ces informations sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-108">This information is subject to change.</span></span>

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a><span data-ttu-id="e8f9e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8f9e-109">Parameters</span></span>

<span data-ttu-id="e8f9e-110">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="e8f9e-110">*pvContext*</span></span>

<span data-ttu-id="e8f9e-111">Contexte ou valeur d’erreur pour lequel les informations d’erreur étendues sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-111">The context or error value for which the extended error information is needed.</span></span> <span data-ttu-id="e8f9e-112">La valeur passée dépend de la valeur du paramètre *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="e8f9e-112">The value passed in depends on the *InfoLevel* parameter value.</span></span>

<span data-ttu-id="e8f9e-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="e8f9e-113">*pvResult*</span></span>

<span data-ttu-id="e8f9e-114">Pointeur vers une mémoire tampon qui recevra les informations.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-114">A pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="e8f9e-115">Le type de la mémoire tampon dépend de la valeur du paramètre *InfoLevel* .</span><span class="sxs-lookup"><span data-stu-id="e8f9e-115">The type of the buffer depends on the *InfoLevel* parameter value.</span></span> <span data-ttu-id="e8f9e-116">L’appelant doit être configuré pour aligner la mémoire tampon de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-116">The caller must be configured to align the buffer appropriately.</span></span>

<span data-ttu-id="e8f9e-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="e8f9e-117">*cbMax*</span></span>

<span data-ttu-id="e8f9e-118">Taille maximale de la structure *pvResult* qui est passée.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-118">The maximum size of the *pvResult* structure that is passed in.</span></span>

<span data-ttu-id="e8f9e-119">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="e8f9e-119">*InfoLevel*</span></span>

<span data-ttu-id="e8f9e-120">Le type d’informations qui sera récupéré pour les informations d’erreur/contexte est spécifié par le paramètre *pvContext* .</span><span class="sxs-lookup"><span data-stu-id="e8f9e-120">The type of information that will be retrieved for the error info/context is specified by the *pvContext* parameter.</span></span> <span data-ttu-id="e8f9e-121">Le format des données stockées dans *pvResult* dépend de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-121">The format of the data that is stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="e8f9e-122">Le tableau suivant répertorie les valeurs possibles pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-122">The following table lists the possible values for this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8f9e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8f9e-123">Value</span></span></p></th>
<th><p><span data-ttu-id="e8f9e-124">Signification</span><span class="sxs-lookup"><span data-stu-id="e8f9e-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8f9e-125">JET_ErrorInfoSpecificErr</span><span class="sxs-lookup"><span data-stu-id="e8f9e-125">JET_ErrorInfoSpecificErr</span></span></p></td>
<td><p><span data-ttu-id="e8f9e-126"><em>pvContext</em> est interprété comme un <a href="gg269297(v=exchg.10).md">JET_ERR</a>code/Error, <em>pvResult</em> est interprété comme un <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>et les champs de la structure <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> sont remplis de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-126"><em>pvContext</em> is interpreted as a <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error code, <em>pvResult</em> is interpreted as a <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>, and the fields of the <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> structure are filled in appropriately.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8f9e-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e8f9e-127">*grbit*</span></span>

<span data-ttu-id="e8f9e-128">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-128">Reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="e8f9e-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e8f9e-129">Return Value</span></span>

<span data-ttu-id="e8f9e-130">Cette fonction retourne le type de données [JET_ERR](./extensible-storage-engine-error-codes.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-130">This function returns the [JET_ERR](./extensible-storage-engine-error-codes.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="e8f9e-131">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e8f9e-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8f9e-132">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e8f9e-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="e8f9e-133">Description</span><span class="sxs-lookup"><span data-stu-id="e8f9e-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8f9e-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e8f9e-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e8f9e-135">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8f9e-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e8f9e-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e8f9e-137">L’un des paramètres fournis contient une valeur inattendue ou contient une valeur qui n’a pas de sens lorsqu’elle est associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-137">One of the parameters provided contains an unexpected value or contains a value that does not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="e8f9e-138">Cela peut se produire pour <strong>JetGetErrorInfo</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="e8f9e-138">This can happen for <strong>JetGetErrorInfo</strong> when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="e8f9e-139">La valeur du paramètre <em>InfoLevel</em> spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-139">The specified <em>InfoLevel</em> parameter value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="e8f9e-140">La valeur <em>Grbit</em> spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-140">The specified <em>grbit</em> value is invalid.</span></span></p></li>
<li><p><span data-ttu-id="e8f9e-141">La valeur <em>cbMax</em> de la mémoire tampon du paramètre <em>pvResult</em> spécifiée est inférieure à la taille requise pour la sortie de ce paramètre <em>InfoLevel</em> .</span><span class="sxs-lookup"><span data-stu-id="e8f9e-141">The specified <em>pvResult</em> parameter buffer’s <em>cbMax</em> value is less than the required size for output of this <em>InfoLevel</em> parameter.</span></span></p></li>
<li><p><span data-ttu-id="e8f9e-142">Pour <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, la valeur <a href="gg294092(v=exchg.10).md">JET_ERR</a> passée est inconnue pour le moteur.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-142">For <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, the <a href="gg294092(v=exchg.10).md">JET_ERR</a> value passed in is unknown to the engine.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8f9e-143">JET_errDisabledFunctionality</span><span class="sxs-lookup"><span data-stu-id="e8f9e-143">JET_errDisabledFunctionality</span></span></p></td>
<td><p><span data-ttu-id="e8f9e-144">Si cette référence de Windows ne prend pas en charge cette fonction, cette erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-144">If this SKU of windows doesn’t support this function, this error will be returned.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8f9e-145">En cas de réussite, la mémoire tampon de sortie qui est appropriée pour le contexte/la valeur de l’erreur demandée sera définie sur les informations d’erreur étendues demandées.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-145">On success, the output buffer that is appropriate for the requested error context/value will be set to the extended error info requested.</span></span>

<span data-ttu-id="e8f9e-146">En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-146">On failure, the state of the output buffers will be undefined.</span></span>

### <a name="remarks"></a><span data-ttu-id="e8f9e-147">Notes</span><span class="sxs-lookup"><span data-stu-id="e8f9e-147">Remarks</span></span>

<span data-ttu-id="e8f9e-148">La fonction [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) et [JET_ERRCAT](./jet-errcat.md) groupe de constantes contiennent la documentation sur les informations d’erreur étendues retournées pour *InfoLevel* = JET_ErrorInfoSpecificErr.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-148">The [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) function and [JET_ERRCAT](./jet-errcat.md) group of constants contain documentation about the extended error information that is returned for *InfoLevel* = JET_ErrorInfoSpecificErr.</span></span>

### <a name="requirements"></a><span data-ttu-id="e8f9e-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8f9e-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8f9e-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e8f9e-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e8f9e-151">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-151">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8f9e-152"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="e8f9e-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e8f9e-153">Nécessite Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-153">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8f9e-154"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="e8f9e-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e8f9e-155">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8f9e-156"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="e8f9e-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e8f9e-157">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8f9e-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e8f9e-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e8f9e-159">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-159">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8f9e-160"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e8f9e-160"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e8f9e-161">Remarque : seul le <strong>JetGetErrorInfoW</strong> (Unicode) est implémenté.</span><span class="sxs-lookup"><span data-stu-id="e8f9e-161">Note: Only the <strong>JetGetErrorInfoW</strong> (Unicode) is implemented.</span></span> <span data-ttu-id="e8f9e-162">Cette API n’a pas de version (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e8f9e-162">This API does not have an A (ANSI) version.</span></span></p></td>
</tr>
</tbody>
</table>
