---
title: Méthode IVMFloppyDrive AttachImage (VPCCOMInterfaces. h)
description: Attache une image de support de disquette sur l’ordinateur hôte au lecteur de disquette de la machine virtuelle.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Méthode AttachImage Virtual PC
- Méthode AttachImage Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, méthode AttachImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941979"
---
# <a name="ivmfloppydriveattachimage-method"></a><span data-ttu-id="b06eb-106">IVMFloppyDrive :: AttachImage, méthode</span><span class="sxs-lookup"><span data-stu-id="b06eb-106">IVMFloppyDrive::AttachImage method</span></span>

<span data-ttu-id="b06eb-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b06eb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b06eb-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b06eb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b06eb-109">Attache une image de support de disquette sur l’ordinateur hôte au lecteur de disquette de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b06eb-109">Attaches a floppy media image on the host to the floppy drive of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="b06eb-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b06eb-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a><span data-ttu-id="b06eb-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b06eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b06eb-112">*mediaImagePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b06eb-112">*mediaImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b06eb-113">Le chemin d’accès complet à l’image de support de disquette à attacher.</span><span class="sxs-lookup"><span data-stu-id="b06eb-113">The full path to the floppy media image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b06eb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b06eb-114">Return value</span></span>

<span data-ttu-id="b06eb-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b06eb-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b06eb-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b06eb-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="b06eb-117">Description</span><span class="sxs-lookup"><span data-stu-id="b06eb-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b06eb-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b06eb-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b06eb-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="b06eb-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="b06eb-121">Le paramètre *mediaImagePath* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b06eb-121">The *mediaImagePath* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b06eb-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="b06eb-123">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b06eb-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="b06eb-124">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="b06eb-125">La mémoire disponible est insuffisante pour effectuer cette requête.</span><span class="sxs-lookup"><span data-stu-id="b06eb-125">There is not enough memory available to complete this request.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="b06eb-126">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="b06eb-127">Le chemin d’accès spécifié par le paramètre *mediaImagePath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="b06eb-127">The path specified by the *mediaImagePath* parameter is too long.</span></span> <span data-ttu-id="b06eb-128">Le chemin d’accès doit être inférieur à la **longueur maximale \_** (260) caractères.</span><span class="sxs-lookup"><span data-stu-id="b06eb-128">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="b06eb-129">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="b06eb-130">Le paramètre *mediaImagePath* contient un caractère non valide (l’un des caractères \* suivants : «  ? <>/ \| » :»).</span><span class="sxs-lookup"><span data-stu-id="b06eb-130">The *mediaImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="b06eb-131">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="b06eb-132">Le paramètre *mediaImagePath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="b06eb-132">The *mediaImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="b06eb-133">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="b06eb-133">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="b06eb-134"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="b06eb-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="b06eb-135">La configuration de cette machine virtuelle n’est pas valide ou est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b06eb-135">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="b06eb-136"><dt>**Ordinateur virtuel \_ Échec de la \_ \_ capture \_ d’image E**</dt> <dt>0xA00400650</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-136"><dt>**VM\_E\_IMAGE\_CAPTURE\_FAIL**</dt> <dt>0xA00400650</dt></span></span> </dl>                  | <span data-ttu-id="b06eb-137">Impossible de capturer le fichier image spécifié.</span><span class="sxs-lookup"><span data-stu-id="b06eb-137">The image file specified could not be captured.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b06eb-138"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b06eb-139">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b06eb-139">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="b06eb-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b06eb-140">Requirements</span></span>



| <span data-ttu-id="b06eb-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b06eb-141">Requirement</span></span> | <span data-ttu-id="b06eb-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="b06eb-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b06eb-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b06eb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b06eb-144">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b06eb-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b06eb-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b06eb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b06eb-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b06eb-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b06eb-147">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b06eb-147">End of client support</span></span><br/>    | <span data-ttu-id="b06eb-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b06eb-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b06eb-149">Produit</span><span class="sxs-lookup"><span data-stu-id="b06eb-149">Product</span></span><br/>                  | <span data-ttu-id="b06eb-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b06eb-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b06eb-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="b06eb-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="b06eb-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b06eb-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b06eb-153">IID</span><span class="sxs-lookup"><span data-stu-id="b06eb-153">IID</span></span><br/>                      | <span data-ttu-id="b06eb-154">IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="b06eb-154">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b06eb-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b06eb-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b06eb-156">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="b06eb-156">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

