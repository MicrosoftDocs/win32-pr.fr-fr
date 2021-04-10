---
title: IVMDisplay VideoMode, propriété (VPCCOMInterfaces. h)
description: Récupère le mode vidéo actuel.
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- VideoMode propriété Virtual PC
- VideoMode, propriété Virtual PC, IVMDisplay, interface
- IVMDisplay interface Virtual PC, propriété VideoMode
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164a658766cb8973a7c1ac403756ee888abab1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942081"
---
# <a name="ivmdisplayvideomode-property"></a><span data-ttu-id="c3b09-106">IVMDisplay :: VideoMode, propriété</span><span class="sxs-lookup"><span data-stu-id="c3b09-106">IVMDisplay::VideoMode property</span></span>

<span data-ttu-id="c3b09-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c3b09-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c3b09-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c3b09-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c3b09-109">Récupère le mode vidéo actuel.</span><span class="sxs-lookup"><span data-stu-id="c3b09-109">Retrieves the current video mode.</span></span>

<span data-ttu-id="c3b09-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c3b09-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3b09-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3b09-111">Syntax</span></span>


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a><span data-ttu-id="c3b09-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c3b09-112">Property value</span></span>

<span data-ttu-id="c3b09-113">Mode vidéo actuel du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="c3b09-113">The current video mode of the guest operating system.</span></span> <span data-ttu-id="c3b09-114">Pour obtenir la liste des valeurs, consultez [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span><span class="sxs-lookup"><span data-stu-id="c3b09-114">For a list of values, see [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="c3b09-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c3b09-115">Error codes</span></span>



| <span data-ttu-id="c3b09-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="c3b09-116">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="c3b09-117">Signification</span><span class="sxs-lookup"><span data-stu-id="c3b09-117">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3b09-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c3b09-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="c3b09-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c3b09-119">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c3b09-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c3b09-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="c3b09-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c3b09-121">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c3b09-122"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="c3b09-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="c3b09-123">L’ordinateur virtuel doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="c3b09-123">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="c3b09-124"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="c3b09-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="c3b09-125">L’ordinateur virtuel n’est pas valide ou n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c3b09-125">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="c3b09-126"><dt>Ordinateur virtuel \_ E \_ aucun \_ </dt> <dt>0xA0040850</dt> d’affichage</span><span class="sxs-lookup"><span data-stu-id="c3b09-126"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="c3b09-127">Impossible de trouver un affichage valide pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c3b09-127">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="c3b09-128"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c3b09-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="c3b09-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c3b09-129">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="c3b09-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3b09-130">Requirements</span></span>



| <span data-ttu-id="c3b09-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3b09-131">Requirement</span></span> | <span data-ttu-id="c3b09-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3b09-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b09-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3b09-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c3b09-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3b09-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3b09-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3b09-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c3b09-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3b09-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c3b09-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c3b09-137">End of client support</span></span><br/>    | <span data-ttu-id="c3b09-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3b09-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c3b09-139">Produit</span><span class="sxs-lookup"><span data-stu-id="c3b09-139">Product</span></span><br/>                  | <span data-ttu-id="c3b09-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c3b09-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c3b09-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3b09-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3b09-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3b09-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c3b09-143">IID</span><span class="sxs-lookup"><span data-stu-id="c3b09-143">IID</span></span><br/>                      | <span data-ttu-id="c3b09-144">IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="c3b09-144">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="c3b09-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3b09-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3b09-146">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="c3b09-146">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

