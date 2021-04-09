---
title: Énumération VMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Spécifie les événements de machine virtuelle.
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- Virtual PC de l’énumération VMVirtualMachineEvents
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1e1d8f4d89c28f63886444537fb9d894fc42e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033158"
---
# <a name="vmvirtualmachineevents-enumeration"></a><span data-ttu-id="64b7c-104">Énumération VMVirtualMachineEvents</span><span class="sxs-lookup"><span data-stu-id="64b7c-104">VMVirtualMachineEvents enumeration</span></span>

<span data-ttu-id="64b7c-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="64b7c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="64b7c-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="64b7c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="64b7c-107">Spécifie les événements d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="64b7c-107">Specifies the virtual machine (VM) events.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b7c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64b7c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a><span data-ttu-id="64b7c-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="64b7c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="64b7c-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent \_ StateChanged**</span><span class="sxs-lookup"><span data-stu-id="64b7c-110"><span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent\_StateChanged**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-111">L’état d’une machine virtuelle a changé.</span><span class="sxs-lookup"><span data-stu-id="64b7c-111">A VM's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ RequestShutdown**</span><span class="sxs-lookup"><span data-stu-id="64b7c-112"><span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_RequestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-113">Un arrêt a été demandé.</span><span class="sxs-lookup"><span data-stu-id="64b7c-113">A shutdown has been requested.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**\_réinitialisation vmVirtualMachineEvent**</span><span class="sxs-lookup"><span data-stu-id="64b7c-114"><span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmVirtualMachineEvent\_Reset**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-115">Une machine virtuelle a été réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="64b7c-115">A VM has been reset.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent \_ TripleFault**</span><span class="sxs-lookup"><span data-stu-id="64b7c-116"><span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent\_TripleFault**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-117">Une machine virtuelle a une erreur triple.</span><span class="sxs-lookup"><span data-stu-id="64b7c-117">A VM has triple-faulted.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent \_ HeartbeatStopped**</span><span class="sxs-lookup"><span data-stu-id="64b7c-118"><span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent\_HeartbeatStopped**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-119">La pulsation d’une machine virtuelle s’est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="64b7c-119">A VM's heartbeat has stopped.</span></span> <span data-ttu-id="64b7c-120">Cela indique généralement que le système d’exploitation invité s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="64b7c-120">This usually indicates that the guest operating system has crashed.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent \_ ConfigurationChanged**</span><span class="sxs-lookup"><span data-stu-id="64b7c-121"><span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent\_ConfigurationChanged**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-122">Une valeur de la configuration pour cette machine virtuelle a changé</span><span class="sxs-lookup"><span data-stu-id="64b7c-122">A value in the configuration for this VM has changed</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent \_ EnhancedVideoModeChanged**</span><span class="sxs-lookup"><span data-stu-id="64b7c-123"><span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent\_EnhancedVideoModeChanged**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-124">Le mode vidéo d’une machine virtuelle a changé.</span><span class="sxs-lookup"><span data-stu-id="64b7c-124">A VM's video mode has changed.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent \_ AdditionsUninstalled**</span><span class="sxs-lookup"><span data-stu-id="64b7c-125"><span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent\_AdditionsUninstalled**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-126">Les composants d’intégration ont été désinstallés de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="64b7c-126">Integration components have been uninstalled from the VM.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent \_ AdditionsAvailable**</span><span class="sxs-lookup"><span data-stu-id="64b7c-127"><span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent\_AdditionsAvailable**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-128">L’intégration est disponible dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="64b7c-128">Integration are available in the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ GuestShutdown**</span><span class="sxs-lookup"><span data-stu-id="64b7c-129"><span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent\_GuestShutdown**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-130">Un système d’exploitation invité s’arrête.</span><span class="sxs-lookup"><span data-stu-id="64b7c-130">A guest operating system is shutting down.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent \_ GuestLogoff**</span><span class="sxs-lookup"><span data-stu-id="64b7c-131"><span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent\_GuestLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-132">Utilisateur déconnecté du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="64b7c-132">A user logged off from the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="64b7c-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent \_ DiskOutOfSpace**</span><span class="sxs-lookup"><span data-stu-id="64b7c-133"><span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent\_DiskOutOfSpace**</span></span>
</dt> <dd>

<span data-ttu-id="64b7c-134">Un disque requis par la machine virtuelle ne dispose pas de suffisamment d’espace.</span><span class="sxs-lookup"><span data-stu-id="64b7c-134">A disk required by the VM is low on space.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64b7c-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64b7c-135">Requirements</span></span>



| <span data-ttu-id="64b7c-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64b7c-136">Requirement</span></span> | <span data-ttu-id="64b7c-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="64b7c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b7c-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64b7c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="64b7c-139">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64b7c-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="64b7c-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64b7c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="64b7c-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="64b7c-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="64b7c-142">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="64b7c-142">End of client support</span></span><br/>    | <span data-ttu-id="64b7c-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="64b7c-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="64b7c-144">Produit</span><span class="sxs-lookup"><span data-stu-id="64b7c-144">Product</span></span><br/>                  | <span data-ttu-id="64b7c-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="64b7c-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="64b7c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="64b7c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="64b7c-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="64b7c-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b7c-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64b7c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b7c-149">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="64b7c-149">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

