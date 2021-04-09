---
title: Méthode IDeliveryOptimizationJob2 AddFile
description: La méthode AddFile ajoute un seul fichier à une tâche DO existante.
keywords:
- AddFile (méthode)
- Méthode AddFile, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, méthode AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103245"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a><span data-ttu-id="4b22b-106">IDeliveryOptimizationJob2 :: AddFileWithRanges, méthode</span><span class="sxs-lookup"><span data-stu-id="4b22b-106">IDeliveryOptimizationJob2::AddFileWithRanges method</span></span>

<span data-ttu-id="4b22b-107">La méthode AddFile ajoute un seul fichier à une tâche DO existante.</span><span class="sxs-lookup"><span data-stu-id="4b22b-107">The AddFile method adds a single file to an existing DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b22b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b22b-108">Syntax</span></span>

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a><span data-ttu-id="4b22b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b22b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b22b-110">*fileid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b22b-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b22b-111">La chaîne d’ID de fichier, qui identifie de façon unique le fichier à télécharger.</span><span class="sxs-lookup"><span data-stu-id="4b22b-111">The file ID string, which uniquely identifies the file to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="4b22b-112">*remoteUrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b22b-112">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b22b-113">L’URL de fichier qui tentera de se connecter pour télécharger le fichier.</span><span class="sxs-lookup"><span data-stu-id="4b22b-113">The file URL that DO will attempt to connect to download the file.</span></span>

</dd> <dt>

<span data-ttu-id="4b22b-114">*rangeCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b22b-114">*rangeCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b22b-115">Nombre d’éléments contenus dans les *plages*.</span><span class="sxs-lookup"><span data-stu-id="4b22b-115">The number of items contained in *ranges*.</span></span> <span data-ttu-id="4b22b-116">Une valeur zéro signifie qu’aucune plage n’est utilisée pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="4b22b-116">A zero value means that no ranges are used for the file.</span></span>

</dd> <dt>

<span data-ttu-id="4b22b-117">*plages* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b22b-117">*ranges* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b22b-118">Liste de plages facultatives.</span><span class="sxs-lookup"><span data-stu-id="4b22b-118">The optional range list.</span></span> <span data-ttu-id="4b22b-119">Chaque plage de la liste est une structure [**BG_FILE_RANGE**](bg-file-range.md) .</span><span class="sxs-lookup"><span data-stu-id="4b22b-119">Each range in the list is a [**BG_FILE_RANGE**](bg-file-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4b22b-120">*riid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b22b-120">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b22b-121">Type de l’objet contenu dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="4b22b-121">The type of object contained in object.</span></span> <span data-ttu-id="4b22b-122">Le type doit être IID_IDeliveryOptimizationFile.</span><span class="sxs-lookup"><span data-stu-id="4b22b-122">This must by of type IID_IDeliveryOptimizationFile.</span></span>

</dd> <dt>

<span data-ttu-id="4b22b-123">*objet* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4b22b-123">*object* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b22b-124">Objet IDeliveryOptimizationFile, qui représente le fichier de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="4b22b-124">The IDeliveryOptimizationFile object, which represents the download file.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b22b-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b22b-125">Return value</span></span>

<span data-ttu-id="4b22b-126">Cette méthode retourne S_OK en cas de réussite ou une des valeurs HRESULT standard en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4b22b-126">This method returns S_OK on success or one of the standard HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b22b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b22b-127">Requirements</span></span>

| <span data-ttu-id="4b22b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b22b-128">Requirement</span></span> | <span data-ttu-id="4b22b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b22b-129">Value</span></span> |
|---------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4b22b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b22b-130">Minimum supported client</span></span>  | <span data-ttu-id="4b22b-131">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b22b-131">Windows 10, version 1803 \[desktop apps only\]</span></span>                                  |
| <span data-ttu-id="4b22b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b22b-132">Minimum supported server</span></span>  | <span data-ttu-id="4b22b-133">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b22b-133">Windows Server, version 1709 \[desktop apps only\]</span></span>                              |
| <span data-ttu-id="4b22b-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b22b-134">Header</span></span>                    | <span data-ttu-id="4b22b-135">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="4b22b-135">Deliveryoptimization.h</span></span>                                                          |
| <span data-ttu-id="4b22b-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="4b22b-136">IDL</span></span>                       | <span data-ttu-id="4b22b-137">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="4b22b-137">DeliveryOptimization.idl</span></span>                                                        |
| <span data-ttu-id="4b22b-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4b22b-138">Library</span></span>                   | <span data-ttu-id="4b22b-139">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="4b22b-139">Dosvc.lib</span></span>                                                                       |
| <span data-ttu-id="4b22b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4b22b-140">DLL</span></span>                       | <span data-ttu-id="4b22b-141">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="4b22b-141">Dosvc.dll</span></span>                                                                       |
| <span data-ttu-id="4b22b-142">IID</span><span class="sxs-lookup"><span data-stu-id="4b22b-142">IID</span></span>                       | <span data-ttu-id="4b22b-143">IID_IDeliveryOptimizationJob est défini comme EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="4b22b-143">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span> |

## <a name="see-also"></a><span data-ttu-id="4b22b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b22b-144">See also</span></span>

[<span data-ttu-id="4b22b-145">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="4b22b-145">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
