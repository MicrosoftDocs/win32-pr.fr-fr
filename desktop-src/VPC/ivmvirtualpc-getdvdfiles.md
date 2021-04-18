---
title: Méthode IVMVirtualPC GetDVDFiles (VPCCOMInterfaces. h)
description: Récupère un tableau de fichiers de DVD connus.
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- Méthode GetDVDFiles Virtual PC
- Méthode GetDVDFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetDVDFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a91d7f0d65d1f62feb21d41bd9b27bf6ce112ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509340"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a><span data-ttu-id="8cbba-106">IVMVirtualPC :: GetDVDFiles, méthode</span><span class="sxs-lookup"><span data-stu-id="8cbba-106">IVMVirtualPC::GetDVDFiles method</span></span>

<span data-ttu-id="8cbba-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8cbba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8cbba-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8cbba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8cbba-109">Récupère un tableau de fichiers de DVD connus.</span><span class="sxs-lookup"><span data-stu-id="8cbba-109">Retrieves an array of known DVD files.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cbba-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cbba-110">Syntax</span></span>


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a><span data-ttu-id="8cbba-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cbba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cbba-112">*inAdditionalSearchPaths* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8cbba-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cbba-113">Ces chemins d’accès seront recherchés avec les chemins d’accès définis dans la propriété [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) .</span><span class="sxs-lookup"><span data-stu-id="8cbba-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="8cbba-114">*outDVDFileList* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8cbba-114">*outDVDFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8cbba-115">Tableau de fichiers de DVD virtuels trouvés dans les chemins de recherche spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8cbba-115">An array of virtual DVD files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cbba-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8cbba-116">Return value</span></span>

<span data-ttu-id="8cbba-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8cbba-117">This method can return one of these values.</span></span>



| <span data-ttu-id="8cbba-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8cbba-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="8cbba-119">Description</span><span class="sxs-lookup"><span data-stu-id="8cbba-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8cbba-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8cbba-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="8cbba-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8cbba-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="8cbba-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8cbba-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="8cbba-123">Le paramètre *outDVDFileList* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8cbba-123">The *outDVDFileList* parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="8cbba-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8cbba-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="8cbba-125">Le paramètre *inAdditionalSearchPaths* n’est pas un tableau de chaînes.</span><span class="sxs-lookup"><span data-stu-id="8cbba-125">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="8cbba-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8cbba-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="8cbba-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8cbba-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="8cbba-128"><dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="8cbba-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="8cbba-129">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="8cbba-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8cbba-130">Notes</span><span class="sxs-lookup"><span data-stu-id="8cbba-130">Remarks</span></span>

<span data-ttu-id="8cbba-131">Les chemins de recherche utilisés pour récupérer le tableau de fichiers incluent ceux qui ont été précédemment définis par [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) en plus de ceux spécifiés par le paramètre *inAdditionalSearchPaths* et l’emplacement du programme d’installation du module Integration Components.</span><span class="sxs-lookup"><span data-stu-id="8cbba-131">The search paths used to retrieve the array of files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) in addition to those specified by the *inAdditionalSearchPaths* parameter and the installer location for the integration components module.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cbba-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cbba-132">Requirements</span></span>



| <span data-ttu-id="8cbba-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cbba-133">Requirement</span></span> | <span data-ttu-id="8cbba-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cbba-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cbba-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cbba-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8cbba-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cbba-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8cbba-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cbba-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8cbba-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cbba-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8cbba-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8cbba-139">End of client support</span></span><br/>    | <span data-ttu-id="8cbba-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8cbba-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8cbba-141">Produit</span><span class="sxs-lookup"><span data-stu-id="8cbba-141">Product</span></span><br/>                  | <span data-ttu-id="8cbba-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8cbba-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8cbba-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="8cbba-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cbba-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cbba-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8cbba-145">IID</span><span class="sxs-lookup"><span data-stu-id="8cbba-145">IID</span></span><br/>                      | <span data-ttu-id="8cbba-146">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="8cbba-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8cbba-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cbba-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cbba-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="8cbba-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

