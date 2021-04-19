---
title: IVMGuestOS IsHeartbeating, propriété (VPCCOMInterfaces. h)
description: Détermine si l’ordinateur virtuel a une pulsation.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- IsHeartbeating propriété Virtual PC
- IsHeartbeating, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété IsHeartbeating
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510576"
---
# <a name="ivmguestosisheartbeating-property"></a><span data-ttu-id="07d97-106">IVMGuestOS :: IsHeartbeating, propriété</span><span class="sxs-lookup"><span data-stu-id="07d97-106">IVMGuestOS::IsHeartbeating property</span></span>

<span data-ttu-id="07d97-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="07d97-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="07d97-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="07d97-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="07d97-109">Détermine si l’ordinateur virtuel a une pulsation.</span><span class="sxs-lookup"><span data-stu-id="07d97-109">Determines whether the virtual machine has a heartbeat.</span></span>

<span data-ttu-id="07d97-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="07d97-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d97-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07d97-111">Syntax</span></span>


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a><span data-ttu-id="07d97-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="07d97-112">Property value</span></span>

<span data-ttu-id="07d97-113">**Variante \_ TRUE** si une pulsation est détectée **, \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="07d97-113">**VARIANT\_TRUE** if a heartbeat is detected, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07d97-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="07d97-114">Error codes</span></span>



| <span data-ttu-id="07d97-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="07d97-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="07d97-116">Signification</span><span class="sxs-lookup"><span data-stu-id="07d97-116">Meaning</span></span>                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07d97-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="07d97-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="07d97-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="07d97-118">The operation was successful.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="07d97-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="07d97-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="07d97-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="07d97-120">The parameter is **NULL**.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="07d97-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="07d97-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="07d97-122">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="07d97-122">The configuration is unknown.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="07d97-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="07d97-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="07d97-124">L’ordinateur virtuel doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="07d97-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="07d97-125"><dt>Ordinateur virtuel \_ \_Ajouts \_ non \_ </dt> réalisés <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="07d97-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="07d97-126">L’ordinateur virtuel n’est pas entièrement démarré, la fonctionnalité composants d’intégration n’est pas installée ou la version installée ne prend pas en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="07d97-126">The virtual machine is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="07d97-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="07d97-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="07d97-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07d97-128">An unexpected error has occurred.</span></span><br/>                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="07d97-129">Notes</span><span class="sxs-lookup"><span data-stu-id="07d97-129">Remarks</span></span>

<span data-ttu-id="07d97-130">Lorsque les composants d’intégration sont installés dans le système d’exploitation invité, un « battement » ou une pulsation standard est envoyé de la session de l’ordinateur virtuel vers Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="07d97-130">When integration components is installed in the guest operating system, a regular 'tick' or heartbeat is sent from the virtual machine session to Windows Virtual PC.</span></span> <span data-ttu-id="07d97-131">Si le système d’exploitation invité est lourdement chargé, il est possible que Virtual PC reçoive moins de pulsations que prévu.</span><span class="sxs-lookup"><span data-stu-id="07d97-131">If the guest operating system is heavily loaded, it's possible that Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="07d97-132">Si aucune pulsation n’est détectée, il est possible que le système d’exploitation invité ne réponde pas ou soit bloqué.</span><span class="sxs-lookup"><span data-stu-id="07d97-132">If no heartbeat is detected, it is possible that the guest operating system is not responding or is crashed.</span></span>

<span data-ttu-id="07d97-133">Par défaut, un ordinateur virtuel produit dix cycles de pulsations par minute.</span><span class="sxs-lookup"><span data-stu-id="07d97-133">By default, a virtual machine produces ten heartbeat ticks per minute.</span></span> <span data-ttu-id="07d97-134">Si aucune pulsation n’est détectée pendant une minute entière, Windows Virtual PC tente de redémarrer la session de l’ordinateur virtuel une fois toutes les dix secondes pendant une durée de deux minutes maximum.</span><span class="sxs-lookup"><span data-stu-id="07d97-134">If no heartbeat ticks are detected for an entire minute, Windows Virtual PC will attempt to restart the virtual machine session once every ten seconds for up to two minutes.</span></span> <span data-ttu-id="07d97-135">Ce comportement est contrôlé par les valeurs de clé suivantes dans le fichier de configuration de la session d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="07d97-135">This behavior is controlled by the following key values in the virtual machine session's configuration file.</span></span>



| <span data-ttu-id="07d97-136">Clé de configuration</span><span class="sxs-lookup"><span data-stu-id="07d97-136">Configuration key</span></span>                                            | <span data-ttu-id="07d97-137">Default</span><span class="sxs-lookup"><span data-stu-id="07d97-137">Default</span></span>       | <span data-ttu-id="07d97-138">Description</span><span class="sxs-lookup"><span data-stu-id="07d97-138">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d97-139">intégration/Microsoft/pulsation/heure</span><span class="sxs-lookup"><span data-stu-id="07d97-139">integration/microsoft/heartbeat/time</span></span><br/>              | <span data-ttu-id="07d97-140">60</span><span class="sxs-lookup"><span data-stu-id="07d97-140">60</span></span><br/> | <span data-ttu-id="07d97-141">Longueur du bloc de temps utilisé pour générer des graduations de pulsations, en secondes.</span><span class="sxs-lookup"><span data-stu-id="07d97-141">The length of the block of time used to generate heartbeat ticks, in in seconds.</span></span><br/>                                             |
| <span data-ttu-id="07d97-142">intégration/Microsoft/pulsation/taux</span><span class="sxs-lookup"><span data-stu-id="07d97-142">integration/microsoft/heartbeat/rate</span></span><br/>              | <span data-ttu-id="07d97-143">10</span><span class="sxs-lookup"><span data-stu-id="07d97-143">10</span></span><br/> | <span data-ttu-id="07d97-144">Nombre de graduations générées dans chaque bloc de temps de pulsation.</span><span class="sxs-lookup"><span data-stu-id="07d97-144">The number of ticks generated in each heartbeat time block.</span></span><br/>                                                                  |
| <span data-ttu-id="07d97-145">intégration/Microsoft/pulsation/intervalle de défaillance \_</span><span class="sxs-lookup"><span data-stu-id="07d97-145">integration/microsoft/heartbeat/failure\_interval</span></span><br/> | <span data-ttu-id="07d97-146">10</span><span class="sxs-lookup"><span data-stu-id="07d97-146">10</span></span><br/> | <span data-ttu-id="07d97-147">Nombre de secondes entre les tentatives de redémarrage, une fois qu’aucun cycle de pulsation n’est reçu dans un bloc de temps de pulsation spécifique.</span><span class="sxs-lookup"><span data-stu-id="07d97-147">The number of seconds between restart attempts, once no heartbeat ticks are received within a specific heartbeat time block.</span></span><br/> |
| <span data-ttu-id="07d97-148">intégration/Microsoft/pulsations/échecs de \_ tentative</span><span class="sxs-lookup"><span data-stu-id="07d97-148">integration/microsoft/heartbeat/failure\_attempts</span></span><br/> | <span data-ttu-id="07d97-149">12</span><span class="sxs-lookup"><span data-stu-id="07d97-149">12</span></span><br/> | <span data-ttu-id="07d97-150">Nombre de tentatives de redémarrage effectuées.</span><span class="sxs-lookup"><span data-stu-id="07d97-150">The number of restart attempts made.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="07d97-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07d97-151">Requirements</span></span>



| <span data-ttu-id="07d97-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07d97-152">Requirement</span></span> | <span data-ttu-id="07d97-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="07d97-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d97-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07d97-154">Minimum supported client</span></span><br/> | <span data-ttu-id="07d97-155">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07d97-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07d97-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07d97-156">Minimum supported server</span></span><br/> | <span data-ttu-id="07d97-157">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="07d97-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="07d97-158">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="07d97-158">End of client support</span></span><br/>    | <span data-ttu-id="07d97-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07d97-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="07d97-160">Produit</span><span class="sxs-lookup"><span data-stu-id="07d97-160">Product</span></span><br/>                  | <span data-ttu-id="07d97-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="07d97-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="07d97-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="07d97-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="07d97-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d97-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="07d97-164">IID</span><span class="sxs-lookup"><span data-stu-id="07d97-164">IID</span></span><br/>                      | <span data-ttu-id="07d97-165">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="07d97-165">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="07d97-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07d97-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d97-167">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="07d97-167">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

