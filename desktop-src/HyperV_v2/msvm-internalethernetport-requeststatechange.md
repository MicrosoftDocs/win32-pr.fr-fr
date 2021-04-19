---
description: Demande un changement d’État.
ms.assetid: 34f226a2-392b-4b3c-898e-308af52b71a2
title: Méthode RequestStateChange de la classe Msvm_InternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 88483a72a677863f7e81ccbf50a8fb1f3dee7d03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514647"
---
# <a name="requeststatechange-method-of-the-msvm_internalethernetport-class"></a><span data-ttu-id="6a8df-103">Méthode RequestStateChange de la \_ classe MSVM InternalEthernetPort</span><span class="sxs-lookup"><span data-stu-id="6a8df-103">RequestStateChange method of the Msvm\_InternalEthernetPort class</span></span>

<span data-ttu-id="6a8df-104">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="6a8df-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a8df-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="6a8df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a8df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a8df-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a8df-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8df-108">Nouvel état.</span><span class="sxs-lookup"><span data-stu-id="6a8df-108">The new state.</span></span> <span data-ttu-id="6a8df-109">Les informations sont placées dans la propriété **RequestedState** de l’instance si le code de retour de la méthode **RequestStateChange** est 0 ou 4096.</span><span class="sxs-lookup"><span data-stu-id="6a8df-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="6a8df-110">Pour plus d’informations, consultez la description des propriétés **EnabledState** et **RequestedState** de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6a8df-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="6a8df-111">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a8df-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6a8df-112">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="6a8df-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6a8df-113">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="6a8df-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="6a8df-114">**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="6a8df-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="6a8df-115">**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="6a8df-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="6a8df-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="6a8df-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="6a8df-117">**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="6a8df-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="6a8df-118">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="6a8df-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="6a8df-119">**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="6a8df-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="6a8df-120">**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="6a8df-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a8df-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="6a8df-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6a8df-122">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6a8df-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="6a8df-123">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6a8df-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8df-124">Peut contenir une référence au [**\_ ConcreteJob CIM**](cim-concretejob.md) créé pour effectuer le suivi de la transition d’État initiée par l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="6a8df-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="6a8df-125">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a8df-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8df-126">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="6a8df-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="6a8df-127">Le format d’intervalle doit être utilisé pour spécifier le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="6a8df-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="6a8df-128">La valeur 0 ou **null** indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="6a8df-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="6a8df-129">Si cette propriété ne contient pas 0 ou **null** et que l’implémentation ne prend pas en charge ce paramètre, un code de retour de 4098 (**utilisation du paramètre timeout non pris en charge**) doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="6a8df-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a8df-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a8df-130">Return value</span></span>

<span data-ttu-id="6a8df-131">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a8df-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6a8df-132">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="6a8df-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6a8df-133">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="6a8df-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6a8df-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a8df-134">Requirements</span></span>



| <span data-ttu-id="6a8df-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a8df-135">Requirement</span></span> | <span data-ttu-id="6a8df-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a8df-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8df-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a8df-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6a8df-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6a8df-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6a8df-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a8df-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6a8df-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6a8df-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6a8df-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a8df-141">Namespace</span></span><br/>                | <span data-ttu-id="6a8df-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6a8df-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a8df-143">MOF</span><span class="sxs-lookup"><span data-stu-id="6a8df-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a8df-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a8df-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a8df-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6a8df-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a8df-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a8df-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a8df-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a8df-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a8df-148">**MSVM \_ InternalEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="6a8df-148">**Msvm\_InternalEthernetPort**</span></span>](msvm-internalethernetport.md)
</dt> </dl>

 

 




