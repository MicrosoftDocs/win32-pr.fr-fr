---
title: IVMVirtualPC SearchPaths, propriété (VPCCOMInterfaces. h)
description: Chemins d’accès de système de fichiers utilisés pour rechercher des fichiers associés à Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- SearchPaths propriété Virtual PC
- SearchPaths, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété SearchPaths
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739748"
---
# <a name="ivmvirtualpcsearchpaths-property"></a><span data-ttu-id="134c5-106">IVMVirtualPC :: SearchPaths, propriété</span><span class="sxs-lookup"><span data-stu-id="134c5-106">IVMVirtualPC::SearchPaths property</span></span>

<span data-ttu-id="134c5-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="134c5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="134c5-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="134c5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="134c5-109">Récupère et définit les chemins d’accès du système de fichiers qui sont utilisés pour rechercher des fichiers associés à Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="134c5-109">Retrieves and sets the file system paths that are used to find files associated with Windows Virtual PC.</span></span>

<span data-ttu-id="134c5-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="134c5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="134c5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="134c5-111">Syntax</span></span>


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a><span data-ttu-id="134c5-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="134c5-112">Property value</span></span>

<span data-ttu-id="134c5-113">Spécifie un SafeArray contenant un chemin d’accès au système de fichiers pour chaque entrée.</span><span class="sxs-lookup"><span data-stu-id="134c5-113">Specifies a safearray containing a file system path for each entry.</span></span>

## <a name="error-codes"></a><span data-ttu-id="134c5-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="134c5-114">Error codes</span></span>



| <span data-ttu-id="134c5-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="134c5-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="134c5-116">Signification</span><span class="sxs-lookup"><span data-stu-id="134c5-116">Meaning</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="134c5-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="134c5-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="134c5-118">The operation was successful.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="134c5-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="134c5-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="134c5-120">The parameter is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="134c5-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="134c5-122">Le paramètre *searchPaths* n’est pas valide et n’a pas pu être analysé dans un tableau de chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="134c5-122">The *searchPaths* parameter is not valid and could not be parsed into an array of paths.</span></span><br/>                                    |
| <dl> <span data-ttu-id="134c5-123">Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="134c5-124">Le système ne peut pas trouver un répertoire spécifié dans le paramètre *searchPaths* .</span><span class="sxs-lookup"><span data-stu-id="134c5-124">The system cannot find a directory specified in the *searchPaths* parameter.</span></span><br/>                                                |
| <dl> <span data-ttu-id="134c5-125">Valeur <dt>HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="134c5-126">Le système ne trouve pas de chemin d’accès spécifié par le paramètre *searchPaths* .</span><span class="sxs-lookup"><span data-stu-id="134c5-126">The system cannot find a path specified by the *searchPaths* parameter.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="134c5-127">Valeur <dt>HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-127"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="134c5-128">Un chemin d’accès spécifié dans le paramètre *searchPaths* contient des caractères non conformes.</span><span class="sxs-lookup"><span data-stu-id="134c5-128">A path specified in the *searchPaths* parameter contains illegal characters.</span></span> <span data-ttu-id="134c5-129">Les caractères non autorisés sont « \* ? <>/ \| » : «».</span><span class="sxs-lookup"><span data-stu-id="134c5-129">The illegal characters are "\*?<>/\|":".</span></span><br/> |
| <dl> <span data-ttu-id="134c5-130">Valeur <dt>HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-130"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="134c5-131">Un chemin d’accès contenu dans le paramètre *searchPaths* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="134c5-131">A path contained in the *searchPaths* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="134c5-132">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="134c5-132">An absolute path is required.</span></span><br/>          |
| <dl> <span data-ttu-id="134c5-133">Valeur <dt>HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-133"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="134c5-134">Le chemin d’accès spécifié dans le paramètre *searchPaths* est trop long.</span><span class="sxs-lookup"><span data-stu-id="134c5-134">The path specified in the *searchPaths* parameter is too long.</span></span> <span data-ttu-id="134c5-135">La longueur du chemin d’accès doit être inférieure à 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="134c5-135">The length of the path must be less than 260 characters.</span></span><br/>     |
| <dl> <span data-ttu-id="134c5-136"><dt>Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-136"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl>                       | <span data-ttu-id="134c5-137">La préférence est introuvable.</span><span class="sxs-lookup"><span data-stu-id="134c5-137">The preference was not found.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="134c5-138"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-138"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="134c5-139">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="134c5-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                        |
| <dl> <span data-ttu-id="134c5-140"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-140"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="134c5-141">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="134c5-141">An unexpected error has occurred.</span></span><br/>                                                                                           |



## <a name="requirements"></a><span data-ttu-id="134c5-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="134c5-142">Requirements</span></span>



| <span data-ttu-id="134c5-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="134c5-143">Requirement</span></span> | <span data-ttu-id="134c5-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="134c5-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="134c5-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="134c5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="134c5-146">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="134c5-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="134c5-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="134c5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="134c5-148">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="134c5-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="134c5-149">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="134c5-149">End of client support</span></span><br/>    | <span data-ttu-id="134c5-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="134c5-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="134c5-151">Produit</span><span class="sxs-lookup"><span data-stu-id="134c5-151">Product</span></span><br/>                  | <span data-ttu-id="134c5-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="134c5-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="134c5-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="134c5-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="134c5-154"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="134c5-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="134c5-155">IID</span><span class="sxs-lookup"><span data-stu-id="134c5-155">IID</span></span><br/>                      | <span data-ttu-id="134c5-156">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="134c5-156">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="134c5-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="134c5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="134c5-158">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="134c5-158">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

