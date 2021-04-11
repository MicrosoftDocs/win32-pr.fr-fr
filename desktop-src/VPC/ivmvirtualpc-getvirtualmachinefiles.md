---
title: Méthode IVMVirtualPC GetVirtualMachineFiles (VPCCOMInterfaces. h)
description: Récupère un tableau de fichiers de configuration d’ordinateur virtuel connus.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- Méthode GetVirtualMachineFiles Virtual PC
- Méthode GetVirtualMachineFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetVirtualMachineFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317466"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a><span data-ttu-id="77ebf-106">IVMVirtualPC :: GetVirtualMachineFiles, méthode</span><span class="sxs-lookup"><span data-stu-id="77ebf-106">IVMVirtualPC::GetVirtualMachineFiles method</span></span>

<span data-ttu-id="77ebf-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77ebf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="77ebf-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="77ebf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="77ebf-109">Récupère un tableau de fichiers de configuration d’ordinateur virtuel connus.</span><span class="sxs-lookup"><span data-stu-id="77ebf-109">Retrieves an array of known virtual machine configuration files.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ebf-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77ebf-110">Syntax</span></span>


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a><span data-ttu-id="77ebf-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77ebf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77ebf-112">*inAdditionalSearchPaths* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77ebf-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ebf-113">Ces chemins d’accès seront recherchés avec les chemins d’accès définis dans les propriétés [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) et [**IVMVirtualPC ::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) .</span><span class="sxs-lookup"><span data-stu-id="77ebf-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="77ebf-114">*inExcludedRegisteredVMs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77ebf-114">*inExcludedRegisteredVMs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ebf-115">**True** si les machines virtuelles inscrites doivent être exclues du retour de tableau dans le paramètre *outVirtualMachineFileList* et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="77ebf-115">**TRUE** if registered virtual machines should be excluded from the array return in the *outVirtualMachineFileList* parameter and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="77ebf-116">*outVirtualMachineFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="77ebf-116">*outVirtualMachineFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="77ebf-117">Tableau de chaînes de chemin d’accès pour les fichiers de configuration d’ordinateur virtuel trouvés dans les chemins de recherche spécifiés.</span><span class="sxs-lookup"><span data-stu-id="77ebf-117">An array of path strings for the virtual machine configuration files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77ebf-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77ebf-118">Return value</span></span>

<span data-ttu-id="77ebf-119">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="77ebf-119">This method can return one of these values.</span></span>



| <span data-ttu-id="77ebf-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="77ebf-120">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="77ebf-121">Description</span><span class="sxs-lookup"><span data-stu-id="77ebf-121">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77ebf-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="77ebf-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="77ebf-123">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="77ebf-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="77ebf-124"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="77ebf-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="77ebf-125">Le paramètre *outVirtualMachineFileList* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="77ebf-125">The *outVirtualMachineFileList* parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="77ebf-126"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="77ebf-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="77ebf-127">Le paramètre *inAdditionalSearchPaths* n’est pas un tableau de chaînes.</span><span class="sxs-lookup"><span data-stu-id="77ebf-127">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="77ebf-128"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="77ebf-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="77ebf-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="77ebf-129">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="77ebf-130"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="77ebf-130"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="77ebf-131">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="77ebf-131">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="77ebf-132">Notes</span><span class="sxs-lookup"><span data-stu-id="77ebf-132">Remarks</span></span>

<span data-ttu-id="77ebf-133">Les chemins de recherche utilisés pour récupérer le tableau de fichiers de configuration incluent ceux qui ont été précédemment définis par [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) et [**IVMVirtualPC ::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) en plus de ceux spécifiés par le paramètre *inAdditionalSearchPaths* .</span><span class="sxs-lookup"><span data-stu-id="77ebf-133">The search paths used to retrieve the array of configuration files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ebf-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77ebf-134">Requirements</span></span>



| <span data-ttu-id="77ebf-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77ebf-135">Requirement</span></span> | <span data-ttu-id="77ebf-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="77ebf-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ebf-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77ebf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="77ebf-138">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77ebf-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77ebf-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77ebf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="77ebf-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="77ebf-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="77ebf-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="77ebf-141">End of client support</span></span><br/>    | <span data-ttu-id="77ebf-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="77ebf-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="77ebf-143">Produit</span><span class="sxs-lookup"><span data-stu-id="77ebf-143">Product</span></span><br/>                  | <span data-ttu-id="77ebf-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="77ebf-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="77ebf-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="77ebf-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="77ebf-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="77ebf-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="77ebf-147">IID</span><span class="sxs-lookup"><span data-stu-id="77ebf-147">IID</span></span><br/>                      | <span data-ttu-id="77ebf-148">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="77ebf-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="77ebf-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77ebf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ebf-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="77ebf-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

