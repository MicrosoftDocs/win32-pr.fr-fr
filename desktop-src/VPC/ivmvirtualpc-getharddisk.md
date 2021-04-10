---
title: Méthode IVMVirtualPC GetHardDisk (VPCCOMInterfaces. h)
description: Récupère un objet correspondant à un fichier image de disque existant.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- Méthode GetHardDisk Virtual PC
- Méthode GetHardDisk Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 558d098b6745718830c63dd700c14febf4f6bed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942610"
---
# <a name="ivmvirtualpcgetharddisk-method"></a><span data-ttu-id="2ac22-106">IVMVirtualPC :: GetHardDisk, méthode</span><span class="sxs-lookup"><span data-stu-id="2ac22-106">IVMVirtualPC::GetHardDisk method</span></span>

<span data-ttu-id="2ac22-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2ac22-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2ac22-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2ac22-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2ac22-109">Récupère un objet correspondant à un fichier image de disque existant.</span><span class="sxs-lookup"><span data-stu-id="2ac22-109">Retrieves an object corresponding to an existing disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac22-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ac22-110">Syntax</span></span>


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a><span data-ttu-id="2ac22-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ac22-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac22-112">*ImagePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ac22-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac22-113">Chemin d’accès complet à un fichier image de disque existant.</span><span class="sxs-lookup"><span data-stu-id="2ac22-113">The full path to an existing disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="2ac22-114">*dur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2ac22-114">*hardDisk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac22-115">Objet [**IVMHardDisk**](ivmharddisk.md) correspondant à cette image de disque.</span><span class="sxs-lookup"><span data-stu-id="2ac22-115">An [**IVMHardDisk**](ivmharddisk.md) object corresponding to this disk image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac22-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ac22-116">Return value</span></span>

<span data-ttu-id="2ac22-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2ac22-117">This method can return one of these values.</span></span>



| <span data-ttu-id="2ac22-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2ac22-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="2ac22-119">Description</span><span class="sxs-lookup"><span data-stu-id="2ac22-119">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ac22-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="2ac22-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2ac22-121">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="2ac22-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="2ac22-123">Le paramètre *ImagePath* ou de la **valeur du type** *de la* valeur est null.</span><span class="sxs-lookup"><span data-stu-id="2ac22-123">The *imagePath* or *hardDisk* parameter is **NULL**.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="2ac22-124">Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="2ac22-125">Le système ne peut pas trouver le fichier spécifié par le paramètre *ImagePath* .</span><span class="sxs-lookup"><span data-stu-id="2ac22-125">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="2ac22-126">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="2ac22-127">Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *ImagePath* .</span><span class="sxs-lookup"><span data-stu-id="2ac22-127">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="2ac22-128">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="2ac22-129">Le paramètre *ImagePath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).</span><span class="sxs-lookup"><span data-stu-id="2ac22-129">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="2ac22-130">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="2ac22-131">Le paramètre *ImagePath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="2ac22-131">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="2ac22-132">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="2ac22-132">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="2ac22-133">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="2ac22-134">Le chemin d’accès spécifié par le paramètre *ImagePath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="2ac22-134">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="2ac22-135">La longueur du chemin d’accès doit être inférieure à 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="2ac22-135">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="2ac22-136"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="2ac22-137">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2ac22-137">An unexpected error has occurred.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="2ac22-138"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-138"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="2ac22-139">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="2ac22-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="2ac22-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ac22-140">Requirements</span></span>



| <span data-ttu-id="2ac22-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ac22-141">Requirement</span></span> | <span data-ttu-id="2ac22-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ac22-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac22-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ac22-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2ac22-144">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ac22-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ac22-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ac22-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2ac22-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ac22-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2ac22-147">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2ac22-147">End of client support</span></span><br/>    | <span data-ttu-id="2ac22-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2ac22-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2ac22-149">Produit</span><span class="sxs-lookup"><span data-stu-id="2ac22-149">Product</span></span><br/>                  | <span data-ttu-id="2ac22-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2ac22-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2ac22-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ac22-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ac22-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac22-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2ac22-153">IID</span><span class="sxs-lookup"><span data-stu-id="2ac22-153">IID</span></span><br/>                      | <span data-ttu-id="2ac22-154">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="2ac22-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2ac22-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ac22-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac22-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="2ac22-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

