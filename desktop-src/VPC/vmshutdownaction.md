---
title: Énumération VMShutdownAction (VPCCOMInterfaces. h)
description: Indique comment arrêter un ordinateur virtuel lorsque l’ordinateur hôte s’arrête ou que le processus de vpc.exe se termine.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- Virtual PC de l’énumération VMShutdownAction
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536908"
---
# <a name="vmshutdownaction-enumeration"></a><span data-ttu-id="cab6e-104">Énumération VMShutdownAction</span><span class="sxs-lookup"><span data-stu-id="cab6e-104">VMShutdownAction enumeration</span></span>

<span data-ttu-id="cab6e-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cab6e-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cab6e-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cab6e-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cab6e-107">Indique comment arrêter un ordinateur virtuel (VM) lorsque l’ordinateur hôte s’arrête ou que le processus de vpc.exe se termine.</span><span class="sxs-lookup"><span data-stu-id="cab6e-107">Specifies how to shut down a virtual machine (VM) when the host shuts down or the vpc.exe process exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="cab6e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cab6e-108">Syntax</span></span>


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a><span data-ttu-id="cab6e-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="cab6e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cab6e-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction \_ Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="cab6e-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction\_Save**</span></span>
</dt> <dd>

<span data-ttu-id="cab6e-111">Enregistrez l’état de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="cab6e-111">Save the VM state.</span></span>

</dd> <dt>

<span data-ttu-id="cab6e-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction \_ turnoff**</span><span class="sxs-lookup"><span data-stu-id="cab6e-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction\_TurnOff**</span></span>
</dt> <dd>

<span data-ttu-id="cab6e-113">Désactivez la machine virtuelle sans annuler les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="cab6e-113">Turn off the VM without undoing the drives.</span></span>

</dd> <dt>

<span data-ttu-id="cab6e-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**arrêt de vmShutdownAction \_**</span><span class="sxs-lookup"><span data-stu-id="cab6e-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction\_Shutdown**</span></span>
</dt> <dd>

<span data-ttu-id="cab6e-115">Arrêtez le système d’exploitation invité sur la machine virtuelle sans annuler les lecteurs si les composants d’intégration sont disponibles et enregistrera la machine virtuelle dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cab6e-115">Shut down the guest operating system on the VM without undoing the drives if the integration components are available and will save the VM otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cab6e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cab6e-116">Requirements</span></span>



| <span data-ttu-id="cab6e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cab6e-117">Requirement</span></span> | <span data-ttu-id="cab6e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cab6e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cab6e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cab6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cab6e-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cab6e-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cab6e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cab6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cab6e-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cab6e-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cab6e-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="cab6e-123">End of client support</span></span><br/>    | <span data-ttu-id="cab6e-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cab6e-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cab6e-125">Produit</span><span class="sxs-lookup"><span data-stu-id="cab6e-125">Product</span></span><br/>                  | <span data-ttu-id="cab6e-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cab6e-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cab6e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="cab6e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cab6e-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cab6e-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab6e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cab6e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab6e-130">Énumérations de PC virtuels Windows</span><span class="sxs-lookup"><span data-stu-id="cab6e-130">Windows Virtual PC Enumerations</span></span>](virtual-pc-enumerations.md)
</dt> <dt>

[<span data-ttu-id="cab6e-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="cab6e-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

