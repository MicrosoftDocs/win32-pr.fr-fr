---
description: Méthode RequestStateChange de la classe Msvm_DiskDrive-demande un changement d’État.
ms.assetid: 9dfa96b1-19d4-42ea-b927-80b0d63a9be1
title: Méthode RequestStateChange de la classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca2f9263d29a4412ab505e94268d0d18d28a60b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112067"
---
# <a name="requeststatechange-method-of-the-msvm_diskdrive-class"></a><span data-ttu-id="04e3b-103">Méthode RequestStateChange de la \_ classe MSVM DiskDrive</span><span class="sxs-lookup"><span data-stu-id="04e3b-103">RequestStateChange method of the Msvm\_DiskDrive class</span></span>

<span data-ttu-id="04e3b-104">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="04e3b-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="04e3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04e3b-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="04e3b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04e3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e3b-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04e3b-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e3b-108">État demandé pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="04e3b-108">The state requested for the element.</span></span> <span data-ttu-id="04e3b-109">Ces informations seront placées dans la propriété RequestedState de l’instance si le code de retour de la méthode RequestStateChange est 0 (terminé sans erreur») ou 4096 (0x1000) ('Job Started').</span><span class="sxs-lookup"><span data-stu-id="04e3b-109">This information will be placed into the RequestedState property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="04e3b-110">Reportez-vous à la description des propriétés EnabledState et RequestedState pour obtenir des explications détaillées sur les valeurs de RequestedState.</span><span class="sxs-lookup"><span data-stu-id="04e3b-110">Refer to the description of the EnabledState and RequestedState properties for the detailed explanations of the RequestedState values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="04e3b-111">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="04e3b-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="04e3b-112">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="04e3b-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="04e3b-113">**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="04e3b-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="04e3b-114">**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="04e3b-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="04e3b-115">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="04e3b-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="04e3b-116">**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="04e3b-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="04e3b-117">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="04e3b-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="04e3b-118">**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="04e3b-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="04e3b-119">**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="04e3b-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="04e3b-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="04e3b-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="04e3b-121">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="04e3b-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="04e3b-122">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04e3b-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04e3b-123">Peut contenir une référence au ConcreteJob créé pour effectuer le suivi de la transition d’État initiée par l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="04e3b-123">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="04e3b-124">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04e3b-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e3b-125">Délai d’attente qui spécifie la durée maximale pendant laquelle le client attend la transition vers le nouvel État.</span><span class="sxs-lookup"><span data-stu-id="04e3b-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="04e3b-126">Le format d’intervalle doit être utilisé pour spécifier le TimeoutPeriod.</span><span class="sxs-lookup"><span data-stu-id="04e3b-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="04e3b-127">La valeur 0 ou un paramètre null indique que le client n’a aucune exigence de temps pour la transition.</span><span class="sxs-lookup"><span data-stu-id="04e3b-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="04e3b-128">Si cette propriété ne contient pas 0 ou null et que l’implémentation ne prend pas en charge ce paramètre, le code de retour « utilisation du paramètre de délai d’attente non pris en charge » doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="04e3b-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e3b-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="04e3b-129">Return value</span></span>

<span data-ttu-id="04e3b-130">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="04e3b-130">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="04e3b-131">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="04e3b-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04e3b-132">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="04e3b-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="04e3b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04e3b-133">Requirements</span></span>



| <span data-ttu-id="04e3b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04e3b-134">Requirement</span></span> | <span data-ttu-id="04e3b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="04e3b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e3b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04e3b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="04e3b-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="04e3b-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="04e3b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04e3b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="04e3b-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="04e3b-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="04e3b-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="04e3b-140">Namespace</span></span><br/>                | <span data-ttu-id="04e3b-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="04e3b-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="04e3b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="04e3b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04e3b-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04e3b-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04e3b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="04e3b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04e3b-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04e3b-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04e3b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04e3b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e3b-147">**MSVM \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="04e3b-147">**Msvm\_DiskDrive**</span></span>](msvm-diskdrive.md)
</dt> </dl>

 

 




