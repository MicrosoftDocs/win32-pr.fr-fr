---
title: IVMDisplay CanResize, propriété (VPCCOMInterfaces. h)
description: Détermine si l’invité autorise les modifications de résolution.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- CanResize propriété Virtual PC
- CanResize, propriété Virtual PC, IVMDisplay, interface
- IVMDisplay interface Virtual PC, propriété CanResize
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca865189b1fd155e0edf85bac9a36d94ffe5d656
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743469"
---
# <a name="ivmdisplaycanresize-property"></a><span data-ttu-id="de5b1-106">IVMDisplay :: CanResize, propriété</span><span class="sxs-lookup"><span data-stu-id="de5b1-106">IVMDisplay::CanResize property</span></span>

<span data-ttu-id="de5b1-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="de5b1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="de5b1-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="de5b1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="de5b1-109">Détermine si l’invité autorise les modifications de résolution.</span><span class="sxs-lookup"><span data-stu-id="de5b1-109">Determines whether the Guest allows resolution changes.</span></span>

<span data-ttu-id="de5b1-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="de5b1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="de5b1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de5b1-111">Syntax</span></span>


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a><span data-ttu-id="de5b1-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="de5b1-112">Property value</span></span>

<span data-ttu-id="de5b1-113">**Variante \_ TRUE** si l’invité autorise les modifications de résolution et la **\_ valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="de5b1-113">**VARIANT\_TRUE** if the Guest allows resolution changes and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="de5b1-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="de5b1-114">Error codes</span></span>



| <span data-ttu-id="de5b1-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="de5b1-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="de5b1-116">Signification</span><span class="sxs-lookup"><span data-stu-id="de5b1-116">Meaning</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de5b1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="de5b1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="de5b1-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="de5b1-118">The operation was successful.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="de5b1-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="de5b1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="de5b1-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="de5b1-120">The parameter is **NULL**.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="de5b1-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="de5b1-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="de5b1-122">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="de5b1-122">The configuration is unknown.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="de5b1-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="de5b1-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="de5b1-124">L’ordinateur virtuel doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="de5b1-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="de5b1-125"><dt>Ordinateur virtuel \_ E \_ aucun \_ </dt> <dt>0xA0040850</dt> d’affichage</span><span class="sxs-lookup"><span data-stu-id="de5b1-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="de5b1-126">Aucun périphérique vidéo n’a été trouvé pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="de5b1-126">There was no video device found for the virtual machine.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="de5b1-127"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="de5b1-127"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="de5b1-128">La fonctionnalité composants d’intégration n’est pas disponible. soit les composants d’intégration ne sont pas installés, soit la fonctionnalité a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="de5b1-128">The integration components feature is not available; either the integration components are not installed or the feature has been disabled.</span></span><br/> |
| <dl> <span data-ttu-id="de5b1-129"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="de5b1-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="de5b1-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="de5b1-130">An unexpected error has occurred.</span></span><br/>                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="de5b1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de5b1-131">Requirements</span></span>



| <span data-ttu-id="de5b1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de5b1-132">Requirement</span></span> | <span data-ttu-id="de5b1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="de5b1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="de5b1-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de5b1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="de5b1-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de5b1-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de5b1-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de5b1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="de5b1-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="de5b1-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="de5b1-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="de5b1-138">End of client support</span></span><br/>    | <span data-ttu-id="de5b1-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="de5b1-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="de5b1-140">Produit</span><span class="sxs-lookup"><span data-stu-id="de5b1-140">Product</span></span><br/>                  | <span data-ttu-id="de5b1-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="de5b1-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="de5b1-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="de5b1-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="de5b1-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="de5b1-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="de5b1-144">IID</span><span class="sxs-lookup"><span data-stu-id="de5b1-144">IID</span></span><br/>                      | <span data-ttu-id="de5b1-145">IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="de5b1-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="de5b1-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de5b1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5b1-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="de5b1-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

