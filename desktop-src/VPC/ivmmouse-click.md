---
title: IVMMouse Click, méthode (VPCCOMInterfaces. h)
description: Simule un clic sur le bouton de la souris.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Cliquez sur méthode Virtual PC
- Cliquez sur méthode Virtual PC, interface IVMMouse
- IVMMouse interface Virtual PC, méthode click
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ea1b861db0a92ad92e689770182d225778aee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466830"
---
# <a name="ivmmouseclick-method"></a><span data-ttu-id="49e2f-106">IVMMouse :: Click, méthode</span><span class="sxs-lookup"><span data-stu-id="49e2f-106">IVMMouse::Click method</span></span>

<span data-ttu-id="49e2f-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="49e2f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="49e2f-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="49e2f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="49e2f-109">Simule un clic sur le bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="49e2f-109">Simulates a mouse button click.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e2f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49e2f-110">Syntax</span></span>


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="49e2f-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49e2f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e2f-112">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49e2f-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e2f-113">Index du bouton sur lequel un clic a été effectué.</span><span class="sxs-lookup"><span data-stu-id="49e2f-113">The index of the button being clicked.</span></span> <span data-ttu-id="49e2f-114">Pour obtenir la liste des valeurs, consultez [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="49e2f-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e2f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49e2f-115">Return value</span></span>

<span data-ttu-id="49e2f-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="49e2f-116">This method can return one of these values.</span></span>



| <span data-ttu-id="49e2f-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="49e2f-117">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="49e2f-118">Description</span><span class="sxs-lookup"><span data-stu-id="49e2f-118">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49e2f-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="49e2f-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="49e2f-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="49e2f-120">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="49e2f-121"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="49e2f-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="49e2f-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="49e2f-122">The parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="49e2f-123"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="49e2f-123"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="49e2f-124">L’ordinateur virtuel auquel ce périphérique de souris est attaché n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="49e2f-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="49e2f-125"><dt>**Ordinateur virtuel \_ E \_ souris \_ non \_ active**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="49e2f-125"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="49e2f-126">L’opération n’a pas pu aboutir car le périphérique de la souris n’est pas sous tension ou n’est pas actuellement actif sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="49e2f-126">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="49e2f-127"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="49e2f-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="49e2f-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="49e2f-128">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="49e2f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49e2f-129">Requirements</span></span>



| <span data-ttu-id="49e2f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49e2f-130">Requirement</span></span> | <span data-ttu-id="49e2f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="49e2f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e2f-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49e2f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="49e2f-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49e2f-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49e2f-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49e2f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="49e2f-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="49e2f-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="49e2f-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="49e2f-136">End of client support</span></span><br/>    | <span data-ttu-id="49e2f-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="49e2f-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="49e2f-138">Produit</span><span class="sxs-lookup"><span data-stu-id="49e2f-138">Product</span></span><br/>                  | <span data-ttu-id="49e2f-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="49e2f-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="49e2f-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="49e2f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="49e2f-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="49e2f-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="49e2f-142">IID</span><span class="sxs-lookup"><span data-stu-id="49e2f-142">IID</span></span><br/>                      | <span data-ttu-id="49e2f-143">IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="49e2f-143">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="49e2f-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49e2f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e2f-145">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="49e2f-145">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

