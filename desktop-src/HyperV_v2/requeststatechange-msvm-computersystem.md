---
description: Demande que l’état de l’ordinateur virtuel soit remplacé par la valeur spécifiée.
ms.assetid: 87BE4C7D-604B-4F8D-B4DC-89BD563E3999
title: Méthode RequestStateChange de la classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 291d72797b1ee765507a3d23921cd518cf605354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211103"
---
# <a name="requeststatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="58c6d-103">Méthode RequestStateChange de la \_ classe MSVM ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="58c6d-103">RequestStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="58c6d-104">Demande que l’état de l’ordinateur virtuel soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="58c6d-104">Requests that the state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="58c6d-105">L’appel de la méthode **RequestStateChange** plusieurs fois peut entraîner le remplacement ou la perte des demandes antérieures.</span><span class="sxs-lookup"><span data-stu-id="58c6d-105">Invoking the **RequestStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="58c6d-106">Cette méthode est prise en charge uniquement pour les instances de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représentent un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="58c6d-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

<span data-ttu-id="58c6d-107">Tandis que le changement d’État est en cours, la propriété **requestedstate** est remplacée par la valeur du paramètre *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="58c6d-107">While the state change is in progress, the **RequestedState** property is changed to the value of the *RequestedState* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c6d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58c6d-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="58c6d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58c6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c6d-110">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58c6d-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c6d-111">Type : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58c6d-111">Type: **uint16**</span></span>

<span data-ttu-id="58c6d-112">Nouvel état.</span><span class="sxs-lookup"><span data-stu-id="58c6d-112">The new state.</span></span> <span data-ttu-id="58c6d-113">Les valeurs supérieures à 32767 sont des valeurs proposées par le **DMTF** et peuvent faire l’objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="58c6d-113">Values that are greater than 32767 are **DMTF** proposed values and are subject to change.</span></span>

<span data-ttu-id="58c6d-114">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="58c6d-114">Here are possible values:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="58c6d-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="58c6d-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-116">Correspond à [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = other.</span><span class="sxs-lookup"><span data-stu-id="58c6d-116">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Other.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="58c6d-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="58c6d-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-118">Correspond à [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled.</span><span class="sxs-lookup"><span data-stu-id="58c6d-118">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="58c6d-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="58c6d-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-120">Correspond à [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Disabled.</span><span class="sxs-lookup"><span data-stu-id="58c6d-120">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Disabled.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="58c6d-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="58c6d-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-122">Valide dans la version 1 (v1) d’Hyper-V uniquement.</span><span class="sxs-lookup"><span data-stu-id="58c6d-122">Valid in version 1 (V1) of Hyper-V only.</span></span> <span data-ttu-id="58c6d-123">L’ordinateur virtuel est en cours d’arrêt par le biais du service d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="58c6d-123">The virtual machine is shutting down via the shutdown service.</span></span> <span data-ttu-id="58c6d-124">Correspond à [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span><span class="sxs-lookup"><span data-stu-id="58c6d-124">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="58c6d-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="58c6d-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-126">Correspond à [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled mais offline.</span><span class="sxs-lookup"><span data-stu-id="58c6d-126">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled but offline.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="58c6d-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="58c6d-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="58c6d-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="58c6d-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="58c6d-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="58c6d-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-130">Correspond à [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = suspend, Enabled mais Paused.</span><span class="sxs-lookup"><span data-stu-id="58c6d-130">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Quiesce, Enabled but paused.</span></span>

</dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="58c6d-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="58c6d-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-132">Transition d’état de **off** ou **saved** à **Running**.</span><span class="sxs-lookup"><span data-stu-id="58c6d-132">State transition from **Off** or **Saved** to **Running**.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="58c6d-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="58c6d-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-134">Réinitialisez la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="58c6d-134">Reset the virtual machine.</span></span> <span data-ttu-id="58c6d-135">Correspond à [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Reset.</span><span class="sxs-lookup"><span data-stu-id="58c6d-135">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Reset.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="58c6d-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Enregistrement** (32773)</span><span class="sxs-lookup"><span data-stu-id="58c6d-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-137">Dans la version 1 (v1) d’Hyper-V, correspond à **EnabledStateSaving**.</span><span class="sxs-lookup"><span data-stu-id="58c6d-137">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateSaving**.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="58c6d-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Suspension** (32776)</span><span class="sxs-lookup"><span data-stu-id="58c6d-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-139">Dans la version 1 (v1) d’Hyper-V, correspond à **EnabledStatePausing**.</span><span class="sxs-lookup"><span data-stu-id="58c6d-139">In version 1 (V1) of Hyper-V, corresponds to **EnabledStatePausing**.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="58c6d-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Reprise** (32777)</span><span class="sxs-lookup"><span data-stu-id="58c6d-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-141">Dans la version 1 (v1) d’Hyper-V, correspond à **EnabledStateResuming**.</span><span class="sxs-lookup"><span data-stu-id="58c6d-141">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateResuming**.</span></span> <span data-ttu-id="58c6d-142">Transition d’état de **suspendu** à **en cours d’exécution**.</span><span class="sxs-lookup"><span data-stu-id="58c6d-142">State transition from **Paused** to **Running**.</span></span>

</dd> <dt>

<span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>

<span data-ttu-id="58c6d-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span><span class="sxs-lookup"><span data-stu-id="58c6d-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-144">Correspond à **EnabledStateFastSuspend**.</span><span class="sxs-lookup"><span data-stu-id="58c6d-144">Corresponds to **EnabledStateFastSuspend**.</span></span>

</dd> <dt>

<span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>

<span data-ttu-id="58c6d-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span><span class="sxs-lookup"><span data-stu-id="58c6d-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span></span>


</dt> <dd>

<span data-ttu-id="58c6d-146">Correspond à **EnabledStateFastSuspending**.</span><span class="sxs-lookup"><span data-stu-id="58c6d-146">Corresponds to **EnabledStateFastSuspending**.</span></span> <span data-ttu-id="58c6d-147">Transition d’état de l' **exécution** à **FastSaved**.</span><span class="sxs-lookup"><span data-stu-id="58c6d-147">State transition from **Running** to **FastSaved**.</span></span>

</dd> </dl>

<span data-ttu-id="58c6d-148">Ces valeurs représentent les États critiques :</span><span class="sxs-lookup"><span data-stu-id="58c6d-148">These values represent critical states:</span></span>

<dt>

<span id="RunningCritical"></span><span id="runningcritical"></span><span id="RUNNINGCRITICAL"></span>

<span data-ttu-id="58c6d-149">**RunningCritical** (32781)</span><span class="sxs-lookup"><span data-stu-id="58c6d-149">**RunningCritical** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="OffCritical"></span><span id="offcritical"></span><span id="OFFCRITICAL"></span>

<span data-ttu-id="58c6d-150">**OffCritical** (32782)</span><span class="sxs-lookup"><span data-stu-id="58c6d-150">**OffCritical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="StoppingCritical"></span><span id="stoppingcritical"></span><span id="STOPPINGCRITICAL"></span>

<span data-ttu-id="58c6d-151">**StoppingCritical** (32783)</span><span class="sxs-lookup"><span data-stu-id="58c6d-151">**StoppingCritical** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="SavedCritical"></span><span id="savedcritical"></span><span id="SAVEDCRITICAL"></span>

<span data-ttu-id="58c6d-152">**SavedCritical** (32784)</span><span class="sxs-lookup"><span data-stu-id="58c6d-152">**SavedCritical** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="PausedCritical"></span><span id="pausedcritical"></span><span id="PAUSEDCRITICAL"></span>

<span data-ttu-id="58c6d-153">**PausedCritical** (32785)</span><span class="sxs-lookup"><span data-stu-id="58c6d-153">**PausedCritical** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="StartingCritical"></span><span id="startingcritical"></span><span id="STARTINGCRITICAL"></span>

<span data-ttu-id="58c6d-154">**StartingCritical** (32786)</span><span class="sxs-lookup"><span data-stu-id="58c6d-154">**StartingCritical** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="ResetCritical"></span><span id="resetcritical"></span><span id="RESETCRITICAL"></span>

<span data-ttu-id="58c6d-155">**ResetCritical** (32787)</span><span class="sxs-lookup"><span data-stu-id="58c6d-155">**ResetCritical** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="SavingCritical"></span><span id="savingcritical"></span><span id="SAVINGCRITICAL"></span>

<span data-ttu-id="58c6d-156">**SavingCritical** (32788)</span><span class="sxs-lookup"><span data-stu-id="58c6d-156">**SavingCritical** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="PausingCritical"></span><span id="pausingcritical"></span><span id="PAUSINGCRITICAL"></span>

<span data-ttu-id="58c6d-157">**PausingCritical** (32789)</span><span class="sxs-lookup"><span data-stu-id="58c6d-157">**PausingCritical** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="ResumingCritical"></span><span id="resumingcritical"></span><span id="RESUMINGCRITICAL"></span>

<span data-ttu-id="58c6d-158">**ResumingCritical** (32790)</span><span class="sxs-lookup"><span data-stu-id="58c6d-158">**ResumingCritical** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavedCritical"></span><span id="fastsavedcritical"></span><span id="FASTSAVEDCRITICAL"></span>

<span data-ttu-id="58c6d-159">**FastSavedCritical** (32791)</span><span class="sxs-lookup"><span data-stu-id="58c6d-159">**FastSavedCritical** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavingCritical"></span><span id="fastsavingcritical"></span><span id="FASTSAVINGCRITICAL"></span>

<span data-ttu-id="58c6d-160">**FastSavingCritical** (32792)</span><span class="sxs-lookup"><span data-stu-id="58c6d-160">**FastSavingCritical** (32792)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="58c6d-161">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="58c6d-161">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58c6d-162">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="58c6d-162">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="58c6d-163">Référence facultative à un objet [**\_ ConcreteJob MSVM**](msvm-concretejob.md) qui est retourné si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="58c6d-163">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="58c6d-164">Si elle est présente, la référence retournée peut être utilisée pour surveiller la progression et obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="58c6d-164">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="58c6d-165">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58c6d-165">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c6d-166">Type : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="58c6d-166">Type: **datetime**</span></span>

<span data-ttu-id="58c6d-167">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="58c6d-167">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c6d-168">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58c6d-168">Return value</span></span>

<span data-ttu-id="58c6d-169">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58c6d-169">Type: **uint32**</span></span>

<span data-ttu-id="58c6d-170">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="58c6d-170">This method returns one of the following values.</span></span>



| <span data-ttu-id="58c6d-171">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="58c6d-171">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="58c6d-172">Description</span><span class="sxs-lookup"><span data-stu-id="58c6d-172">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58c6d-173"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-173"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="58c6d-174">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="58c6d-174">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="58c6d-175"><dt>**Paramètres de méthode vérifiés-transition démarrée**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-175"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="58c6d-176">La transition est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="58c6d-176">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="58c6d-177"><dt>**Accès refusé**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-177"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="58c6d-178">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="58c6d-178">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="58c6d-179"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-179"><dt></dt> <dt>32768</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="58c6d-180"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-180"><dt></dt> <dt>32770</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="58c6d-181"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-181"><dt></dt> <dt>32771</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="58c6d-182"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-182"><dt></dt> <dt>32772</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="58c6d-183"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-183"><dt></dt> <dt>32773</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="58c6d-184"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-184"><dt></dt> <dt>32774</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="58c6d-185"><dt>**État non valide pour cette opération**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-185"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="58c6d-186">La valeur spécifiée dans le paramètre *RequestedState* n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="58c6d-186">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="58c6d-187"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-187"><dt></dt> <dt>32776</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="58c6d-188"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-188"><dt></dt> <dt>32777</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="58c6d-189"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-189"><dt></dt> <dt>32778</dt></span></span> </dl>                                                  |                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="58c6d-190">Notes</span><span class="sxs-lookup"><span data-stu-id="58c6d-190">Remarks</span></span>

<span data-ttu-id="58c6d-191">L’accès à la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="58c6d-191">Access to the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="58c6d-192">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="58c6d-192">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="58c6d-193">Exemples</span><span class="sxs-lookup"><span data-stu-id="58c6d-193">Examples</span></span>

<span data-ttu-id="58c6d-194">L’exemple C# suivant démarre ou désactive un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="58c6d-194">The following C# example starts or disables a virtual machine.</span></span> <span data-ttu-id="58c6d-195">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="58c6d-195">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58c6d-196">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="58c6d-196">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    public class RequestStateChangeClass
    {
        public static void RequestStateChange(string vmName, string action)
        {
            ManagementScope scope = new ManagementScope(@"\\.\root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

            if (null == vm)
            {
                throw new ArgumentException(
                    string.Format(
                    "The virtual machine '{0}' could not be found.", 
                    vmName));
            }

            ManagementBaseObject inParams = vm.GetMethodParameters("RequestStateChange");

            const int Enabled = 2;
            const int Disabled = 3;

            if (action.ToLower() == "start")
            {
                inParams["RequestedState"] = Enabled;
            }
            else if (action.ToLower() == "stop")
            {
                inParams["RequestedState"] = Disabled;
            }
            else
            {
                throw new Exception("Wrong action is specified");
            }

            ManagementBaseObject outParams = vm.InvokeMethod(
                "RequestStateChange", 
                inParams, 
                null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine(
                        "{0} state was changed successfully.", 
                        vmName);
                }
                else
                {
                    Console.WriteLine("Failed to change virtual system state");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine(
                    "{0} state was changed successfully.", 
                    vmName);
            }
            else
            {
                Console.WriteLine(
                    "Change virtual system state failed with error {0}", 
                    outParams["ReturnValue"]);
            }

        }

        public static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: <application> vmName action");
                Console.WriteLine("action: start|stop");
                return;
            }

            RequestStateChange(args[0], args[1]);
        }

    }
}
```



<span data-ttu-id="58c6d-197">L’exemple de Visual Basic Scripting Edition (VBScript) suivant démarre ou désactive un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="58c6d-197">The following Visual Basic Scripting Edition (VBScript) example starts or disables a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58c6d-198">Pour fonctionner correctement, le code suivant doit être exécuté sur le serveur hôte de l’ordinateur virtuel et doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="58c6d-198">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```VB
dim objWMIService
dim fileSystem

const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const Enabled = 2
const Disabled = 3



Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    strComputer = "."
    set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       action = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript StartVM.vbs vmName start|stop"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)

    if RequestStateChange(computerSystem, action) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "RequestStateChange failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Turn on a virtual machine
'-----------------------------------------------------------------
Function RequestStateChange(computerSystem, action)
    WriteLog Format2("RequestStateChange({0}, {1})", computerSystem.ElementName, action)

    RequestStateChange = false
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    
    if action = "start" then
        objInParam.RequestedState = Enabled
    else
        objInParam.RequestedState = Disabled
    end if

    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VM {0} was started successfully", computerSystem.ElementName)
            RequestStateChange = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)

    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        end if

    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    dim WMIJob

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting

        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState

    wend


    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\StartVM.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="58c6d-199">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58c6d-199">Requirements</span></span>



| <span data-ttu-id="58c6d-200">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58c6d-200">Requirement</span></span> | <span data-ttu-id="58c6d-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="58c6d-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c6d-202">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58c6d-202">Minimum supported client</span></span><br/> | <span data-ttu-id="58c6d-203">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58c6d-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="58c6d-204">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58c6d-204">Minimum supported server</span></span><br/> | <span data-ttu-id="58c6d-205">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58c6d-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58c6d-206">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="58c6d-206">Namespace</span></span><br/>                | <span data-ttu-id="58c6d-207">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="58c6d-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="58c6d-208">MOF</span><span class="sxs-lookup"><span data-stu-id="58c6d-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58c6d-209"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58c6d-210">DLL</span><span class="sxs-lookup"><span data-stu-id="58c6d-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58c6d-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58c6d-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58c6d-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58c6d-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c6d-213">**MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="58c6d-213">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

