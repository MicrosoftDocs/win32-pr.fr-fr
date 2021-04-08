---
description: 'En savoir plus sur : fonction JetGetInstanceMiscInfo'
title: JetGetInstanceMiscInfo fonction)
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034904"
---
# <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="29f3a-103">JetGetInstanceMiscInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="29f3a-103">JetGetInstanceMiscInfo Function</span></span>


<span data-ttu-id="29f3a-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="29f3a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="29f3a-105">JetGetInstanceMiscInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="29f3a-105">JetGetInstanceMiscInfo Function</span></span>

<span data-ttu-id="29f3a-106">La fonction **JetGetInstanceMiscInfo** récupère des informations sur l’instance, tandis que l’instance est en ligne.</span><span class="sxs-lookup"><span data-stu-id="29f3a-106">The **JetGetInstanceMiscInfo** function retrieves information about the instance, while the instance is online.</span></span>

<span data-ttu-id="29f3a-107">**Windows Vista : JetGetInstanceMiscInfo** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="29f3a-107">**Windows Vista:  JetGetInstanceMiscInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="29f3a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29f3a-108">Parameters</span></span>

<span data-ttu-id="29f3a-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="29f3a-109">*instance*</span></span>

<span data-ttu-id="29f3a-110">Identifie l’instance de base de données qui sera utilisée pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="29f3a-110">Identifies the database instance that will be used for the API call.</span></span>

<span data-ttu-id="29f3a-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="29f3a-111">*pvResult*</span></span>

<span data-ttu-id="29f3a-112">Pointeur vers une mémoire tampon qui recevra les informations.</span><span class="sxs-lookup"><span data-stu-id="29f3a-112">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="29f3a-113">Le type de la mémoire tampon dépend de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="29f3a-113">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="29f3a-114">L’appelant est chargé d’aligner la mémoire tampon de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="29f3a-114">The caller is responsible for aligning the buffer appropriately.</span></span>

<span data-ttu-id="29f3a-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="29f3a-115">*cbMax*</span></span>

<span data-ttu-id="29f3a-116">Taille, en octets, de la mémoire tampon passée dans *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="29f3a-116">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="29f3a-117">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="29f3a-117">*InfoLevel*</span></span>

<span data-ttu-id="29f3a-118">Détermine le type d’informations qui sera récupéré pour l’instance spécifiée par l' *instance*.</span><span class="sxs-lookup"><span data-stu-id="29f3a-118">Determines what type of information will be retrieved for the instance specified by *instance*.</span></span> <span data-ttu-id="29f3a-119">Le format des données stockées dans *pvResult* dépend de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="29f3a-119">The format of the data stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="29f3a-120">Les options suivantes peuvent être utilisées avec ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="29f3a-120">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29f3a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="29f3a-121">Value</span></span></p></th>
<th><p><span data-ttu-id="29f3a-122">Signification</span><span class="sxs-lookup"><span data-stu-id="29f3a-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29f3a-123">JET_InstanceMiscInfoLogSignature</span><span class="sxs-lookup"><span data-stu-id="29f3a-123">JET_InstanceMiscInfoLogSignature</span></span></p></td>
<td><p><span data-ttu-id="29f3a-124"><em>pvResult</em> est interprété comme une structure <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> de la séquence du journal des transactions associée à cette instance.</span><span class="sxs-lookup"><span data-stu-id="29f3a-124"><em>pvResult</em> is interpreted as a <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> structure of the transaction log sequence associated with this instance.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="29f3a-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="29f3a-125">Return Value</span></span>

<span data-ttu-id="29f3a-126">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="29f3a-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="29f3a-127">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="29f3a-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29f3a-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="29f3a-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="29f3a-129">Description</span><span class="sxs-lookup"><span data-stu-id="29f3a-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29f3a-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="29f3a-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="29f3a-131">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="29f3a-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29f3a-132">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="29f3a-132">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="29f3a-133">La mémoire tampon est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="29f3a-133">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29f3a-134">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="29f3a-134">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="29f3a-135">Un <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> non valide ou un <em>InfoLevel</em> non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="29f3a-135">Either an invalid <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> or an invalid <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="29f3a-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29f3a-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29f3a-137"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="29f3a-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="29f3a-138">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="29f3a-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29f3a-139"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="29f3a-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="29f3a-140">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="29f3a-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29f3a-141"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="29f3a-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="29f3a-142">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="29f3a-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29f3a-143"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="29f3a-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="29f3a-144">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="29f3a-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29f3a-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="29f3a-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="29f3a-146">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="29f3a-146">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="29f3a-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29f3a-147">See Also</span></span>

[<span data-ttu-id="29f3a-148">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="29f3a-148">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="29f3a-149">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="29f3a-149">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="29f3a-150">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="29f3a-150">JET_SIGNATURE</span></span>](./jet-signature-structure.md)
