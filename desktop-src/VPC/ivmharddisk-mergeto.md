---
title: Méthode IVMHardDisk MergeTo (VPCCOMInterfaces. h)
description: Fusionne un disque dur virtuel de différenciation avec tous ses parents.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Méthode MergeTo Virtual PC
- Méthode MergeTo Virtual PC, interface IVMHardDisk
- IVMHardDisk interface Virtual PC, méthode MergeTo
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103966"
---
# <a name="ivmharddiskmergeto-method"></a><span data-ttu-id="8c7fc-106">IVMHardDisk :: MergeTo, méthode</span><span class="sxs-lookup"><span data-stu-id="8c7fc-106">IVMHardDisk::MergeTo method</span></span>

<span data-ttu-id="8c7fc-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8c7fc-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8c7fc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8c7fc-109">Fusionne un disque dur virtuel de différenciation avec tous ses parents (jusqu’à et y compris le disque dur virtuel parent racine) vers un nouveau fichier de disque dur.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-109">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c7fc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c7fc-110">Syntax</span></span>


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="8c7fc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c7fc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c7fc-112">*newDiskImagePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c7fc-112">*newDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c7fc-113">Chemin d’accès à la nouvelle image de disque cible dans laquelle les images de disque sélectionnées seront fusionnées.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-113">The path to the new target disk image where the selected disk images will be merged.</span></span>

</dd> <dt>

<span data-ttu-id="8c7fc-114">*newDiskImageType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c7fc-114">*newDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c7fc-115">Type de nouvelle image de disque cible.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-115">The type of new target disk image.</span></span> <span data-ttu-id="8c7fc-116">Les types d’images autorisés pour la nouvelle image de disque cible sont **vmDiskType \_ Dynamic** et **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-116">The image types allowed for the new target disk image are **vmDiskType\_Dynamic** and **vmDiskType\_FixedSize**.</span></span> <span data-ttu-id="8c7fc-117">Pour plus d’informations, consultez [**VMHardDiskType**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="8c7fc-117">For more information, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c7fc-118">*mergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8c7fc-118">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8c7fc-119">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre l’achèvement du processus de fusion.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-119">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c7fc-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c7fc-120">Return value</span></span>

<span data-ttu-id="8c7fc-121">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-121">This method can return one of these values.</span></span>



| <span data-ttu-id="8c7fc-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8c7fc-122">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="8c7fc-123">Description</span><span class="sxs-lookup"><span data-stu-id="8c7fc-123">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8c7fc-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="8c7fc-125">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="8c7fc-126"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="8c7fc-127">Un paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="8c7fc-128"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="8c7fc-129">Le paramètre *newDiskImagePath* est vide.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-129">The *newDiskImagePath* parameter is empty.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="8c7fc-130">Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="8c7fc-131">Le système ne peut pas trouver le fichier spécifié par le paramètre *newDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="8c7fc-131">The system cannot find the file specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="8c7fc-132">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="8c7fc-133">Le système ne trouve pas le chemin d’accès spécifié par le paramètre *newDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="8c7fc-133">The system cannot find the path specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="8c7fc-134">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="8c7fc-135">Le paramètre *newDiskImagePath* contient un caractère non valide (l’un des éléments suivants : " \* ? <>/ \| " : ").</span><span class="sxs-lookup"><span data-stu-id="8c7fc-135">The *newDiskImagePath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="8c7fc-136">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="8c7fc-137">Le paramètre *newDiskImagePath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-137">The *newDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="8c7fc-138">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-138">An absolute path is required.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="8c7fc-139">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="8c7fc-140">Le chemin d’accès spécifié par le paramètre *newDiskImagePath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-140">The path specified by the *newDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="8c7fc-141">Le chemin d’accès doit être inférieur à 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-141">The path must be less than 260 characters.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="8c7fc-142">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="8c7fc-143">Soit le disque dur virtuel référencé par cet objet est en cours d’utilisation, soit le parent de ce disque dur virtuel est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-143">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="8c7fc-144"><dt>**Ordinateur virtuel \_ E \_ mauvais \_ \_ \_ type d’image HD**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-144"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="8c7fc-145">Cette erreur est due au fait que l’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) n’est pas une image de disque de différenciation ou que le paramètre *newDiskImageType* n’est pas l’une des valeurs acceptées, **vmDiskType \_ Dynamic** ou **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-145">This error is caused either because the virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is not a differencing disk image or because the parameter *newDiskImageType* is not one of the accepted values, **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/> |
| <dl> <span data-ttu-id="8c7fc-146">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="8c7fc-147">Le fichier référencé par le paramètre *newDiskImagePath* existe déjà.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-147">The file referenced by the *newDiskImagePath* parameter already exists.</span></span><br/>                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="8c7fc-148">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="8c7fc-149">Le volume hôte ne dispose pas de suffisamment d’espace pour fusionner ce disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-149">The host volume does not have enough space to merge this virtual hard disk.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="8c7fc-150"><dt>**Ordinateur virtuel \_ \_Chemin parent \_ E \_ \_ introuvable**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-150"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="8c7fc-151">Le parent du disque dur virtuel référencé par cet objet n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-151">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="8c7fc-152"><dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-152"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="8c7fc-153">Impossible de fusionner l’image de disque dur virtuel, car l’application est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-153">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="8c7fc-154"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-154"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="8c7fc-155">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8c7fc-155">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="8c7fc-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c7fc-156">Requirements</span></span>



| <span data-ttu-id="8c7fc-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c7fc-157">Requirement</span></span> | <span data-ttu-id="8c7fc-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c7fc-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7fc-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c7fc-159">Minimum supported client</span></span><br/> | <span data-ttu-id="8c7fc-160">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c7fc-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c7fc-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c7fc-161">Minimum supported server</span></span><br/> | <span data-ttu-id="8c7fc-162">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c7fc-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8c7fc-163">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8c7fc-163">End of client support</span></span><br/>    | <span data-ttu-id="8c7fc-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c7fc-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8c7fc-165">Produit</span><span class="sxs-lookup"><span data-stu-id="8c7fc-165">Product</span></span><br/>                  | <span data-ttu-id="8c7fc-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8c7fc-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8c7fc-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c7fc-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c7fc-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c7fc-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8c7fc-169">IID</span><span class="sxs-lookup"><span data-stu-id="8c7fc-169">IID</span></span><br/>                      | <span data-ttu-id="8c7fc-170">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="8c7fc-170">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="8c7fc-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c7fc-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c7fc-172">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="8c7fc-172">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

