---
description: Demande que l’état du composant d’interface de service invité soit remplacé par la valeur spécifiée.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Msvm_GuestServiceInterfaceComponent :: RequestStateChange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524641"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a><span data-ttu-id="23e98-103">MSVM \_ GuestServiceInterfaceComponent :: RequestStateChange, méthode</span><span class="sxs-lookup"><span data-stu-id="23e98-103">Msvm\_GuestServiceInterfaceComponent::RequestStateChange method</span></span>

<span data-ttu-id="23e98-104">Demande que l’état du composant d’interface de service invité soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="23e98-104">Requests that the state of the guest service interface component be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23e98-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="23e98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23e98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e98-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23e98-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23e98-108">Type : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23e98-108">Type: **uint16**</span></span>

<span data-ttu-id="23e98-109">Nouvel état.</span><span class="sxs-lookup"><span data-stu-id="23e98-109">The new state.</span></span> <span data-ttu-id="23e98-110">Les informations sont placées dans la propriété **RequestedState** de l’instance si le code de retour de la méthode **RequestStateChange** est 0 ou 4096.</span><span class="sxs-lookup"><span data-stu-id="23e98-110">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="23e98-111">Pour plus d’informations, consultez la description des propriétés **EnabledState** et **RequestedState** de l’élément.</span><span class="sxs-lookup"><span data-stu-id="23e98-111">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="23e98-112">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="23e98-112">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="23e98-113">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="23e98-113">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="23e98-114">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="23e98-114">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="23e98-115">**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="23e98-115">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="23e98-116">**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="23e98-116">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="23e98-117">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="23e98-117">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="23e98-118">**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="23e98-118">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="23e98-119">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="23e98-119">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="23e98-120">**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="23e98-120">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="23e98-121">**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="23e98-121">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="23e98-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="23e98-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="23e98-123">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="23e98-123">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="23e98-124">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="23e98-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23e98-125">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="23e98-125">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="23e98-126">Référence facultative à un objet [**\_ ConcreteJob MSVM**](msvm-concretejob.md) qui est retourné si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="23e98-126">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="23e98-127">Si elle est présente, la référence retournée peut être utilisée pour surveiller la progression et obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="23e98-127">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="23e98-128">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23e98-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23e98-129">Type : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="23e98-129">Type: **datetime**</span></span>

<span data-ttu-id="23e98-130">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="23e98-130">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="23e98-131">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="23e98-131">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="23e98-132">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="23e98-132">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="23e98-133">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="23e98-133">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23e98-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23e98-134">Return value</span></span>

<span data-ttu-id="23e98-135">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23e98-135">Type: **uint32**</span></span>

<span data-ttu-id="23e98-136">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="23e98-136">This method returns one of the following values.</span></span>



| <span data-ttu-id="23e98-137">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="23e98-137">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="23e98-138">Description</span><span class="sxs-lookup"><span data-stu-id="23e98-138">Description</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="23e98-139"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-139"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="23e98-140">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="23e98-140">Success.</span></span><br/> |
| <dl> <span data-ttu-id="23e98-141"><dt>**Non pris en charge**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-141"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                     |
| <dl> <span data-ttu-id="23e98-142"><dt>**Erreur 2 inconnue/non spécifiée**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="23e98-142"><dt>**Unknown/Unspecified Error**</dt> <dt>2</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="23e98-143"><dt>**Impossible de se terminer dans le délai d’expiration**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-143"><dt>**Can NOT complete within Timeout Period**</dt> <dt>3</dt></span></span> </dl>            |                     |
| <dl> <span data-ttu-id="23e98-144"><dt>**Échec**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-144"><dt>**Failed**</dt> <dt>4</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="23e98-145"><dt>**Paramètre non valide**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-145"><dt>**Invalid Parameter**</dt> <dt>5</dt></span></span> </dl>                                 |                     |
| <dl> <span data-ttu-id="23e98-146"><dt>**En cours d’utilisation**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-146"><dt>**In Use**</dt> <dt>6</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="23e98-147"><dt>**DMTF réservé**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-147"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                    |                     |
| <dl> <span data-ttu-id="23e98-148"><dt>**Paramètres de méthode vérifiés-transition démarrée**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-148"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> |                     |
| <dl> <span data-ttu-id="23e98-149"><dt>**Transition d’État non valide**</dt> <dt>4097</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-149"><dt>**Invalid State Transition**</dt> <dt>4097</dt></span></span> </dl>                       |                     |
| <dl> <span data-ttu-id="23e98-150"><dt>**Utilisation du paramètre timeout non prise en charge**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-150"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                     |
| <dl> <span data-ttu-id="23e98-151"><dt>**Occupé**</dt> <dt>4099</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-151"><dt>**Busy**</dt> <dt>4099</dt></span></span> </dl>                                           |                     |
| <dl> <span data-ttu-id="23e98-152"><dt>**Méthode réservée**</dt> <dt>4100.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-152"><dt>**Method Reserved**</dt> <dt>4100..32767</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="23e98-153"><dt></dt> <dt>32 768.. 65535</dt> spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="23e98-153"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                        |                     |



 

## <a name="requirements"></a><span data-ttu-id="23e98-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23e98-154">Requirements</span></span>



| <span data-ttu-id="23e98-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23e98-155">Requirement</span></span> | <span data-ttu-id="23e98-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="23e98-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e98-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23e98-157">Minimum supported client</span></span><br/> | <span data-ttu-id="23e98-158">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23e98-158">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="23e98-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23e98-159">Minimum supported server</span></span><br/> | <span data-ttu-id="23e98-160">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23e98-160">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="23e98-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="23e98-161">Namespace</span></span><br/>                | <span data-ttu-id="23e98-162">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="23e98-162">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="23e98-163">MOF</span><span class="sxs-lookup"><span data-stu-id="23e98-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23e98-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23e98-165">DLL</span><span class="sxs-lookup"><span data-stu-id="23e98-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23e98-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23e98-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="23e98-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23e98-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e98-168">**MSVM \_ GuestServiceInterfaceComponent**</span><span class="sxs-lookup"><span data-stu-id="23e98-168">**Msvm\_GuestServiceInterfaceComponent**</span></span>](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

