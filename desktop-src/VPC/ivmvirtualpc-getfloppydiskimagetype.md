---
title: Méthode IVMVirtualPC GetFloppyDiskImageType (VPCCOMInterfaces. h)
description: Récupère le type d’un fichier image de disquette existant.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- Méthode GetFloppyDiskImageType Virtual PC
- Méthode GetFloppyDiskImageType Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetFloppyDiskImageType
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106042"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a><span data-ttu-id="f6096-106">IVMVirtualPC :: GetFloppyDiskImageType, méthode</span><span class="sxs-lookup"><span data-stu-id="f6096-106">IVMVirtualPC::GetFloppyDiskImageType method</span></span>

<span data-ttu-id="f6096-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f6096-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f6096-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f6096-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f6096-109">Récupère le type d’un fichier image de disquette existant.</span><span class="sxs-lookup"><span data-stu-id="f6096-109">Retrieves the type of an existing floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6096-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6096-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a><span data-ttu-id="f6096-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6096-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6096-112">*ImagePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6096-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6096-113">Chemin d’accès complet au fichier image de disque.</span><span class="sxs-lookup"><span data-stu-id="f6096-113">The full path to the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="f6096-114">*ImageType* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f6096-114">*imageType* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f6096-115">Type d’image de disque.</span><span class="sxs-lookup"><span data-stu-id="f6096-115">The disk image type.</span></span> <span data-ttu-id="f6096-116">Pour obtenir la liste des valeurs, consultez [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="f6096-116">For a list of values, see [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6096-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6096-117">Return value</span></span>

<span data-ttu-id="f6096-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f6096-118">This method can return one of these values.</span></span>



| <span data-ttu-id="f6096-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f6096-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="f6096-120">Description</span><span class="sxs-lookup"><span data-stu-id="f6096-120">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6096-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="f6096-122">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f6096-122">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="f6096-123"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="f6096-124">Le paramètre *ImagePath* ou *ImageType* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f6096-124">The *imagePath* or *imageType* parameter is **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="f6096-125">Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="f6096-126">Le système ne peut pas trouver le fichier spécifié par le paramètre *ImagePath* .</span><span class="sxs-lookup"><span data-stu-id="f6096-126">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="f6096-127">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="f6096-128">Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *ImagePath* .</span><span class="sxs-lookup"><span data-stu-id="f6096-128">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="f6096-129">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="f6096-130">Le paramètre *ImagePath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).</span><span class="sxs-lookup"><span data-stu-id="f6096-130">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="f6096-131">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="f6096-132">Le paramètre *ImagePath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="f6096-132">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="f6096-133">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="f6096-133">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="f6096-134">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="f6096-135">Le chemin d’accès spécifié par le paramètre *ImagePath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="f6096-135">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="f6096-136">La longueur du chemin d’accès doit être inférieure à 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="f6096-136">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="f6096-137"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="f6096-138">Le fichier spécifié par *ImagePath* n’est pas une image de disquette, ou une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f6096-138">The file specified by *imagePath* is not a floppy image, or an unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="f6096-139"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-139"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="f6096-140">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="f6096-140">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="f6096-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6096-141">Requirements</span></span>



| <span data-ttu-id="f6096-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6096-142">Requirement</span></span> | <span data-ttu-id="f6096-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6096-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6096-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6096-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f6096-145">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6096-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6096-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6096-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f6096-147">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6096-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f6096-148">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f6096-148">End of client support</span></span><br/>    | <span data-ttu-id="f6096-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6096-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f6096-150">Produit</span><span class="sxs-lookup"><span data-stu-id="f6096-150">Product</span></span><br/>                  | <span data-ttu-id="f6096-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f6096-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f6096-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6096-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6096-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6096-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f6096-154">IID</span><span class="sxs-lookup"><span data-stu-id="f6096-154">IID</span></span><br/>                      | <span data-ttu-id="f6096-155">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f6096-155">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f6096-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6096-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6096-157">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="f6096-157">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

