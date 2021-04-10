---
title: Méthode IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces. h)
description: Attache un périphérique USB à une machine virtuelle.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Méthode AttachUSBDevice Virtual PC
- Méthode AttachUSBDevice Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode AttachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032990"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a><span data-ttu-id="673fd-106">IVMVirtualMachine :: AttachUSBDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="673fd-106">IVMVirtualMachine::AttachUSBDevice method</span></span>

<span data-ttu-id="673fd-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="673fd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="673fd-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="673fd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="673fd-109">Attache un périphérique USB à une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="673fd-109">Attaches a USB device to a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="673fd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="673fd-110">Syntax</span></span>


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="673fd-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="673fd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="673fd-112">*inUSBDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="673fd-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="673fd-113">Pointeur [**IVMUSBDevice**](ivmusbdevice.md) qui représente le périphérique USB connecté à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="673fd-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device connected to the host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="673fd-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="673fd-114">Return value</span></span>

<span data-ttu-id="673fd-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="673fd-115">This method can return one of these values.</span></span>



| <span data-ttu-id="673fd-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="673fd-116">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="673fd-117">Description</span><span class="sxs-lookup"><span data-stu-id="673fd-117">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="673fd-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="673fd-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="673fd-119">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="673fd-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="673fd-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="673fd-121">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="673fd-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                        | <span data-ttu-id="673fd-123">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="673fd-123">The VM is not running.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="673fd-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="673fd-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                             | <span data-ttu-id="673fd-125">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="673fd-125">The configuration is unknown.</span></span><br/>                                           |
| <dl> <span data-ttu-id="673fd-126"><dt>**Ordinateur virtuel \_ \_Ajouts \_ non \_**</dt> réalisés <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-126"><dt>**VM\_E\_ADDITIONS\_NOT\_AVAIL**</dt> <dt>0xA0040504</dt></span></span> </dl>                   | <span data-ttu-id="673fd-127">Les composants d’intégration ne sont pas disponibles dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="673fd-127">Integration Components are not available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="673fd-128"><dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>          | <span data-ttu-id="673fd-129">La fonctionnalité USB n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="673fd-129">The USB feature is not available.</span></span><br/>                                       |
| <dl> <span data-ttu-id="673fd-130"><dt>**Ordinateur virtuel \_ \_Erreur de \_ \_ pilote de \_ connecteur USB E**</dt> <dt>0xA00400925</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-130"><dt>**VM\_E\_USB\_CONNECTOR\_DRIVER\_ERROR**</dt> <dt>0xA00400925</dt></span></span> </dl>          | <span data-ttu-id="673fd-131">Une erreur de pilote de connecteur USB s’est produite.</span><span class="sxs-lookup"><span data-stu-id="673fd-131">There was a USB Connector driver error.</span></span><br/>                                 |
| <dl> <span data-ttu-id="673fd-132"><dt>**Ordinateur virtuel \_ Échec de l' \_ attachement USB E- \_ \_ \_ \_ périphériques supplémentaires**</dt> <dt>0xA00400931</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-132"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_MORE\_DEVICES**</dt> <dt>0xA00400931</dt></span></span> </dl>     | <span data-ttu-id="673fd-133">Impossible d’attacher d’autres appareils à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="673fd-133">Cannot attach more devices to the VM.</span></span><br/>                                   |
| <dl> <span data-ttu-id="673fd-134"><dt>**Ordinateur virtuel \_ Échec de l' \_ \_ \_ \_ \_ erreur de stratégie**</dt> de <dt>0xA00400932</dt> d’attachement USB</span><span class="sxs-lookup"><span data-stu-id="673fd-134"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_GP\_ERROR**</dt> <dt>0xA00400932</dt></span></span> </dl>         | <span data-ttu-id="673fd-135">Un paramètre de stratégie de groupe empêche la redirection USB.</span><span class="sxs-lookup"><span data-stu-id="673fd-135">A group policy setting is preventing the USB redirection.</span></span><br/>               |
| <dl> <span data-ttu-id="673fd-136"><dt>**Ordinateur virtuel \_ Échec de l' \_ attachement USB E 0xA00400933 \_ \_ \_ déjà \_ affecté**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="673fd-136"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_ALREADY\_ASSIGNED**</dt> <dt>0xA00400933</dt></span></span> </dl> | <span data-ttu-id="673fd-137">Un périphérique USB a déjà été attaché par un autre client.</span><span class="sxs-lookup"><span data-stu-id="673fd-137">A USB device has already been attached by some other client.</span></span><br/>            |
| <dl> <span data-ttu-id="673fd-138"><dt>**Ordinateur virtuel \_ Échec de l' \_ \_ attachement \_ USB E**</dt> <dt>0xA00400926</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-138"><dt>**VM\_E\_USB\_ATTACH\_FAILED**</dt> <dt>0xA00400926</dt></span></span> </dl>                    | <span data-ttu-id="673fd-139">Échec de l’opération d’attachement.</span><span class="sxs-lookup"><span data-stu-id="673fd-139">The attach operation failed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="673fd-140"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-140"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="673fd-141">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="673fd-141">An unexpected error has occurred.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="673fd-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="673fd-142">Requirements</span></span>



| <span data-ttu-id="673fd-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="673fd-143">Requirement</span></span> | <span data-ttu-id="673fd-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="673fd-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="673fd-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="673fd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="673fd-146">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="673fd-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="673fd-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="673fd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="673fd-148">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="673fd-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="673fd-149">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="673fd-149">End of client support</span></span><br/>    | <span data-ttu-id="673fd-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="673fd-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="673fd-151">Produit</span><span class="sxs-lookup"><span data-stu-id="673fd-151">Product</span></span><br/>                  | <span data-ttu-id="673fd-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="673fd-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="673fd-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="673fd-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="673fd-154"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="673fd-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="673fd-155">IID</span><span class="sxs-lookup"><span data-stu-id="673fd-155">IID</span></span><br/>                      | <span data-ttu-id="673fd-156">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="673fd-156">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="673fd-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="673fd-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673fd-158">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="673fd-158">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

