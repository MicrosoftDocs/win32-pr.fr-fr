---
title: Interface IVMTask (VPCCOMInterfaces. h)
description: Utilisez l’interface IVMTask pour surveiller et contrôler les tâches asynchrones pour différentes méthodes COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Virtual PC de l’interface IVMTask
- IVMTask interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508978"
---
# <a name="ivmtask-interface"></a><span data-ttu-id="1cc28-105">Interface IVMTask</span><span class="sxs-lookup"><span data-stu-id="1cc28-105">IVMTask interface</span></span>

<span data-ttu-id="1cc28-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1cc28-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1cc28-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1cc28-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1cc28-108">Utilisez l’interface **IVMTask** pour surveiller et contrôler les tâches asynchrones pour différentes méthodes com.</span><span class="sxs-lookup"><span data-stu-id="1cc28-108">Use the **IVMTask** interface to monitor and control asynchronous tasks for various COM methods.</span></span>

## <a name="members"></a><span data-ttu-id="1cc28-109">Membres</span><span class="sxs-lookup"><span data-stu-id="1cc28-109">Members</span></span>

<span data-ttu-id="1cc28-110">L’interface **IVMTask** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="1cc28-110">The **IVMTask** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="1cc28-111">**IVMTask** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1cc28-111">**IVMTask** also has these types of members:</span></span>

-   [<span data-ttu-id="1cc28-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1cc28-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1cc28-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cc28-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1cc28-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1cc28-114">Methods</span></span>

<span data-ttu-id="1cc28-115">L’interface **IVMTask** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1cc28-115">The **IVMTask** interface has these methods.</span></span>



| <span data-ttu-id="1cc28-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="1cc28-116">Method</span></span>                                                 | <span data-ttu-id="1cc28-117">Description</span><span class="sxs-lookup"><span data-stu-id="1cc28-117">Description</span></span>                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1cc28-118">**Annuler**</span><span class="sxs-lookup"><span data-stu-id="1cc28-118">**Cancel**</span></span>](ivmtask-cancel.md)                       | <span data-ttu-id="1cc28-119">Annule la tâche.</span><span class="sxs-lookup"><span data-stu-id="1cc28-119">Cancels the task.</span></span><br/>                                                                |
| [<span data-ttu-id="1cc28-120">**WaitForCompletion**</span><span class="sxs-lookup"><span data-stu-id="1cc28-120">**WaitForCompletion**</span></span>](ivmtask-waitforcompletion.md) | <span data-ttu-id="1cc28-121">Attend que la tâche soit terminée ou que l’intervalle de délai d’attente spécifié soit écoulé.</span><span class="sxs-lookup"><span data-stu-id="1cc28-121">Waits for the task to complete or for the specified time-out interval to elapse.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1cc28-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cc28-122">Properties</span></span>

<span data-ttu-id="1cc28-123">L’interface **IVMTask** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1cc28-123">The **IVMTask** interface has these properties.</span></span>



| <span data-ttu-id="1cc28-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="1cc28-124">Property</span></span>                                                        | <span data-ttu-id="1cc28-125">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="1cc28-125">Access type</span></span>          | <span data-ttu-id="1cc28-126">Description</span><span class="sxs-lookup"><span data-stu-id="1cc28-126">Description</span></span>                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="1cc28-127">**Description**</span><span class="sxs-lookup"><span data-stu-id="1cc28-127">**Description**</span></span>](ivmtask-description.md)<br/>           | <span data-ttu-id="1cc28-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cc28-128">Read-only</span></span><br/> | <span data-ttu-id="1cc28-129">Une description de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1cc28-129">A description of the task.</span></span><br/>                              |
| [<span data-ttu-id="1cc28-130">**Error**</span><span class="sxs-lookup"><span data-stu-id="1cc28-130">**Error**</span></span>](ivmtask-error.md)<br/>                       | <span data-ttu-id="1cc28-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cc28-131">Read-only</span></span><br/> | <span data-ttu-id="1cc28-132">Erreur enregistrée pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="1cc28-132">The error recorded for this task.</span></span><br/>                       |
| [<span data-ttu-id="1cc28-133">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1cc28-133">**ErrorDescription**</span></span>](ivmtask-errordescription.md)<br/> | <span data-ttu-id="1cc28-134">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cc28-134">Read-only</span></span><br/> | <span data-ttu-id="1cc28-135">Description d’erreur localisée enregistrée pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="1cc28-135">The localized error description recorded for this task.</span></span><br/> |
| [<span data-ttu-id="1cc28-136">**IDENTIFI**</span><span class="sxs-lookup"><span data-stu-id="1cc28-136">**ID**</span></span>](ivmtask-id.md)<br/>                             | <span data-ttu-id="1cc28-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cc28-137">Read-only</span></span><br/> | <span data-ttu-id="1cc28-138">Identificateur unique pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="1cc28-138">A unique identifier for this task.</span></span><br/>                      |
| [<span data-ttu-id="1cc28-139">**IsCancelable**</span><span class="sxs-lookup"><span data-stu-id="1cc28-139">**IsCancelable**</span></span>](ivmtask-iscancelable.md)<br/>         | <span data-ttu-id="1cc28-140">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cc28-140">Read-only</span></span><br/> | <span data-ttu-id="1cc28-141">Indique si la tâche peut être annulée.</span><span class="sxs-lookup"><span data-stu-id="1cc28-141">Indicates whether the task can be canceled.</span></span><br/>             |
| [<span data-ttu-id="1cc28-142">**IsComplete**</span><span class="sxs-lookup"><span data-stu-id="1cc28-142">**IsComplete**</span></span>](ivmtask-iscomplete.md)<br/>             | <span data-ttu-id="1cc28-143">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cc28-143">Read-only</span></span><br/> | <span data-ttu-id="1cc28-144">Indique si la tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="1cc28-144">Indicates whether the task has completed.</span></span><br/>               |
| [<span data-ttu-id="1cc28-145">**PercentCompleted**</span><span class="sxs-lookup"><span data-stu-id="1cc28-145">**PercentCompleted**</span></span>](ivmtask-percentcompleted.md)<br/> | <span data-ttu-id="1cc28-146">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cc28-146">Read-only</span></span><br/> | <span data-ttu-id="1cc28-147">Pourcentage d’achèvement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1cc28-147">The completion percentage of the task.</span></span><br/>                  |
| [<span data-ttu-id="1cc28-148">**Venir**</span><span class="sxs-lookup"><span data-stu-id="1cc28-148">**Result**</span></span>](ivmtask-result.md)<br/>                     | <span data-ttu-id="1cc28-149">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cc28-149">Read-only</span></span><br/> | <span data-ttu-id="1cc28-150">Résultat de la tâche.</span><span class="sxs-lookup"><span data-stu-id="1cc28-150">The result of the task.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="1cc28-151">Notes</span><span class="sxs-lookup"><span data-stu-id="1cc28-151">Remarks</span></span>

<span data-ttu-id="1cc28-152">Un objet **IVMTask** est retourné par des méthodes qui peuvent éventuellement nécessiter un temps considérable.</span><span class="sxs-lookup"><span data-stu-id="1cc28-152">An **IVMTask** object is returned by methods that could potentially require a significant amount of time to complete.</span></span> <span data-ttu-id="1cc28-153">Cela permet à l’application de surveiller la progression de l’opération souhaitée sans la forcer à bloquer une exécution supplémentaire en attendant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1cc28-153">This allows the application to monitor the progress of the desired operation without forcing it to block further execution while waiting for the completion of the operation.</span></span>

<span data-ttu-id="1cc28-154">Les méthodes suivantes retournent un objet **IVMTask** qui peut être utilisé pour suivre la progression :</span><span class="sxs-lookup"><span data-stu-id="1cc28-154">The following methods return an **IVMTask** object that can be used to track progress:</span></span>

-   [<span data-ttu-id="1cc28-155">**IVMGuestOS :: Logoff**</span><span class="sxs-lookup"><span data-stu-id="1cc28-155">**IVMGuestOS::Logoff**</span></span>](ivmguestos-logoff.md)
-   [<span data-ttu-id="1cc28-156">**IVMGuestOS :: Restart**</span><span class="sxs-lookup"><span data-stu-id="1cc28-156">**IVMGuestOS::Restart**</span></span>](ivmguestos-restart.md)
-   [<span data-ttu-id="1cc28-157">**IVMGuestOS :: Shutdown**</span><span class="sxs-lookup"><span data-stu-id="1cc28-157">**IVMGuestOS::Shutdown**</span></span>](ivmguestos-shutdown.md)
-   [<span data-ttu-id="1cc28-158">**IVMHardDisk :: compact**</span><span class="sxs-lookup"><span data-stu-id="1cc28-158">**IVMHardDisk::Compact**</span></span>](ivmharddisk-compact.md)
-   [<span data-ttu-id="1cc28-159">**IVMHardDisk :: Convert**</span><span class="sxs-lookup"><span data-stu-id="1cc28-159">**IVMHardDisk::Convert**</span></span>](ivmharddisk-convert.md)
-   [<span data-ttu-id="1cc28-160">**IVMHardDisk :: Merge**</span><span class="sxs-lookup"><span data-stu-id="1cc28-160">**IVMHardDisk::Merge**</span></span>](ivmharddisk-merge.md)
-   [<span data-ttu-id="1cc28-161">**IVMHardDisk::MergeTo**</span><span class="sxs-lookup"><span data-stu-id="1cc28-161">**IVMHardDisk::MergeTo**</span></span>](ivmharddisk-mergeto.md)
-   [<span data-ttu-id="1cc28-162">**IVMVirtualMachine::MergeUndoDisks**</span><span class="sxs-lookup"><span data-stu-id="1cc28-162">**IVMVirtualMachine::MergeUndoDisks**</span></span>](ivmvirtualmachine-mergeundodisks.md)
-   [<span data-ttu-id="1cc28-163">**IVMVirtualMachine :: Reset**</span><span class="sxs-lookup"><span data-stu-id="1cc28-163">**IVMVirtualMachine::Reset**</span></span>](ivmvirtualmachine-reset.md)
-   [<span data-ttu-id="1cc28-164">**IVMVirtualMachine :: enregistrer**</span><span class="sxs-lookup"><span data-stu-id="1cc28-164">**IVMVirtualMachine::Save**</span></span>](ivmvirtualmachine-save.md)
-   [<span data-ttu-id="1cc28-165">**IVMVirtualMachine :: Startup**</span><span class="sxs-lookup"><span data-stu-id="1cc28-165">**IVMVirtualMachine::Startup**</span></span>](ivmvirtualmachine-startup.md)
-   [<span data-ttu-id="1cc28-166">**IVMVirtualMachine :: Startup2**</span><span class="sxs-lookup"><span data-stu-id="1cc28-166">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
-   [<span data-ttu-id="1cc28-167">**IVMVirtualMachine::TurnOff**</span><span class="sxs-lookup"><span data-stu-id="1cc28-167">**IVMVirtualMachine::TurnOff**</span></span>](ivmvirtualmachine-turnoff.md)
-   [<span data-ttu-id="1cc28-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="1cc28-168">**IVMVirtualPC::CreateDifferencingVirtualHardDisk**</span></span>](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [<span data-ttu-id="1cc28-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="1cc28-169">**IVMVirtualPC::CreateDynamicVirtualHardDisk**</span></span>](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [<span data-ttu-id="1cc28-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="1cc28-170">**IVMVirtualPC::CreateFixedVirtualHardDisk**</span></span>](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a><span data-ttu-id="1cc28-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cc28-171">Requirements</span></span>



| <span data-ttu-id="1cc28-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cc28-172">Requirement</span></span> | <span data-ttu-id="1cc28-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cc28-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc28-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc28-174">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc28-175">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cc28-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1cc28-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc28-176">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc28-177">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc28-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1cc28-178">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1cc28-178">End of client support</span></span><br/>    | <span data-ttu-id="1cc28-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1cc28-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1cc28-180">Produit</span><span class="sxs-lookup"><span data-stu-id="1cc28-180">Product</span></span><br/>                  | <span data-ttu-id="1cc28-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1cc28-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1cc28-182">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cc28-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cc28-183"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc28-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1cc28-184">IID</span><span class="sxs-lookup"><span data-stu-id="1cc28-184">IID</span></span><br/>                      | <span data-ttu-id="1cc28-185">IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="1cc28-185">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



 

