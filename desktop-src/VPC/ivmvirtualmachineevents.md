---
title: Interface IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Définit l’interface d’événements sortants pour l’interface IVMVirtualMachine.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Virtual PC de l’interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466610"
---
# <a name="ivmvirtualmachineevents-interface"></a><span data-ttu-id="218f5-105">Interface IVMVirtualMachineEvents</span><span class="sxs-lookup"><span data-stu-id="218f5-105">IVMVirtualMachineEvents interface</span></span>

<span data-ttu-id="218f5-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="218f5-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="218f5-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="218f5-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="218f5-108">Définit l’interface d’événements sortants pour l’interface [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="218f5-108">Defines the outgoing event interface for the [**IVMVirtualMachine**](ivmvirtualmachine.md) interface.</span></span> <span data-ttu-id="218f5-109">Le client implémente ces méthodes pour recevoir les événements envoyés par [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="218f5-109">The client implements these methods to receive events sent from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="members"></a><span data-ttu-id="218f5-110">Membres</span><span class="sxs-lookup"><span data-stu-id="218f5-110">Members</span></span>

<span data-ttu-id="218f5-111">L’interface **IVMVirtualMachineEvents** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="218f5-111">The **IVMVirtualMachineEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="218f5-112">**IVMVirtualMachineEvents** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="218f5-112">**IVMVirtualMachineEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="218f5-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="218f5-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="218f5-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="218f5-114">Methods</span></span>

<span data-ttu-id="218f5-115">L’interface **IVMVirtualMachineEvents** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="218f5-115">The **IVMVirtualMachineEvents** interface has these methods.</span></span>



| <span data-ttu-id="218f5-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="218f5-116">Method</span></span>                                                                                   | <span data-ttu-id="218f5-117">Description</span><span class="sxs-lookup"><span data-stu-id="218f5-117">Description</span></span>                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="218f5-118">**OnAdditionsAvailable**</span><span class="sxs-lookup"><span data-stu-id="218f5-118">**OnAdditionsAvailable**</span></span>](ivmvirtualmachineevents-onadditionsavailable.md)             | <span data-ttu-id="218f5-119">Reçoit une notification indiquant que les composants d’intégration sont disponibles sur une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="218f5-119">Receives notification that integration components are available in a virtual machine.</span></span><br/>                                                |
| [<span data-ttu-id="218f5-120">**OnAdditionsUninstalled**</span><span class="sxs-lookup"><span data-stu-id="218f5-120">**OnAdditionsUninstalled**</span></span>](ivmvirtualmachineevents-onadditionsuninstalled.md)         | <span data-ttu-id="218f5-121">Reçoit une notification indiquant que les composants d’intégration sont désinstallés sur une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="218f5-121">Receives notification that integration components are uninstalled in a virtual machine.</span></span><br/>                                              |
| [<span data-ttu-id="218f5-122">**OnConfigurationChanged**</span><span class="sxs-lookup"><span data-stu-id="218f5-122">**OnConfigurationChanged**</span></span>](ivmvirtualmachineevents-onconfigurationchanged.md)         | <span data-ttu-id="218f5-123">Reçoit une notification indiquant qu’une valeur de la configuration de cet ordinateur virtuel a changé.</span><span class="sxs-lookup"><span data-stu-id="218f5-123">Receives notification that a value in the configuration for this virtual machine has changed.</span></span><br/>                                        |
| [<span data-ttu-id="218f5-124">**OnDiskOutOfSpace**</span><span class="sxs-lookup"><span data-stu-id="218f5-124">**OnDiskOutOfSpace**</span></span>](ivmvirtualmachineevents-ondiskoutofspace.md)                     | <span data-ttu-id="218f5-125">Reçoit une notification indiquant qu’un disque requis pour un ordinateur virtuel n’a plus d’espace et que l’ordinateur virtuel ne peut pas s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="218f5-125">Receives notification that a disk required for a virtual machine is out of space and the virtual machine is unable to run.</span></span><br/>           |
| [<span data-ttu-id="218f5-126">**OnEnhancedVideoModeChanged**</span><span class="sxs-lookup"><span data-stu-id="218f5-126">**OnEnhancedVideoModeChanged**</span></span>](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | <span data-ttu-id="218f5-127">Reçoit une notification indiquant que la prise en charge d’un ordinateur virtuel pour le mode vidéo amélioré a changé.</span><span class="sxs-lookup"><span data-stu-id="218f5-127">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span><br/>                                          |
| [<span data-ttu-id="218f5-128">**OnGuestLogoff**</span><span class="sxs-lookup"><span data-stu-id="218f5-128">**OnGuestLogoff**</span></span>](ivmvirtualmachineevents-onguestlogoff.md)                           | <span data-ttu-id="218f5-129">Reçoit une notification indiquant qu’un utilisateur s’est déconnecté du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="218f5-129">Receives notification that a user has logged off from the guest operating system.</span></span><br/>                                                    |
| [<span data-ttu-id="218f5-130">**OnGuestShutdown**</span><span class="sxs-lookup"><span data-stu-id="218f5-130">**OnGuestShutdown**</span></span>](ivmvirtualmachineevents-onguestshutdown.md)                       | <span data-ttu-id="218f5-131">Reçoit une notification indiquant que le système d’exploitation invité s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="218f5-131">Receives notification that guest operating system has shut down.</span></span><br/>                                                                     |
| [<span data-ttu-id="218f5-132">**OnHeartbeatStopped**</span><span class="sxs-lookup"><span data-stu-id="218f5-132">**OnHeartbeatStopped**</span></span>](ivmvirtualmachineevents-onheartbeatstopped.md)                 | <span data-ttu-id="218f5-133">Reçoit une notification indiquant que la pulsation d’une machine virtuelle s’est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="218f5-133">Receives notification that a virtual machine's heartbeat has stopped.</span></span> <span data-ttu-id="218f5-134">Cela indique généralement que le système d’exploitation invité s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="218f5-134">This usually indicates the guest operating system has crashed.</span></span><br/> |
| [<span data-ttu-id="218f5-135">**OnRequestShutdown**</span><span class="sxs-lookup"><span data-stu-id="218f5-135">**OnRequestShutdown**</span></span>](ivmvirtualmachineevents-onrequestshutdown.md)                   | <span data-ttu-id="218f5-136">Reçoit une notification indiquant qu’une demande d’arrêt a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="218f5-136">Receives notification that a shutdown request has been made.</span></span><br/>                                                                         |
| [<span data-ttu-id="218f5-137">**OnReset**</span><span class="sxs-lookup"><span data-stu-id="218f5-137">**OnReset**</span></span>](ivmvirtualmachineevents-onreset.md)                                       | <span data-ttu-id="218f5-138">Reçoit une notification indiquant qu’un ordinateur virtuel a été réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="218f5-138">Receives notification that a virtual machine has been reset.</span></span><br/>                                                                         |
| [<span data-ttu-id="218f5-139">**OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="218f5-139">**OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)                           | <span data-ttu-id="218f5-140">Reçoit une notification indiquant que l’état d’une machine virtuelle a changé.</span><span class="sxs-lookup"><span data-stu-id="218f5-140">Receives notification that a virtual machine's state has changed.</span></span><br/>                                                                    |
| [<span data-ttu-id="218f5-141">**OnTripleFault**</span><span class="sxs-lookup"><span data-stu-id="218f5-141">**OnTripleFault**</span></span>](ivmvirtualmachineevents-ontriplefault.md)                           | <span data-ttu-id="218f5-142">Reçoit une notification indiquant qu’un ordinateur virtuel a une erreur triple.</span><span class="sxs-lookup"><span data-stu-id="218f5-142">Receives notification that a virtual machine has triple-faulted.</span></span><br/>                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="218f5-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="218f5-143">Requirements</span></span>



| <span data-ttu-id="218f5-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="218f5-144">Requirement</span></span> | <span data-ttu-id="218f5-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="218f5-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="218f5-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="218f5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="218f5-147">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="218f5-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="218f5-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="218f5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="218f5-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="218f5-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="218f5-150">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="218f5-150">End of client support</span></span><br/>    | <span data-ttu-id="218f5-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="218f5-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="218f5-152">Produit</span><span class="sxs-lookup"><span data-stu-id="218f5-152">Product</span></span><br/>                  | <span data-ttu-id="218f5-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="218f5-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="218f5-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="218f5-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="218f5-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="218f5-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="218f5-156">IID</span><span class="sxs-lookup"><span data-stu-id="218f5-156">IID</span></span><br/>                      | <span data-ttu-id="218f5-157">DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="218f5-157">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



 

