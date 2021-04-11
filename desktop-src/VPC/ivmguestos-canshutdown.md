---
title: IVMGuestOS CanShutdown, propriété (VPCCOMInterfaces. h)
description: Indique si le système d’exploitation invité peut être arrêté proprement.
ms.assetid: 239cba43-9494-4efd-a4c8-0bb47f476b81
keywords:
- CanShutdown propriété Virtual PC
- CanShutdown, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété CanShutdown
topic_type:
- apiref
api_name:
- IVMGuestOS.CanShutdown
- IVMGuestOS.get_CanShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f76e652b7a172da6f5a438f72b09443a13dcce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317474"
---
# <a name="ivmguestoscanshutdown-property"></a><span data-ttu-id="6fb37-106">IVMGuestOS :: CanShutdown, propriété</span><span class="sxs-lookup"><span data-stu-id="6fb37-106">IVMGuestOS::CanShutdown property</span></span>

<span data-ttu-id="6fb37-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6fb37-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6fb37-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6fb37-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6fb37-109">Indique si le système d’exploitation invité peut être arrêté proprement (nécessite des composants d’intégration).</span><span class="sxs-lookup"><span data-stu-id="6fb37-109">Indicates whether the guest operating system can be cleanly shut down (requires Integration Components).</span></span>

<span data-ttu-id="6fb37-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6fb37-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb37-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fb37-111">Syntax</span></span>


```C++
HRESULT get_CanShutdown(
  [out, retval] VARIANT_BOOL *canShutdown
);
```



## <a name="property-value"></a><span data-ttu-id="6fb37-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6fb37-112">Property value</span></span>

<span data-ttu-id="6fb37-113">**Variante \_ TRUE** si le système d’exploitation prend en charge l’opération d’arrêt et la **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6fb37-113">**VARIANT\_TRUE** if the operating system supports the shutdown operation and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6fb37-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6fb37-114">Error codes</span></span>



| <span data-ttu-id="6fb37-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="6fb37-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6fb37-116">Signification</span><span class="sxs-lookup"><span data-stu-id="6fb37-116">Meaning</span></span>                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="6fb37-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6fb37-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6fb37-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6fb37-118">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="6fb37-119"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6fb37-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="6fb37-120">L’ordinateur virtuel n’est pas allumé.</span><span class="sxs-lookup"><span data-stu-id="6fb37-120">The virtual machine is not turned on.</span></span><br/>   |
| <dl> <span data-ttu-id="6fb37-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6fb37-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6fb37-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6fb37-122">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="6fb37-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="6fb37-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6fb37-124">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="6fb37-124">The virtual machine could not be found.</span></span><br/> |
| <dl> <span data-ttu-id="6fb37-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6fb37-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6fb37-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6fb37-126">An unexpected error has occurred.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="6fb37-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fb37-127">Requirements</span></span>



| <span data-ttu-id="6fb37-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fb37-128">Requirement</span></span> | <span data-ttu-id="6fb37-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fb37-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb37-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fb37-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb37-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fb37-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6fb37-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fb37-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb37-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fb37-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6fb37-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6fb37-134">End of client support</span></span><br/>    | <span data-ttu-id="6fb37-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6fb37-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6fb37-136">Produit</span><span class="sxs-lookup"><span data-stu-id="6fb37-136">Product</span></span><br/>                  | <span data-ttu-id="6fb37-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6fb37-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6fb37-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fb37-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fb37-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fb37-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6fb37-140">IID</span><span class="sxs-lookup"><span data-stu-id="6fb37-140">IID</span></span><br/>                      | <span data-ttu-id="6fb37-141">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="6fb37-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6fb37-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fb37-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb37-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="6fb37-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

