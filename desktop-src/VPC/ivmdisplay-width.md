---
title: Propriété Width de IVMDisplay (VPCCOMInterfaces. h)
description: Largeur de l’affichage de la machine virtuelle, en pixels.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Propriété Width de Virtual PC
- Propriété de largeur Virtual PC, interface IVMDisplay
- IVMDisplay interface Virtual PC, propriété Width
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b6fe7d329498b0f1ffc36304311f733cd990c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509258"
---
# <a name="ivmdisplaywidth-property"></a><span data-ttu-id="4297f-106">IVMDisplay :: Width, propriété</span><span class="sxs-lookup"><span data-stu-id="4297f-106">IVMDisplay::Width property</span></span>

<span data-ttu-id="4297f-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4297f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4297f-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4297f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4297f-109">Récupère, en pixels, la largeur de l’affichage de la machine virtuelle (de la machine virtuelle).</span><span class="sxs-lookup"><span data-stu-id="4297f-109">Retrieves the width of the virtual machine's (VM's) display, in pixels.</span></span>

<span data-ttu-id="4297f-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4297f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4297f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4297f-111">Syntax</span></span>


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a><span data-ttu-id="4297f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4297f-112">Property value</span></span>

<span data-ttu-id="4297f-113">Largeur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="4297f-113">The width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4297f-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4297f-114">Error codes</span></span>



| <span data-ttu-id="4297f-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="4297f-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="4297f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="4297f-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4297f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4297f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="4297f-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4297f-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="4297f-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4297f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="4297f-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4297f-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4297f-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4297f-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="4297f-122">L’ordinateur virtuel doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="4297f-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="4297f-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="4297f-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="4297f-124">L’ordinateur virtuel n’est pas valide ou n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4297f-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="4297f-125"><dt>Ordinateur virtuel \_ E \_ aucun \_ </dt> <dt>0xA0040850</dt> d’affichage</span><span class="sxs-lookup"><span data-stu-id="4297f-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="4297f-126">Impossible de trouver un affichage valide pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4297f-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="4297f-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4297f-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="4297f-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4297f-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="4297f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4297f-129">Requirements</span></span>



| <span data-ttu-id="4297f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4297f-130">Requirement</span></span> | <span data-ttu-id="4297f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4297f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4297f-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4297f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4297f-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4297f-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4297f-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4297f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4297f-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4297f-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4297f-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4297f-136">End of client support</span></span><br/>    | <span data-ttu-id="4297f-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4297f-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4297f-138">Produit</span><span class="sxs-lookup"><span data-stu-id="4297f-138">Product</span></span><br/>                  | <span data-ttu-id="4297f-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4297f-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4297f-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="4297f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4297f-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4297f-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4297f-142">IID</span><span class="sxs-lookup"><span data-stu-id="4297f-142">IID</span></span><br/>                      | <span data-ttu-id="4297f-143">IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="4297f-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4297f-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4297f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4297f-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="4297f-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

