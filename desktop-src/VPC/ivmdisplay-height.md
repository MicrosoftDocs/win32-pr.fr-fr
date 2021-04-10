---
title: Propriété Height de IVMDisplay (VPCCOMInterfaces. h)
description: Hauteur de l’affichage de la machine virtuelle, en pixels.
ms.assetid: 4fbb7c2b-6d5f-4af6-b8cc-3a7546b15cbd
keywords:
- Propriété de hauteur Virtual PC
- Propriété de hauteur Virtual PC, interface IVMDisplay
- IVMDisplay interface Virtual PC, propriété Height
topic_type:
- apiref
api_name:
- IVMDisplay.Height
- IVMDisplay.get_Height
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6ff5746c817dcc81b353f80e2daa345b5587fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032932"
---
# <a name="ivmdisplayheight-property"></a><span data-ttu-id="d2e1c-106">IVMDisplay :: Height, propriété</span><span class="sxs-lookup"><span data-stu-id="d2e1c-106">IVMDisplay::Height property</span></span>

<span data-ttu-id="d2e1c-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d2e1c-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d2e1c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d2e1c-109">Récupère la hauteur de l’affichage de l’ordinateur virtuel, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-109">Retrieves the height of the virtual machine's display, in pixels.</span></span>

<span data-ttu-id="d2e1c-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e1c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2e1c-111">Syntax</span></span>


```C++
HRESULT get_Height(
  [out, retval] long *displayPixelHeight
);
```



## <a name="property-value"></a><span data-ttu-id="d2e1c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d2e1c-112">Property value</span></span>

<span data-ttu-id="d2e1c-113">Hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-113">The height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d2e1c-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d2e1c-114">Error codes</span></span>



| <span data-ttu-id="d2e1c-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="d2e1c-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="d2e1c-116">Signification</span><span class="sxs-lookup"><span data-stu-id="d2e1c-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2e1c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d2e1c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="d2e1c-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d2e1c-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d2e1c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="d2e1c-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d2e1c-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d2e1c-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="d2e1c-122">L’ordinateur virtuel doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="d2e1c-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="d2e1c-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="d2e1c-124">L’ordinateur virtuel n’est pas valide ou n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="d2e1c-125"><dt>Ordinateur virtuel \_ E \_ aucun \_ </dt> <dt>0xA0040850</dt> d’affichage</span><span class="sxs-lookup"><span data-stu-id="d2e1c-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="d2e1c-126">Impossible de trouver un affichage valide pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="d2e1c-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d2e1c-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="d2e1c-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d2e1c-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="d2e1c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2e1c-129">Requirements</span></span>



| <span data-ttu-id="d2e1c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2e1c-130">Requirement</span></span> | <span data-ttu-id="d2e1c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2e1c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e1c-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2e1c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e1c-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2e1c-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2e1c-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2e1c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e1c-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2e1c-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d2e1c-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d2e1c-136">End of client support</span></span><br/>    | <span data-ttu-id="d2e1c-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2e1c-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d2e1c-138">Produit</span><span class="sxs-lookup"><span data-stu-id="d2e1c-138">Product</span></span><br/>                  | <span data-ttu-id="d2e1c-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d2e1c-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d2e1c-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2e1c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2e1c-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2e1c-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d2e1c-142">IID</span><span class="sxs-lookup"><span data-stu-id="d2e1c-142">IID</span></span><br/>                      | <span data-ttu-id="d2e1c-143">IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="d2e1c-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d2e1c-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2e1c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e1c-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="d2e1c-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

