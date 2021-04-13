---
title: Méthode IVMVirtualPC CreateFloppyDiskImage (VPCCOMInterfaces. h)
description: Crée un fichier image de disquette.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- Méthode CreateFloppyDiskImage Virtual PC
- Méthode CreateFloppyDiskImage Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode CreateFloppyDiskImage
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466263"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a><span data-ttu-id="4506e-106">IVMVirtualPC :: CreateFloppyDiskImage, méthode</span><span class="sxs-lookup"><span data-stu-id="4506e-106">IVMVirtualPC::CreateFloppyDiskImage method</span></span>

<span data-ttu-id="4506e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4506e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4506e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4506e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4506e-109">Crée un fichier image de disquette.</span><span class="sxs-lookup"><span data-stu-id="4506e-109">Creates a floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4506e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4506e-110">Syntax</span></span>


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a><span data-ttu-id="4506e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4506e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4506e-112">*ImagePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4506e-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4506e-113">Chemin d’accès complet au nouveau fichier image de disque.</span><span class="sxs-lookup"><span data-stu-id="4506e-113">The full path to the new disk image file.</span></span> <span data-ttu-id="4506e-114">Le dossier conteneur sera créé s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="4506e-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="4506e-115">*ImageType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4506e-115">*imageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4506e-116">Type d’image de disquette à créer.</span><span class="sxs-lookup"><span data-stu-id="4506e-116">The type of floppy disk image to create.</span></span> <span data-ttu-id="4506e-117">Seuls les **vmFloppyDiskImage \_ LowDensity** (1) et **vmFloppyDiskImage \_ HighDensity** (2) sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4506e-117">Only **vmFloppyDiskImage\_LowDensity** (1) and **vmFloppyDiskImage\_HighDensity** (2) are supported.</span></span> <span data-ttu-id="4506e-118">Consultez [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="4506e-118">See [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4506e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4506e-119">Return value</span></span>

<span data-ttu-id="4506e-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="4506e-120">This method can return one of these values.</span></span>



| <span data-ttu-id="4506e-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4506e-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="4506e-122">Description</span><span class="sxs-lookup"><span data-stu-id="4506e-122">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4506e-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-123"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="4506e-124">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4506e-124">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="4506e-125"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="4506e-126">Le paramètre *ImagePath* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4506e-126">The *imagePath* parameter is **NULL**.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="4506e-127"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="4506e-128">Le paramètre *ImageType* n’est pas [**vmFloppyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) ou **vmFloppyDiskImage \_ HighDensity** (2).</span><span class="sxs-lookup"><span data-stu-id="4506e-128">The *imageType* parameter is not [**vmFloppyDiskImage\_LowDensity**](vmfloppydiskimagetype.md) (1) or **vmFloppyDiskImage\_HighDensity** (2).</span></span><br/> |
| <dl> <span data-ttu-id="4506e-129">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="4506e-130">Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *ImagePath* .</span><span class="sxs-lookup"><span data-stu-id="4506e-130">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="4506e-131">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="4506e-132">Le paramètre *ImagePath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).</span><span class="sxs-lookup"><span data-stu-id="4506e-132">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                           |
| <dl> <span data-ttu-id="4506e-133">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="4506e-134">Le paramètre *ImagePath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="4506e-134">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="4506e-135">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="4506e-135">An absolute path is required.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="4506e-136">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="4506e-137">Le chemin d’accès spécifié par le paramètre *ImagePath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="4506e-137">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="4506e-138">La longueur du chemin d’accès doit être inférieure à 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="4506e-138">The length of the path must be less than 260 characters.</span></span><br/>                          |
| <dl> <span data-ttu-id="4506e-139">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="4506e-140">Le fichier référencé par le paramètre *ImagePath* existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4506e-140">The file referenced by the parameter *imagePath* already exists.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="4506e-141">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="4506e-142">Il n’y a pas suffisamment d’espace sur le volume hôte pour créer l’image de disquette virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4506e-142">There is insufficient space on the host volume to create the virtual floppy disk image.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4506e-143"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-143"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="4506e-144">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4506e-144">An unexpected error occurred.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="4506e-145"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-145"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="4506e-146">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="4506e-146">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                           |



 

## <a name="requirements"></a><span data-ttu-id="4506e-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4506e-147">Requirements</span></span>



| <span data-ttu-id="4506e-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4506e-148">Requirement</span></span> | <span data-ttu-id="4506e-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="4506e-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4506e-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4506e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="4506e-151">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4506e-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4506e-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4506e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="4506e-153">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4506e-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4506e-154">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4506e-154">End of client support</span></span><br/>    | <span data-ttu-id="4506e-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4506e-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4506e-156">Produit</span><span class="sxs-lookup"><span data-stu-id="4506e-156">Product</span></span><br/>                  | <span data-ttu-id="4506e-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4506e-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4506e-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="4506e-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="4506e-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4506e-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4506e-160">IID</span><span class="sxs-lookup"><span data-stu-id="4506e-160">IID</span></span><br/>                      | <span data-ttu-id="4506e-161">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="4506e-161">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4506e-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4506e-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4506e-163">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="4506e-163">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

