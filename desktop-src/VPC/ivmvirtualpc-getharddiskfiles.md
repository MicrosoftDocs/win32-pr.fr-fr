---
title: Méthode IVMVirtualPC GetHardDiskFiles (VPCCOMInterfaces. h)
description: Récupère un tableau de fichiers de disque dur virtuel connus.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- Méthode GetHardDiskFiles Virtual PC
- Méthode GetHardDiskFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetHardDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4162ae2667d389b445f44973c89a60fafd4c772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509246"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a><span data-ttu-id="46a39-106">IVMVirtualPC :: GetHardDiskFiles, méthode</span><span class="sxs-lookup"><span data-stu-id="46a39-106">IVMVirtualPC::GetHardDiskFiles method</span></span>

<span data-ttu-id="46a39-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="46a39-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="46a39-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="46a39-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="46a39-109">Récupère un tableau de fichiers de disque dur virtuel connus.</span><span class="sxs-lookup"><span data-stu-id="46a39-109">Retrieves an array of known virtual hard disk files.</span></span>

## <a name="syntax"></a><span data-ttu-id="46a39-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46a39-110">Syntax</span></span>


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a><span data-ttu-id="46a39-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46a39-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46a39-112">*inAdditionalSearchPaths* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46a39-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46a39-113">Ces chemins d’accès seront recherchés avec les chemins d’accès définis dans la propriété [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) .</span><span class="sxs-lookup"><span data-stu-id="46a39-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="46a39-114">*outHardDiskFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="46a39-114">*outHardDiskFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="46a39-115">Tableau de chaînes de chemin d’accès pour les fichiers de disque dur virtuel trouvés dans les chemins de recherche spécifiés.</span><span class="sxs-lookup"><span data-stu-id="46a39-115">An array of path strings for the virtual hard disk files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46a39-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46a39-116">Return value</span></span>

<span data-ttu-id="46a39-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="46a39-117">This method can return one of these values.</span></span>



| <span data-ttu-id="46a39-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="46a39-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="46a39-119">Description</span><span class="sxs-lookup"><span data-stu-id="46a39-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46a39-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="46a39-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="46a39-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="46a39-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="46a39-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="46a39-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="46a39-123">Le paramètre *outHardDiskFileList* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="46a39-123">The *outHardDiskFileList* parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="46a39-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="46a39-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="46a39-125">Le paramètre *inAdditionalSearchPaths* n’est pas un tableau de chaînes.</span><span class="sxs-lookup"><span data-stu-id="46a39-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="46a39-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="46a39-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="46a39-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="46a39-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="46a39-128"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="46a39-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="46a39-129">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="46a39-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="46a39-130">Notes</span><span class="sxs-lookup"><span data-stu-id="46a39-130">Remarks</span></span>

<span data-ttu-id="46a39-131">Les chemins de recherche utilisés pour récupérer le tableau de fichiers incluent ceux qui ont été précédemment définis par [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) en plus de ceux spécifiés par le paramètre *inAdditionalSearchPaths* .</span><span class="sxs-lookup"><span data-stu-id="46a39-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="46a39-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46a39-132">Requirements</span></span>



| <span data-ttu-id="46a39-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46a39-133">Requirement</span></span> | <span data-ttu-id="46a39-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="46a39-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="46a39-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46a39-135">Minimum supported client</span></span><br/> | <span data-ttu-id="46a39-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46a39-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46a39-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46a39-137">Minimum supported server</span></span><br/> | <span data-ttu-id="46a39-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="46a39-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="46a39-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="46a39-139">End of client support</span></span><br/>    | <span data-ttu-id="46a39-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="46a39-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="46a39-141">Produit</span><span class="sxs-lookup"><span data-stu-id="46a39-141">Product</span></span><br/>                  | <span data-ttu-id="46a39-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="46a39-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="46a39-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="46a39-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="46a39-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="46a39-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="46a39-145">IID</span><span class="sxs-lookup"><span data-stu-id="46a39-145">IID</span></span><br/>                      | <span data-ttu-id="46a39-146">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="46a39-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="46a39-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46a39-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46a39-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="46a39-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

