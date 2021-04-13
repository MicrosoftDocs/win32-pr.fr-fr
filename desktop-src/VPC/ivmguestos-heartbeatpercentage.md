---
title: IVMGuestOS HeartbeatPercentage, propriété (VPCCOMInterfaces. h)
description: Pourcentage de pulsations attendues reçues au cours de la dernière minute.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- HeartbeatPercentage propriété Virtual PC
- HeartbeatPercentage, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété HeartbeatPercentage
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509257"
---
# <a name="ivmguestosheartbeatpercentage-property"></a><span data-ttu-id="5121b-106">IVMGuestOS :: HeartbeatPercentage, propriété</span><span class="sxs-lookup"><span data-stu-id="5121b-106">IVMGuestOS::HeartbeatPercentage property</span></span>

<span data-ttu-id="5121b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5121b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5121b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5121b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5121b-109">Récupère le pourcentage de pulsations attendues reçues au cours de la dernière minute.</span><span class="sxs-lookup"><span data-stu-id="5121b-109">Retrieves the percentage of expected heartbeats received over the past minute.</span></span>

<span data-ttu-id="5121b-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5121b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5121b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5121b-111">Syntax</span></span>


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a><span data-ttu-id="5121b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5121b-112">Property value</span></span>

<span data-ttu-id="5121b-113">Pourcentage de pulsations attendues reçues au cours de la dernière minute.</span><span class="sxs-lookup"><span data-stu-id="5121b-113">The percentage of expected heartbeats received over the past minute.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5121b-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5121b-114">Error codes</span></span>



| <span data-ttu-id="5121b-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="5121b-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="5121b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="5121b-116">Meaning</span></span>                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5121b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5121b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="5121b-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="5121b-118">The operation was successful.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="5121b-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5121b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="5121b-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5121b-120">The parameter is **NULL**.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="5121b-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="5121b-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="5121b-122">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="5121b-122">The configuration is unknown.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="5121b-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="5121b-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="5121b-124">L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="5121b-124">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="5121b-125"><dt>Ordinateur virtuel \_ \_Ajouts \_ non \_ </dt> réalisés <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="5121b-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="5121b-126">La machine virtuelle n’est pas entièrement démarrée, la fonctionnalité composants d’intégration n’est pas installée ou la version installée ne prend pas en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="5121b-126">The VM is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="5121b-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5121b-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="5121b-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5121b-128">An unexpected error has occurred.</span></span><br/>                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="5121b-129">Notes</span><span class="sxs-lookup"><span data-stu-id="5121b-129">Remarks</span></span>

<span data-ttu-id="5121b-130">Les composants d’intégration enverront une pulsation périodique à Windows Virtual PC pendant que le système d’exploitation invité est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5121b-130">Integration components will send a periodic heartbeat to Windows Virtual PC while the guest operating system is running.</span></span> <span data-ttu-id="5121b-131">Si le système d’exploitation invité est lourdement chargé, il est possible que Windows Virtual PC reçoive moins de pulsations que prévu.</span><span class="sxs-lookup"><span data-stu-id="5121b-131">If the guest operating system is heavily loaded, it's possible that Windows Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="5121b-132">Si le pourcentage de pulsations chute à zéro, il est possible que le système d’exploitation invité ne réponde pas ou soit bloqué.</span><span class="sxs-lookup"><span data-stu-id="5121b-132">If the heartbeat percentage drops to zero, it is possible that the guest operating system is not responding or is crashed.</span></span> <span data-ttu-id="5121b-133">L’ordinateur virtuel doit être en cours d’exécution (c’est-à-dire être entièrement amorcé et ne pas s’arrêter) et des composants d’intégration doivent être installés lorsque cette propriété est appelée.</span><span class="sxs-lookup"><span data-stu-id="5121b-133">The virtual machine must be running (that is, fully booted and not shutting down) and integration components must be installed when this property is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="5121b-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5121b-134">Requirements</span></span>



| <span data-ttu-id="5121b-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5121b-135">Requirement</span></span> | <span data-ttu-id="5121b-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5121b-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5121b-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5121b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5121b-138">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5121b-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5121b-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5121b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5121b-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5121b-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5121b-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5121b-141">End of client support</span></span><br/>    | <span data-ttu-id="5121b-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5121b-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5121b-143">Produit</span><span class="sxs-lookup"><span data-stu-id="5121b-143">Product</span></span><br/>                  | <span data-ttu-id="5121b-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5121b-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5121b-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="5121b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="5121b-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5121b-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5121b-147">IID</span><span class="sxs-lookup"><span data-stu-id="5121b-147">IID</span></span><br/>                      | <span data-ttu-id="5121b-148">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="5121b-148">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5121b-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5121b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5121b-150">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="5121b-150">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

