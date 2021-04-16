---
title: Méthode IBackgroundCopyFile2 SetRemoteName (Deliveryoptimization. h)
description: Remplace le nom distant par une nouvelle URL dans un travail de téléchargement.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Méthode SetRemoteName
- Méthode SetRemoteName, interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, méthode SetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465074"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a><span data-ttu-id="6d524-106">IBackgroundCopyFile2 :: SetRemoteName, méthode</span><span class="sxs-lookup"><span data-stu-id="6d524-106">IBackgroundCopyFile2::SetRemoteName method</span></span>

<span data-ttu-id="6d524-107">Remplace le nom distant par une nouvelle URL dans un travail de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="6d524-107">Changes the remote name to a new URL in a download job.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d524-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d524-108">Syntax</span></span>


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a><span data-ttu-id="6d524-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d524-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d524-110">*Nom_distant* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d524-110">*RemoteName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d524-111">Chaîne terminée par le caractère null qui contient le nom du fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="6d524-111">Null-terminated string that contains the name of the file on the server.</span></span> <span data-ttu-id="6d524-112">Pour plus d’informations sur la spécification du nom distant, consultez le membre **nom_distant** .</span><span class="sxs-lookup"><span data-stu-id="6d524-112">For information on specifying the remote name, see the **RemoteName** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d524-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d524-113">Return value</span></span>

<span data-ttu-id="6d524-114">Cette méthode retourne les valeurs de retour suivantes, ainsi que d’autres.</span><span class="sxs-lookup"><span data-stu-id="6d524-114">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="6d524-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6d524-115">Return code</span></span>                                                                                  | <span data-ttu-id="6d524-116">Description</span><span class="sxs-lookup"><span data-stu-id="6d524-116">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d524-117"><dt>S_OK \* \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6d524-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="6d524-118">Succès</span><span class="sxs-lookup"><span data-stu-id="6d524-118">Success</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="6d524-119"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6d524-119"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6d524-120">Le nouveau nom distant est une URL non valide ou la nouvelle URL est trop longue (l’URL ne peut pas dépasser 2 200 caractères).</span><span class="sxs-lookup"><span data-stu-id="6d524-120">The new remote name is an invalid URL or the new URL is too long (the URL cannot exceed 2,200 characters).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d524-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6d524-121">Remarks</span></span>

<span data-ttu-id="6d524-122">En général, vous appelez cette méthode si vous souhaitez modifier l’URL utilisée pour transférer le fichier ou si vous souhaitez modifier le nom ou le chemin d’accès du fichier.</span><span class="sxs-lookup"><span data-stu-id="6d524-122">Typically, you call this method if you want to change the URL used to transfer the file or if you want to change the file name or path.</span></span>

<span data-ttu-id="6d524-123">Cette méthode ne sérialise pas quand elle retourne.</span><span class="sxs-lookup"><span data-stu-id="6d524-123">This method does not serialize when it returns.</span></span> <span data-ttu-id="6d524-124">Pour sérialiser la modification, [**interrompez**](ibackgroundcopyjob-suspend.md) la tâche, appelez cette méthode (si vous modifiez plusieurs fichiers du travail, utilisez une boucle) et [**reprenez**](ibackgroundcopyjob-resume.md) la tâche.</span><span class="sxs-lookup"><span data-stu-id="6d524-124">To serialize the change, [**suspend**](ibackgroundcopyjob-suspend.md) the job, call this method (if changing multiple files in the job, use a loop), and [**resume**](ibackgroundcopyjob-resume.md) the job.</span></span> <span data-ttu-id="6d524-125">L’appel de la méthode **méthode ibackgroundcopyjob :: Resume** sérialise la modification.</span><span class="sxs-lookup"><span data-stu-id="6d524-125">Calling the **IBackgroundCopyJob::Resume** method serializes the change.</span></span>

<span data-ttu-id="6d524-126">Si l’horodatage ou la taille de fichier du nouveau nom distant est différent du nom distant précédent ou si le nouveau serveur ne prend pas en charge la reprise de point de contrôle (pour les noms distants HTTP), redémarre le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="6d524-126">If the time stamp or file size of the new remote name is different from the previous remote name or the new server does not support checkpoint resume (for HTTP remote names), DO restarts the download.</span></span> <span data-ttu-id="6d524-127">Dans le cas contraire, le transfert reprend à partir de la même position sur le nouveau serveur.</span><span class="sxs-lookup"><span data-stu-id="6d524-127">Otherwise, the transfer resumes from the same position on the new server.</span></span> <span data-ttu-id="6d524-128">Ne redémarrez pas les fichiers déjà transférés.</span><span class="sxs-lookup"><span data-stu-id="6d524-128">DO does not restart already transferred files.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d524-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d524-129">Requirements</span></span>



| <span data-ttu-id="6d524-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d524-130">Requirement</span></span> | <span data-ttu-id="6d524-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d524-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d524-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d524-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6d524-133">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d524-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6d524-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d524-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6d524-135">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d524-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6d524-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d524-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d524-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d524-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d524-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="6d524-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d524-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d524-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="6d524-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6d524-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d524-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d524-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="6d524-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6d524-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d524-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d524-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="6d524-144">IID</span><span class="sxs-lookup"><span data-stu-id="6d524-144">IID</span></span><br/>                      | <span data-ttu-id="6d524-145">IID_IBackgroundCopyFile2 est défini en tant que 83e81b93-0873-474d-8A8C-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="6d524-145">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6d524-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d524-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d524-147">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="6d524-147">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





