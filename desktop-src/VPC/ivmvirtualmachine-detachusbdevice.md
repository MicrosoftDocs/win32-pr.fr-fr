---
title: Méthode IVMVirtualMachine DetachUSBDevice (VPCCOMInterfaces. h)
description: Libère un périphérique USB d’un ordinateur virtuel.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- Méthode DetachUSBDevice Virtual PC
- Méthode DetachUSBDevice Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode DetachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540779"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a><span data-ttu-id="4ea37-106">IVMVirtualMachine ::D méthode etachUSBDevice</span><span class="sxs-lookup"><span data-stu-id="4ea37-106">IVMVirtualMachine::DetachUSBDevice method</span></span>

<span data-ttu-id="4ea37-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4ea37-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4ea37-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4ea37-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4ea37-109">Libère un périphérique USB d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4ea37-109">Releases a USB device from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea37-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ea37-110">Syntax</span></span>


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="4ea37-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ea37-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ea37-112">*inUSBDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ea37-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ea37-113">Pointeur [**IVMUSBDevice**](ivmusbdevice.md) qui représente le périphérique USB à détacher de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4ea37-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device to be detached from the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ea37-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ea37-114">Return value</span></span>

<span data-ttu-id="4ea37-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="4ea37-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4ea37-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4ea37-116">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="4ea37-117">Description</span><span class="sxs-lookup"><span data-stu-id="4ea37-117">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="4ea37-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4ea37-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="4ea37-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4ea37-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="4ea37-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4ea37-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                  | <span data-ttu-id="4ea37-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4ea37-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="4ea37-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4ea37-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>     | <span data-ttu-id="4ea37-123">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4ea37-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="4ea37-124"><dt>**Ordinateur virtuel \_ \_ \_ \_ Échec du détachement d’E**</dt> /r USB <dt>0xA00400927</dt></span><span class="sxs-lookup"><span data-stu-id="4ea37-124"><dt>**VM\_E\_USB\_DETACH\_FAILED**</dt> <dt>0xA00400927</dt></span></span> </dl> | <span data-ttu-id="4ea37-125">L’opération de détachement a échoué.</span><span class="sxs-lookup"><span data-stu-id="4ea37-125">The detach operation failed.</span></span><br/>        |
| <dl> <span data-ttu-id="4ea37-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4ea37-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="4ea37-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4ea37-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="4ea37-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ea37-128">Requirements</span></span>



| <span data-ttu-id="4ea37-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ea37-129">Requirement</span></span> | <span data-ttu-id="4ea37-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ea37-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea37-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ea37-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4ea37-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ea37-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ea37-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ea37-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4ea37-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ea37-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4ea37-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4ea37-135">End of client support</span></span><br/>    | <span data-ttu-id="4ea37-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4ea37-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4ea37-137">Produit</span><span class="sxs-lookup"><span data-stu-id="4ea37-137">Product</span></span><br/>                  | <span data-ttu-id="4ea37-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4ea37-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4ea37-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ea37-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ea37-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ea37-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4ea37-141">IID</span><span class="sxs-lookup"><span data-stu-id="4ea37-141">IID</span></span><br/>                      | <span data-ttu-id="4ea37-142">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4ea37-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4ea37-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ea37-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea37-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="4ea37-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

