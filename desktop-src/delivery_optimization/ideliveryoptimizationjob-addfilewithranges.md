---
title: Méthode IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization. h)
description: Ajoute un fichier à un travail de téléchargement et spécifie les plages du fichier que vous souhaitez télécharger.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Méthode AddFileWithRanges
- Méthode AddFileWithRanges, interface IDeliveryOptimizationJob
- Interface IDeliveryOptimizationJob, méthode AddFileWithRanges
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510367"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a><span data-ttu-id="2c4e1-106">IDeliveryOptimizationJob :: AddFileWithRanges, méthode</span><span class="sxs-lookup"><span data-stu-id="2c4e1-106">IDeliveryOptimizationJob::AddFileWithRanges method</span></span>

<span data-ttu-id="2c4e1-107">Ajoute un fichier à un travail de téléchargement et spécifie les plages du fichier que vous souhaitez télécharger.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-107">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c4e1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c4e1-108">Syntax</span></span>


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a><span data-ttu-id="2c4e1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c4e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4e1-110">*fileid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c4e1-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4e1-111">Chaîne terminée par le caractère null qui est un identificateur unique du contenu publié.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-111">Null terminated string that s an unique identifier of the published content.</span></span> <span data-ttu-id="2c4e1-112">Pour du contenu non publié, il peut s’agir d’une chaîne unique que l’appelant peut utiliser pour identifier des fichiers dans un travail.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-112">For non-published content, this can be any unique string that caller can use to identify files within a job.</span></span>

</dd> <dt>

<span data-ttu-id="2c4e1-113">*remoteUrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c4e1-113">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4e1-114">Chaîne terminée par le caractère null qui contient le nom du fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-114">Null-terminated string that contains the name of the file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="2c4e1-115">*LocalName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c4e1-115">*localName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4e1-116">Chaîne terminée par le caractère null qui contient le nom du fichier sur le client.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-116">Null-terminated string that contains the name of the file on the client.</span></span>

</dd> <dt>

<span data-ttu-id="2c4e1-117">*rangeCount* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2c4e1-117">*rangeCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4e1-118">Nombre d’éléments dans les *plages*.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-118">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="2c4e1-119">*plages* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2c4e1-119">*ranges* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4e1-120">Tableau d’une ou de plusieurs structures de [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) qui spécifient les plages à télécharger.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-120">Array of one or more [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) structures that specify the ranges to download.</span></span> <span data-ttu-id="2c4e1-121">Ne spécifiez pas de doublons ou de plages qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-121">Do not specify duplicate or overlapping ranges.</span></span>

</dd> <dt>

<span data-ttu-id="2c4e1-122">*taille* \[ du dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2c4e1-122">*fileSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2c4e1-123">Taille du fichier en octets.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-123">Size of the file in bytes.</span></span> <span data-ttu-id="2c4e1-124">Transmettez **DO_UNKNOWN_FILE_SIZE** si la taille n’est pas connue de l’application de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-124">Pass in **DO_UNKNOWN_FILE_SIZE** if size is not known to the caller application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c4e1-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c4e1-125">Return value</span></span>

<span data-ttu-id="2c4e1-126">Cette méthode retourne les valeurs de retour suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-126">This method returns the following return values, as well as others.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c4e1-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2c4e1-127">Return code</span></span></th>
<th><span data-ttu-id="2c4e1-128">Description</span><span class="sxs-lookup"><span data-stu-id="2c4e1-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="2c4e1-129"><dt><strong><strong>S_OK</strong></strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2c4e1-129"><dt><strong><strong>S_OK</strong></strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2c4e1-130">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-130">Success.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="2c4e1-131"><dt><strong>E_INVALIDARG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2c4e1-131"><dt><strong>E_INVALIDARG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2c4e1-132">Le nom de fichier local est NULL ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-132">The local file name is NULL or empty string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="2c4e1-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2c4e1-133"><dt><strong>E_ACCESSDENIED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2c4e1-134">L’utilisateur n’a pas l’autorisation d’écrire dans le répertoire spécifié sur le client.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-134">User does not have permission to write to the specified directory on the client.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="2c4e1-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2c4e1-135"><dt><strong>DO_E_INVALID_RANGE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2c4e1-136">L’une des plages n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-136">One of the ranges is invalid.</span></span> <span data-ttu-id="2c4e1-137">Par exemple, InitialOffset est défini sur <strong>BG_LENGTH_TO_EOF</strong>.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-137">For example, InitialOffset is set to <strong>BG_LENGTH_TO_EOF</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="2c4e1-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2c4e1-138"><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2c4e1-139">Vous ne pouvez pas spécifier des plages en double ou qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-139">You cannot specify duplicate or overlapping ranges.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2c4e1-140">Les plages sont triées selon le décalage de la valeur, et non la longueur.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-140">The ranges are sorted by the offset of the value, not the length.</span></span> <span data-ttu-id="2c4e1-141">Si des plages ont le même décalage, mais sont dans l’ordre inverse, cette erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-141">If ranges are entered that have the same offset, but are in reverse order, then this error will be returned.</span></span> <span data-ttu-id="2c4e1-142">Par exemple, si 100,5 et 100,0 sont entrés dans cet ordre, vous ne serez pas en mesure d’ajouter le fichier au travail.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-142">For example, if 100.5 and 100.0 are entered in that order, then you will not be able to add the file to the job.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="2c4e1-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2c4e1-143"><dt><strong>DO_E_INVALID_STATE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="2c4e1-144">L’état du travail ne peut pas être <strong>BG_JOB_STATE_CANCELLED</strong> ou <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span><span class="sxs-lookup"><span data-stu-id="2c4e1-144">The state of the job cannot be <strong>BG_JOB_STATE_CANCELLED</strong> or <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="2c4e1-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c4e1-145">Requirements</span></span>



| <span data-ttu-id="2c4e1-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c4e1-146">Requirement</span></span> | <span data-ttu-id="2c4e1-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c4e1-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4e1-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c4e1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2c4e1-149">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c4e1-149">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2c4e1-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c4e1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2c4e1-151">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c4e1-151">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2c4e1-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c4e1-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c4e1-153"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c4e1-153"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c4e1-154">MIDL</span><span class="sxs-lookup"><span data-stu-id="2c4e1-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c4e1-155"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c4e1-155"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2c4e1-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c4e1-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c4e1-157"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c4e1-157"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2c4e1-158">DLL</span><span class="sxs-lookup"><span data-stu-id="2c4e1-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c4e1-159"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c4e1-159"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2c4e1-160">IID</span><span class="sxs-lookup"><span data-stu-id="2c4e1-160">IID</span></span><br/>                      | <span data-ttu-id="2c4e1-161">IID_IDeliveryOptimizationJob est défini comme EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="2c4e1-161">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="2c4e1-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c4e1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c4e1-163">**IDeliveryOptimizationJob**</span><span class="sxs-lookup"><span data-stu-id="2c4e1-163">**IDeliveryOptimizationJob**</span></span>](ideliveryoptimizationjob.md)
</dt> </dl>

 

