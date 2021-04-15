---
title: Méthode IVMVirtualPC CreateDynamicVirtualHardDisk (VPCCOMInterfaces. h)
description: Crée un disque dur virtuel de redimensionnement dynamique.
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- Méthode CreateDynamicVirtualHardDisk Virtual PC
- Méthode CreateDynamicVirtualHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode CreateDynamicVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDynamicVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d245072fd5b3135decd814a29dd8a87d2b6a956
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385271"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a><span data-ttu-id="9309d-106">IVMVirtualPC :: CreateDynamicVirtualHardDisk, méthode</span><span class="sxs-lookup"><span data-stu-id="9309d-106">IVMVirtualPC::CreateDynamicVirtualHardDisk method</span></span>

<span data-ttu-id="9309d-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9309d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9309d-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9309d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9309d-109">Crée un disque dur virtuel de redimensionnement dynamique.</span><span class="sxs-lookup"><span data-stu-id="9309d-109">Creates a dynamically resizing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="9309d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9309d-110">Syntax</span></span>


```C++
HRESULT CreateDynamicVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="9309d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9309d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9309d-112">*ImagePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9309d-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9309d-113">Chemin d’accès complet au nouveau fichier image de disque.</span><span class="sxs-lookup"><span data-stu-id="9309d-113">The full path to the new disk image file.</span></span> <span data-ttu-id="9309d-114">Le dossier conteneur sera créé s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="9309d-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="9309d-115">*taille* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9309d-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9309d-116">Taille de l’image, en mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="9309d-116">The size of the image, in megabytes.</span></span> <span data-ttu-id="9309d-117">Cette valeur peut être au maximum de 2 088 960 Mo (2040GB).</span><span class="sxs-lookup"><span data-stu-id="9309d-117">This value can be at most 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="9309d-118">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9309d-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9309d-119">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la création de l’image.</span><span class="sxs-lookup"><span data-stu-id="9309d-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9309d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9309d-120">Return value</span></span>

<span data-ttu-id="9309d-121">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="9309d-121">This method can return one of these values.</span></span>



| <span data-ttu-id="9309d-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9309d-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="9309d-123">Description</span><span class="sxs-lookup"><span data-stu-id="9309d-123">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9309d-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="9309d-125">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="9309d-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="9309d-126"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="9309d-127">Un paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="9309d-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="9309d-128"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="9309d-129">Le paramètre de *taille* est inférieur ou égal à 0.</span><span class="sxs-lookup"><span data-stu-id="9309d-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="9309d-130">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="9309d-131">Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *ImagePath* .</span><span class="sxs-lookup"><span data-stu-id="9309d-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="9309d-132">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ lecteur non valide)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="9309d-133">Le fichier spécifié par le paramètre *ImagePath* se trouve sur un CD-ROM ou un DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="9309d-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="9309d-134">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="9309d-135">Le paramètre *ImagePath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).</span><span class="sxs-lookup"><span data-stu-id="9309d-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="9309d-136">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="9309d-137">Le paramètre *ImagePath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="9309d-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="9309d-138">Au moins l’un des paramètres doit être un chemin d’accès absolu.</span><span class="sxs-lookup"><span data-stu-id="9309d-138">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="9309d-139">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="9309d-140">Le chemin d’accès spécifié par le paramètre *ImagePath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="9309d-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="9309d-141">La longueur du chemin d’accès doit être inférieure à 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="9309d-141">The length of the path must be less than 260 characters.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="9309d-142">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="9309d-143">Le fichier référencé par le paramètre *ImagePath* existe déjà.</span><span class="sxs-lookup"><span data-stu-id="9309d-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="9309d-144">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="9309d-145">L’image de disque dur virtuel de taille dynamique nécessite au moins 8 Mo d’espace libre sur le volume hôte.</span><span class="sxs-lookup"><span data-stu-id="9309d-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="9309d-146"><dt>**Ordinateur virtuel \_ Taille de l' \_ image E \_ \_ trop \_ grande**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="9309d-147">La *taille* du paramètre doit être inférieure à 2 088 960 Mo.</span><span class="sxs-lookup"><span data-stu-id="9309d-147">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="9309d-148">Si le format est FAT16, la taille doit être inférieure à 2000 Mo.</span><span class="sxs-lookup"><span data-stu-id="9309d-148">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="9309d-149"><dt>**Ordinateur virtuel \_ Taille de l' \_ image E \_ \_ trop \_ petite**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="9309d-150">Les images de disque dur virtuel au format non formaté et FAT16 doivent avoir au moins 3 Mo.</span><span class="sxs-lookup"><span data-stu-id="9309d-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="9309d-151">Les images de disque dur virtuel au format FAT32 doivent avoir au moins 514 Mo.</span><span class="sxs-lookup"><span data-stu-id="9309d-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="9309d-152"><dt>**Ordinateur virtuel \_ \_Fichier E \_ trop \_ volumineux \_ pour le \_ volume**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="9309d-153">Le volume hôte ne peut pas prendre en charge un fichier de cette taille si l’image de disque dur virtuel de taille dynamique augmente jusqu’à sa limite maximale.</span><span class="sxs-lookup"><span data-stu-id="9309d-153">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="9309d-154">La taille de fichier maximale pour un volume FAT32 est de 4 Go.</span><span class="sxs-lookup"><span data-stu-id="9309d-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="9309d-155">La taille de fichier maximale pour un volume FAT16 est de 2 Go.</span><span class="sxs-lookup"><span data-stu-id="9309d-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="9309d-156"><dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="9309d-157">Le disque dur virtuel ne peut pas être créé après l’arrêt de l’application.</span><span class="sxs-lookup"><span data-stu-id="9309d-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="9309d-158"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="9309d-159">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="9309d-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="9309d-160"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="9309d-161">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9309d-161">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="9309d-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9309d-162">Requirements</span></span>



| <span data-ttu-id="9309d-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9309d-163">Requirement</span></span> | <span data-ttu-id="9309d-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="9309d-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9309d-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9309d-165">Minimum supported client</span></span><br/> | <span data-ttu-id="9309d-166">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9309d-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9309d-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9309d-167">Minimum supported server</span></span><br/> | <span data-ttu-id="9309d-168">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9309d-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9309d-169">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9309d-169">End of client support</span></span><br/>    | <span data-ttu-id="9309d-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9309d-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9309d-171">Produit</span><span class="sxs-lookup"><span data-stu-id="9309d-171">Product</span></span><br/>                  | <span data-ttu-id="9309d-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9309d-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9309d-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="9309d-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="9309d-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9309d-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9309d-175">IID</span><span class="sxs-lookup"><span data-stu-id="9309d-175">IID</span></span><br/>                      | <span data-ttu-id="9309d-176">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="9309d-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9309d-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9309d-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9309d-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="9309d-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

