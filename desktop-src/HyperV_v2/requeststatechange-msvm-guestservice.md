---
description: Demande que l’état du service invité soit remplacé par la valeur spécifiée.
ms.assetid: F2853BB3-4074-431C-9E10-26AA0757FE99
title: 'Msvm_GuestService :: RequestStateChange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1360c36b58c96b7e621e5f339bd503ce4f1390b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757648"
---
# <a name="msvm_guestservicerequeststatechange-method"></a><span data-ttu-id="8a071-103">MSVM \_ GuestService :: RequestStateChange, méthode</span><span class="sxs-lookup"><span data-stu-id="8a071-103">Msvm\_GuestService::RequestStateChange method</span></span>

<span data-ttu-id="8a071-104">Demande que l’état du service invité soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8a071-104">Requests that the state of the guest service be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a071-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a071-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="8a071-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a071-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a071-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a071-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a071-108">Nouvel état.</span><span class="sxs-lookup"><span data-stu-id="8a071-108">The new state.</span></span> <span data-ttu-id="8a071-109">Les informations sont placées dans la propriété **RequestedState** de l’instance si le code de retour de la méthode **RequestStateChange** est 0 ou 4096.</span><span class="sxs-lookup"><span data-stu-id="8a071-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="8a071-110">Pour plus d’informations, consultez la description des propriétés **EnabledState** et **RequestedState** de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8a071-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="8a071-111">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a071-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8a071-112">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="8a071-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8a071-113">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="8a071-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="8a071-114">**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="8a071-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="8a071-115">**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="8a071-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="8a071-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="8a071-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="8a071-117">**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="8a071-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="8a071-118">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="8a071-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="8a071-119">**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="8a071-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="8a071-120">**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="8a071-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8a071-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="8a071-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="8a071-122">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8a071-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8a071-123">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a071-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a071-124">Référence facultative à un objet [**CIM \_ ConcreteJob**](cim-concretejob.md) qui est retourné si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="8a071-124">An optional reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="8a071-125">Si elle est présente, la référence retournée peut être utilisée pour surveiller la progression et obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="8a071-125">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="8a071-126">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a071-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a071-127">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="8a071-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="8a071-128">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="8a071-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="8a071-129">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="8a071-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="8a071-130">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="8a071-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a071-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a071-131">Return value</span></span>

<span data-ttu-id="8a071-132">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a071-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="8a071-133">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8a071-133">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="8a071-134">Description</span><span class="sxs-lookup"><span data-stu-id="8a071-134">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a071-135"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8a071-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="8a071-136">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="8a071-136">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="8a071-137"><dt>**Non pris en charge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8a071-137"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                                                                                    |
| <dl> <span data-ttu-id="8a071-138"><dt>**Paramètres de méthode vérifiés-transition démarrée**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="8a071-138"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="8a071-139">La transition est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="8a071-139">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="8a071-140"><dt>**Utilisation du paramètre timeout non prise en charge**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="8a071-140"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                                                                                    |
| <dl> <span data-ttu-id="8a071-141"><dt>**Accès refusé**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="8a071-141"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="8a071-142">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="8a071-142">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="8a071-143"><dt>**État non valide pour cette opération**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="8a071-143"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="8a071-144">La valeur spécifiée dans le paramètre *RequestedState* n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8a071-144">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8a071-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a071-145">Requirements</span></span>



| <span data-ttu-id="8a071-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a071-146">Requirement</span></span> | <span data-ttu-id="8a071-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a071-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a071-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a071-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8a071-149">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a071-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8a071-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a071-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8a071-151">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a071-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a071-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8a071-152">Namespace</span></span><br/>                | <span data-ttu-id="8a071-153">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8a071-153">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="8a071-154">MOF</span><span class="sxs-lookup"><span data-stu-id="8a071-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a071-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a071-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a071-156">DLL</span><span class="sxs-lookup"><span data-stu-id="8a071-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a071-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a071-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a071-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a071-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a071-159">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="8a071-159">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




