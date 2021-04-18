---
title: Méthode IVMVirtualPC CreateDifferencingVirtualHardDisk (VPCCOMInterfaces. h)
description: Crée un disque dur virtuel de différenciation.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- Méthode CreateDifferencingVirtualHardDisk Virtual PC
- Méthode CreateDifferencingVirtualHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode CreateDifferencingVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bab178d64008b236988bfb723bd75a09a7edaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511964"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a><span data-ttu-id="d8582-106">IVMVirtualPC :: CreateDifferencingVirtualHardDisk, méthode</span><span class="sxs-lookup"><span data-stu-id="d8582-106">IVMVirtualPC::CreateDifferencingVirtualHardDisk method</span></span>

<span data-ttu-id="d8582-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d8582-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d8582-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d8582-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d8582-109">Crée un disque dur virtuel de différenciation.</span><span class="sxs-lookup"><span data-stu-id="d8582-109">Creates a differencing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8582-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8582-110">Syntax</span></span>


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="d8582-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8582-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8582-112">*ImagePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8582-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8582-113">Chemin d’accès au nouveau fichier image de disque.</span><span class="sxs-lookup"><span data-stu-id="d8582-113">The path to the new disk image file.</span></span> <span data-ttu-id="d8582-114">Le dossier conteneur sera créé s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="d8582-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="d8582-115">*ParentPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8582-115">*parentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8582-116">Chemin d’accès au fichier image de disque parent.</span><span class="sxs-lookup"><span data-stu-id="d8582-116">The path to the parent disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="d8582-117">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d8582-117">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d8582-118">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la création de l’image.</span><span class="sxs-lookup"><span data-stu-id="d8582-118">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8582-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8582-119">Return value</span></span>

<span data-ttu-id="d8582-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="d8582-120">This method can return one of these values.</span></span>



| <span data-ttu-id="d8582-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d8582-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="d8582-122">Description</span><span class="sxs-lookup"><span data-stu-id="d8582-122">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8582-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="d8582-124">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d8582-124">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="d8582-125"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="d8582-126">Un paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d8582-126">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="d8582-127">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="d8582-128">Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *ImagePath* ou *ParentPath* .</span><span class="sxs-lookup"><span data-stu-id="d8582-128">The system cannot find the path specified by the *imagePath* or *parentPath* parameter.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="d8582-129">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ lecteur non valide)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="d8582-130">Le fichier spécifié par le paramètre *ImagePath* se trouve sur un CD-ROM ou un DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d8582-130">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="d8582-131">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="d8582-132">Le paramètre *ImagePath* ou *ParentPath* contient un caractère non valide (l’un des caractères « \* ?: <>/ \| »).</span><span class="sxs-lookup"><span data-stu-id="d8582-132">The *imagePath* or *parentPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="d8582-133">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="d8582-134">Les paramètres *ImagePath* et *ParentPath* spécifient tous deux un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="d8582-134">Both the *imagePath* and *parentPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="d8582-135">Au moins l’un des paramètres doit être un chemin d’accès absolu.</span><span class="sxs-lookup"><span data-stu-id="d8582-135">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="d8582-136">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="d8582-137">Le chemin d’accès spécifié par les paramètres *ImagePath* ou *ParentPath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="d8582-137">The path specified by the *imagePath* or *parentPath* parameters is too long.</span></span> <span data-ttu-id="d8582-138">La longueur du chemin d’accès doit être inférieure à 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="d8582-138">The length of the path must be less than 260 characters.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d8582-139">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="d8582-140">Le fichier référencé par le paramètre *ImagePath* existe déjà.</span><span class="sxs-lookup"><span data-stu-id="d8582-140">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="d8582-141">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="d8582-142">L’image de disque dur virtuel de taille dynamique nécessite au moins 8 Mo d’espace libre sur le volume hôte.</span><span class="sxs-lookup"><span data-stu-id="d8582-142">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="d8582-143"><dt>**Ordinateur virtuel \_ Taille de l' \_ image E \_ \_ trop \_ grande**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-143"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="d8582-144">La *taille* du paramètre doit être inférieure à 2 088 960 Mo.</span><span class="sxs-lookup"><span data-stu-id="d8582-144">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="d8582-145">Si le format est FAT16, la taille doit être inférieure à 2000 Mo.</span><span class="sxs-lookup"><span data-stu-id="d8582-145">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="d8582-146"><dt>**Ordinateur virtuel \_ Taille de l' \_ image E \_ \_ trop \_ petite**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="d8582-147">Les images de disque dur virtuel au format non formaté et FAT16 doivent avoir au moins 3 Mo.</span><span class="sxs-lookup"><span data-stu-id="d8582-147">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="d8582-148">Les images de disque dur virtuel au format FAT32 doivent avoir au moins 514 Mo.</span><span class="sxs-lookup"><span data-stu-id="d8582-148">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="d8582-149"><dt>**Ordinateur virtuel \_ \_Fichier E \_ trop \_ volumineux \_ pour le \_ volume**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-149"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="d8582-150">Le volume hôte ne peut pas prendre en charge un fichier de cette taille si l’image de disque dur virtuel de taille dynamique augmente jusqu’à sa limite maximale.</span><span class="sxs-lookup"><span data-stu-id="d8582-150">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="d8582-151">La taille de fichier maximale pour un volume FAT32 est de 4 Go.</span><span class="sxs-lookup"><span data-stu-id="d8582-151">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="d8582-152">La taille de fichier maximale pour un volume FAT16 est de 2 Go.</span><span class="sxs-lookup"><span data-stu-id="d8582-152">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="d8582-153"><dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-153"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="d8582-154">Le disque dur virtuel ne peut pas être créé après l’arrêt de l’application.</span><span class="sxs-lookup"><span data-stu-id="d8582-154">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="d8582-155"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-155"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="d8582-156">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="d8582-156">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="d8582-157"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-157"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="d8582-158">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d8582-158">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="d8582-159">Notes</span><span class="sxs-lookup"><span data-stu-id="d8582-159">Remarks</span></span>

<span data-ttu-id="d8582-160">Bien que *ImagePath* ou *ParentPath* puisse être un chemin d’accès relatif, au moins l’un d’eux doit être un chemin d’accès absolu.</span><span class="sxs-lookup"><span data-stu-id="d8582-160">Although either *imagePath* or *parentPath* can be a relative path, at least one of these must be an absolute path.</span></span> <span data-ttu-id="d8582-161">Si un paramètre de chemin d’accès est un chemin d’accès relatif, il est supposé être relatif par rapport à l’autre paramètre de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="d8582-161">If one path parameter is a relative path, it is assumed to be relative to the other path parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8582-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8582-162">Requirements</span></span>



| <span data-ttu-id="d8582-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8582-163">Requirement</span></span> | <span data-ttu-id="d8582-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8582-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8582-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8582-165">Minimum supported client</span></span><br/> | <span data-ttu-id="d8582-166">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8582-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8582-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8582-167">Minimum supported server</span></span><br/> | <span data-ttu-id="d8582-168">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8582-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d8582-169">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d8582-169">End of client support</span></span><br/>    | <span data-ttu-id="d8582-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d8582-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d8582-171">Produit</span><span class="sxs-lookup"><span data-stu-id="d8582-171">Product</span></span><br/>                  | <span data-ttu-id="d8582-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d8582-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d8582-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8582-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8582-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8582-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d8582-175">IID</span><span class="sxs-lookup"><span data-stu-id="d8582-175">IID</span></span><br/>                      | <span data-ttu-id="d8582-176">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="d8582-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d8582-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8582-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8582-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="d8582-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

