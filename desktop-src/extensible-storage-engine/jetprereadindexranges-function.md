---
description: 'En savoir plus sur : fonction JetPrereadIndexRanges'
title: JetPrereadIndexRanges fonction)
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112047"
---
# <a name="jetprereadindexranges-function"></a><span data-ttu-id="f8fac-103">JetPrereadIndexRanges fonction)</span><span class="sxs-lookup"><span data-stu-id="f8fac-103">JetPrereadIndexRanges Function</span></span>


<span data-ttu-id="f8fac-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f8fac-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="f8fac-105">La fonction **JetPrereadIndexRanges** prélit les index pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="f8fac-105">The **JetPrereadIndexRanges** function prereads indexes to improve the performance.</span></span>

<span data-ttu-id="f8fac-106">La fonction **JetPrereadIndexRanges** a été introduite dans le système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f8fac-106">The **JetPrereadIndexRanges** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="f8fac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8fac-107">Parameters</span></span>

<span data-ttu-id="f8fac-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f8fac-108">*sesid*</span></span>

<span data-ttu-id="f8fac-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="f8fac-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="f8fac-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="f8fac-110">*tableid*</span></span>

<span data-ttu-id="f8fac-111">Table avec laquelle émettre les prélectures.</span><span class="sxs-lookup"><span data-stu-id="f8fac-111">The table to issue the prereads against.</span></span>

<span data-ttu-id="f8fac-112">*rgIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="f8fac-112">*rgIndexRanges*</span></span>

<span data-ttu-id="f8fac-113">Plages de clés à prélire.</span><span class="sxs-lookup"><span data-stu-id="f8fac-113">The key ranges to preread.</span></span>

<span data-ttu-id="f8fac-114">*cIndexRanges*</span><span class="sxs-lookup"><span data-stu-id="f8fac-114">*cIndexRanges*</span></span>

<span data-ttu-id="f8fac-115">Nombre de plages de clés à prélire, déterminé par le nombre d’éléments dans *rgIndexRanges*.</span><span class="sxs-lookup"><span data-stu-id="f8fac-115">The number of key ranges to preread, determined by the number of elements in *rgIndexRanges*.</span></span>

<span data-ttu-id="f8fac-116">*pcRangesPreread*</span><span class="sxs-lookup"><span data-stu-id="f8fac-116">*pcRangesPreread*</span></span>

<span data-ttu-id="f8fac-117">Nombre de plages de clés réellement prélues.</span><span class="sxs-lookup"><span data-stu-id="f8fac-117">The number of key ranges that were actually preread.</span></span>

<span data-ttu-id="f8fac-118">*rgcolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="f8fac-118">*rgcolumnidPreread*</span></span>

<span data-ttu-id="f8fac-119">Liste des ID de colonne pour les colonnes de valeur longue à prélire.</span><span class="sxs-lookup"><span data-stu-id="f8fac-119">List of column IDs for long value columns to preread.</span></span> <span data-ttu-id="f8fac-120">Par défaut, seul l’enregistrement sur la page est prélecture.</span><span class="sxs-lookup"><span data-stu-id="f8fac-120">By default, only the on-page record is preread.</span></span> <span data-ttu-id="f8fac-121">Si les colonnes de valeur longue page non paginée doivent être prélues, leurs ID de colonne doivent être transmis via ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f8fac-121">If Off-page long value columns need to be preread, their column IDs need to be passed via this parameter.</span></span>

<span data-ttu-id="f8fac-122">*ccolumnidPreread*</span><span class="sxs-lookup"><span data-stu-id="f8fac-122">*ccolumnidPreread*</span></span>

<span data-ttu-id="f8fac-123">Nombre d’ID de colonne pour les colonnes de valeurs longues à prélire, déterminé par le nombre d’éléments dans *rgcolumnidPreread*.</span><span class="sxs-lookup"><span data-stu-id="f8fac-123">The number of column IDs for long value columns to preread, determined by the number of elements in *rgcolumnidPreread*.</span></span>

<span data-ttu-id="f8fac-124">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f8fac-124">*grbit*</span></span>

<span data-ttu-id="f8fac-125">Groupe de bits qui spécifie zéro, une ou plusieurs des valeurs de direction de prélecture énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f8fac-125">A group of bits that specifies zero or more of the preread direction values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8fac-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8fac-126">Value</span></span></p></th>
<th><p><span data-ttu-id="f8fac-127">Signification</span><span class="sxs-lookup"><span data-stu-id="f8fac-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8fac-128">Transférer</span><span class="sxs-lookup"><span data-stu-id="f8fac-128">Forward</span></span></p></td>
<td><p><span data-ttu-id="f8fac-129">Lecture anticipée.</span><span class="sxs-lookup"><span data-stu-id="f8fac-129">Preread forward.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8fac-130">Vers l'arrière</span><span class="sxs-lookup"><span data-stu-id="f8fac-130">Backwards</span></span></p></td>
<td><p><span data-ttu-id="f8fac-131">Prélire en arrière.</span><span class="sxs-lookup"><span data-stu-id="f8fac-131">Preread backward.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8fac-132">FirstPageOnly</span><span class="sxs-lookup"><span data-stu-id="f8fac-132">FirstPageOnly</span></span></p></td>
<td><p><span data-ttu-id="f8fac-133">Prélire uniquement la première page d’une colonne longue.</span><span class="sxs-lookup"><span data-stu-id="f8fac-133">Preread only the first page of any long column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8fac-134">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="f8fac-134">NormalizedKey</span></span></p></td>
<td><p><span data-ttu-id="f8fac-135">Clé/signet normalisé fourni à la place de la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="f8fac-135">Normalized key/bookmark provided instead of column value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f8fac-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8fac-136">Return value</span></span>

<span data-ttu-id="f8fac-137">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f8fac-137">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="f8fac-138">Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f8fac-138">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8fac-139">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f8fac-139">Return code</span></span></p></th>
<th><p><span data-ttu-id="f8fac-140">Description</span><span class="sxs-lookup"><span data-stu-id="f8fac-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8fac-141">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f8fac-141">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f8fac-142">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f8fac-142">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="f8fac-143">Notes</span><span class="sxs-lookup"><span data-stu-id="f8fac-143">Remarks</span></span>

<span data-ttu-id="f8fac-144">Si les enregistrements avec les plages de clés spécifiées ne se trouvent pas dans le cache des tampons, vous devez démarrer des lectures asynchrones pour placer les enregistrements dans le cache des tampons de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f8fac-144">If the records with the specified key ranges are not in the buffer cache, you should start asynchronous reads to bring the records into the database buffer cache.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f8fac-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8fac-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8fac-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f8fac-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f8fac-147">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f8fac-147">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8fac-148"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f8fac-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f8fac-149">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="f8fac-149">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8fac-150"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f8fac-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f8fac-151">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f8fac-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8fac-152"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="f8fac-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f8fac-153">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f8fac-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8fac-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f8fac-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f8fac-155">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f8fac-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f8fac-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8fac-156">See also</span></span>

[<span data-ttu-id="f8fac-157">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f8fac-157">JET_ERR</span></span>](./jet-err.md)
