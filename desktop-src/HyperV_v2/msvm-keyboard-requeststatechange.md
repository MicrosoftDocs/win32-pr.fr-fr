---
description: Demande que l’état de l’élément soit modifié.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: Méthode RequestStateChange de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3358c6c9907717e536466466dd074faf3a038a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951284"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="8a4a7-103">Méthode RequestStateChange de la \_ classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="8a4a7-103">RequestStateChange method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="8a4a7-104">Demande que l’état de l’élément soit modifié.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-104">Requests that the state of the element be changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a4a7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a4a7-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="8a4a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a4a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a4a7-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a4a7-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a4a7-108">Nouvel État demandé pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-108">The new state requested for the element.</span></span> <span data-ttu-id="8a4a7-109">Ces informations seront placées dans la propriété **RequestedState** de l’instance si le code de retour est 0 (« terminé sans erreur »), 3 (« délai d’expiration ») ou 4096 (0x1000) (« travail démarré »).</span><span class="sxs-lookup"><span data-stu-id="8a4a7-109">This information will be placed into the **RequestedState** property of the instance if the return code is 0 ('Completed with No Error'), 3 ('Timeout'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="8a4a7-110">Pour obtenir des explications détaillées sur les valeurs de *RequestedState* , consultez la description des propriétés **EnabledState** et **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="8a4a7-110">For detailed explanations of the *RequestedState* values, see the description of the **EnabledState** and **RequestedState** properties.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8a4a7-111">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8a4a7-112">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="8a4a7-113">**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="8a4a7-114">**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="8a4a7-115">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="8a4a7-116">**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8a4a7-117">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="8a4a7-118">**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="8a4a7-119">**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8a4a7-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8a4a7-121">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8a4a7-122">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a4a7-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a4a7-123">Référence au travail.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-123">A reference to the job.</span></span> <span data-ttu-id="8a4a7-124">Ce paramètre peut avoir la **valeur null** si la tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-124">This parameter can be **Null** if the task is completed.</span></span>

</dd> <dt>

<span data-ttu-id="8a4a7-125">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a4a7-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a4a7-126">Durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-126">The maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="8a4a7-127">Le format d’intervalle doit être utilisé pour spécifier ce délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-127">The interval format must be used to specify this time-out period.</span></span> <span data-ttu-id="8a4a7-128">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="8a4a7-129">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (« utilisation du paramètre de délai d’expiration non pris en charge ») est retourné.</span><span class="sxs-lookup"><span data-stu-id="8a4a7-129">If this property does not contain 0 or **Null**, and the implementation does not support this parameter, a return code of 4098 ("Use Of Timeout Parameter Not Supported") is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a4a7-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a4a7-130">Return value</span></span>

<dl> <dt>

<span data-ttu-id="8a4a7-131">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-132">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-132">**Not supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-133">**Erreur inconnue ou non spécifiée** (2)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-133">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-134">**Impossible de se terminer dans le délai imparti** (3)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-134">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-135">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-135">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-136">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-136">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-137">**En cours d’utilisation** (6)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-137">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-138">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-139">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-140">**Transition d’État non valide** (4097)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-140">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-141">**Utilisation du paramètre timeout non prise en charge** (4098)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-141">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-142">**Occupé** (4099)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-142">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-143">**Méthode réservée** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-143">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8a4a7-144">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8a4a7-144">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8a4a7-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a4a7-145">Requirements</span></span>



| <span data-ttu-id="8a4a7-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a4a7-146">Requirement</span></span> | <span data-ttu-id="8a4a7-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a4a7-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a4a7-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a4a7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8a4a7-149">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a4a7-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8a4a7-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a4a7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8a4a7-151">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a4a7-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a4a7-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8a4a7-152">Namespace</span></span><br/>                | <span data-ttu-id="8a4a7-153">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8a4a7-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8a4a7-154">MOF</span><span class="sxs-lookup"><span data-stu-id="8a4a7-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a4a7-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a4a7-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a4a7-156">DLL</span><span class="sxs-lookup"><span data-stu-id="8a4a7-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a4a7-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a4a7-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a4a7-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a4a7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a4a7-159">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="8a4a7-159">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




