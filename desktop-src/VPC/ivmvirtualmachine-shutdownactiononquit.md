---
title: IVMVirtualMachine ShutdownActionOnQuit, propriété (VPCCOMInterfaces. h)
description: Action à exécuter sur cet ordinateur virtuel s’il est en cours d’exécution lorsque Windows Virtual PC est fermé.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- ShutdownActionOnQuit propriété Virtual PC
- ShutdownActionOnQuit, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété ShutdownActionOnQuit
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466383"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a><span data-ttu-id="c7506-106">IVMVirtualMachine :: ShutdownActionOnQuit, propriété</span><span class="sxs-lookup"><span data-stu-id="c7506-106">IVMVirtualMachine::ShutdownActionOnQuit property</span></span>

<span data-ttu-id="c7506-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c7506-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c7506-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c7506-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c7506-109">Récupère et définit l’action à effectuer sur cet ordinateur virtuel (VM) s’il est en cours d’exécution lorsque Windows Virtual PC est fermé.</span><span class="sxs-lookup"><span data-stu-id="c7506-109">Retrieves and sets the action to be performed on this virtual machine (VM) if it is running when Windows Virtual PC is quit.</span></span>

<span data-ttu-id="c7506-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c7506-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7506-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7506-111">Syntax</span></span>


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a><span data-ttu-id="c7506-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c7506-112">Property value</span></span>

<span data-ttu-id="c7506-113">Indique comment arrêter cette machine virtuelle si elle est en cours d’exécution au moment de la fermeture de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="c7506-113">Specifies how to shut down this VM if it is running when Windows Virtual PC is quit.</span></span> <span data-ttu-id="c7506-114">Pour obtenir la liste des valeurs, consultez [**VMShutdownAction**](vmshutdownaction.md).</span><span class="sxs-lookup"><span data-stu-id="c7506-114">For a list of values, see [**VMShutdownAction**](vmshutdownaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="c7506-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c7506-115">Error codes</span></span>



| <span data-ttu-id="c7506-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="c7506-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c7506-117">Signification</span><span class="sxs-lookup"><span data-stu-id="c7506-117">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7506-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c7506-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c7506-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c7506-119">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="c7506-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c7506-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c7506-121">Le paramètre est **null** ou n’est pas une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="c7506-121">The parameter is **NULL** or not a valid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="c7506-122"><dt>E \_ ACCESSDENIED</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="c7506-122"><dt>E\_ACCESSDENIED</dt> <dt>0x80070005</dt></span></span> </dl>    | <span data-ttu-id="c7506-123">L’utilisateur actuel ne dispose pas d’un accès suffisant au fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="c7506-123">The current user has insufficient access to the configuration file.</span></span><br/> |
| <dl> <span data-ttu-id="c7506-124"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="c7506-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c7506-125">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="c7506-125">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="c7506-126"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c7506-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c7506-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c7506-127">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="remarks"></a><span data-ttu-id="c7506-128">Notes</span><span class="sxs-lookup"><span data-stu-id="c7506-128">Remarks</span></span>

<span data-ttu-id="c7506-129">Par défaut, les machines virtuelles en cours d’exécution sont enregistrées lorsque Windows Virtual PC est fermé.</span><span class="sxs-lookup"><span data-stu-id="c7506-129">By default, running VMs are saved when Windows Virtual PC is quit.</span></span> <span data-ttu-id="c7506-130">L’action d’arrêt **vmShutdownAction \_ Save** (0) enregistre l’état de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c7506-130">The shutdown action **vmShutdownAction\_Save** (0) will save the VM's state.</span></span> <span data-ttu-id="c7506-131">L’action **vmShutdownAction \_ turnoff** (1) désactive la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c7506-131">The **vmShutdownAction\_TurnOff** (1) action will turn off the VM.</span></span> <span data-ttu-id="c7506-132">L’action d' **\_ arrêt vmShutdownAction** (2) arrêtera le système d’exploitation invité si les composants d’intégration sont disponibles et ENREGISTRERA la machine virtuelle dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c7506-132">The **vmShutdownAction\_Shutdown** (2) action will shut down the guest operating system if the integration components are available and will save the VM otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7506-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7506-133">Requirements</span></span>



| <span data-ttu-id="c7506-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7506-134">Requirement</span></span> | <span data-ttu-id="c7506-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7506-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7506-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7506-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c7506-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7506-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7506-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7506-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c7506-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7506-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c7506-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c7506-140">End of client support</span></span><br/>    | <span data-ttu-id="c7506-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c7506-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c7506-142">Produit</span><span class="sxs-lookup"><span data-stu-id="c7506-142">Product</span></span><br/>                  | <span data-ttu-id="c7506-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c7506-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c7506-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7506-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7506-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7506-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c7506-146">IID</span><span class="sxs-lookup"><span data-stu-id="c7506-146">IID</span></span><br/>                      | <span data-ttu-id="c7506-147">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c7506-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c7506-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7506-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7506-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="c7506-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="c7506-150">**VMShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="c7506-150">**VMShutdownAction**</span></span>](vmshutdownaction.md)
</dt> </dl>

 

