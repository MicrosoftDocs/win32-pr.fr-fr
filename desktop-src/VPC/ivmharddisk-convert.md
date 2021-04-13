---
title: Méthode Convert IVMHardDisk (VPCCOMInterfaces. h)
description: Convertit un disque dur virtuel de taille fixe en disque dur virtuel de taille dynamique ou convertit un disque dur virtuel de taille dynamique en disque dur virtuel de taille fixe.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Convertir la méthode Virtual PC
- Méthode de conversion Virtual PC, interface IVMHardDisk
- IVMHardDisk interface Virtual PC, méthode Convert
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466699"
---
# <a name="ivmharddiskconvert-method"></a><span data-ttu-id="425c6-106">IVMHardDisk :: Convert, méthode</span><span class="sxs-lookup"><span data-stu-id="425c6-106">IVMHardDisk::Convert method</span></span>

<span data-ttu-id="425c6-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="425c6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="425c6-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="425c6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="425c6-109">Convertit un disque dur virtuel de taille fixe en disque dur virtuel de taille dynamique ou convertit un disque dur virtuel de taille dynamique en disque dur virtuel de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="425c6-109">Converts a fixed-size virtual hard disk to a dynamically expanding virtual hard disk or converts a dynamically expanding virtual hard disk to a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="425c6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="425c6-110">Syntax</span></span>


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a><span data-ttu-id="425c6-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="425c6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="425c6-112">*convertedDiskImagePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="425c6-112">*convertedDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="425c6-113">Chemin d’accès au fichier image de disque cible.</span><span class="sxs-lookup"><span data-stu-id="425c6-113">The path to the target disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="425c6-114">*convertedDiskImageType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="425c6-114">*convertedDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="425c6-115">Type de l’image de disque cible.</span><span class="sxs-lookup"><span data-stu-id="425c6-115">The type of the target disk image.</span></span> <span data-ttu-id="425c6-116">Pour obtenir la liste des valeurs, consultez [**VMHardDiskType**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="425c6-116">For a list of values, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="425c6-117">*convertTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="425c6-117">*convertTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="425c6-118">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre l’achèvement du processus de conversion.</span><span class="sxs-lookup"><span data-stu-id="425c6-118">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the conversion process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="425c6-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="425c6-119">Return value</span></span>

<span data-ttu-id="425c6-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="425c6-120">This method can return one of these values.</span></span>



| <span data-ttu-id="425c6-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="425c6-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="425c6-122">Description</span><span class="sxs-lookup"><span data-stu-id="425c6-122">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="425c6-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="425c6-124">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="425c6-124">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="425c6-125"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="425c6-126">Le paramètre *convertedDiskImagePath* est vide ou n’a pas d’extension. vhd sur le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="425c6-126">The *convertedDiskImagePath* parameter is empty or missing the .vhd extension on the file name.</span></span><br/>                                      |
| <dl> <span data-ttu-id="425c6-127"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-127"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="425c6-128">Un paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="425c6-128">A parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="425c6-129">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="425c6-130">Le système ne trouve pas le chemin d’accès spécifié par le paramètre *convertedDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="425c6-130">The system cannot find the path specified by the *convertedDiskImagePath* parameter.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="425c6-131">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="425c6-132">Le paramètre *convertedDiskImagePath* contient un caractère non valide (l’un des caractères \* suivants : «  ? <>/ \| » :»).</span><span class="sxs-lookup"><span data-stu-id="425c6-132">The *convertedDiskImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="425c6-133">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="425c6-134">Le paramètre *convertedDiskImagePath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="425c6-134">The *convertedDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="425c6-135">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="425c6-135">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="425c6-136">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="425c6-137">Le chemin d’accès spécifié par le paramètre *convertedDiskImagePath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="425c6-137">The path specified by the *convertedDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="425c6-138">Le chemin d’accès doit être inférieur à la **longueur maximale \_** (260) caractères.</span><span class="sxs-lookup"><span data-stu-id="425c6-138">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="425c6-139">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="425c6-140">Soit le disque dur virtuel référencé par cet objet est en cours d’utilisation, soit le parent de ce disque dur virtuel est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="425c6-140">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                  |
| <dl> <span data-ttu-id="425c6-141">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="425c6-142">Le volume hôte ne dispose pas de suffisamment d’espace pour convertir ce disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="425c6-142">The host volume does not have enough space to convert this virtual hard disk.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="425c6-143">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-143"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="425c6-144">Le fichier référencé par le paramètre *convertedDiskImagePath* existe déjà.</span><span class="sxs-lookup"><span data-stu-id="425c6-144">The file referenced by the *convertedDiskImagePath* parameter already exists.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="425c6-145"><dt>**Ordinateur virtuel \_ E \_ mauvais \_ \_ \_ type d’image HD**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-145"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="425c6-146">Le paramètre *convertedDiskImagePath* doit être **VmDiskType \_ dynamique** ou **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="425c6-146">The *convertedDiskImagePath* parameter must be either **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/>                          |
| <dl> <span data-ttu-id="425c6-147"><dt>**Ordinateur virtuel \_ E \_ \_ \_ fichier HD 0xA0040682 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="425c6-147"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="425c6-148">L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) ne semble pas être une image valide.</span><span class="sxs-lookup"><span data-stu-id="425c6-148">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |
| <dl> <span data-ttu-id="425c6-149"><dt>**Ordinateur virtuel \_ \_Chemin parent \_ E \_ \_ introuvable**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-149"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="425c6-150">Le parent du disque dur virtuel référencé par cet objet n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="425c6-150">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="425c6-151"><dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-151"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="425c6-152">L’image de disque dur virtuel ne peut pas être convertie parce que l’application est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="425c6-152">The virtual hard disk image cannot be converted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="425c6-153"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="425c6-154">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="425c6-154">An unexpected error has occurred.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="425c6-155">Notes</span><span class="sxs-lookup"><span data-stu-id="425c6-155">Remarks</span></span>

<span data-ttu-id="425c6-156">Le fichier source reste intact après le processus de conversion.</span><span class="sxs-lookup"><span data-stu-id="425c6-156">The source file is left intact after the conversion process.</span></span>

## <a name="requirements"></a><span data-ttu-id="425c6-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="425c6-157">Requirements</span></span>



| <span data-ttu-id="425c6-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="425c6-158">Requirement</span></span> | <span data-ttu-id="425c6-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="425c6-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="425c6-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="425c6-160">Minimum supported client</span></span><br/> | <span data-ttu-id="425c6-161">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="425c6-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="425c6-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="425c6-162">Minimum supported server</span></span><br/> | <span data-ttu-id="425c6-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="425c6-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="425c6-164">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="425c6-164">End of client support</span></span><br/>    | <span data-ttu-id="425c6-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="425c6-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="425c6-166">Produit</span><span class="sxs-lookup"><span data-stu-id="425c6-166">Product</span></span><br/>                  | <span data-ttu-id="425c6-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="425c6-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="425c6-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="425c6-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="425c6-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="425c6-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="425c6-170">IID</span><span class="sxs-lookup"><span data-stu-id="425c6-170">IID</span></span><br/>                      | <span data-ttu-id="425c6-171">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="425c6-171">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="425c6-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="425c6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425c6-173">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="425c6-173">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

