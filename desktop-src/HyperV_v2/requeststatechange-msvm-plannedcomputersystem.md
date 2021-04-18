---
description: Demande que l’état du système planifié soit remplacé par la valeur spécifiée.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Méthode RequestStateChange de la classe Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519098"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a><span data-ttu-id="0dc2b-103">Méthode RequestStateChange de la \_ classe MSVM PlannedComputerSystem</span><span class="sxs-lookup"><span data-stu-id="0dc2b-103">RequestStateChange method of the Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="0dc2b-104">Demande que l’état du système planifié soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0dc2b-104">Requests that the state of the planned system be changed to the value specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dc2b-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="0dc2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dc2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc2b-107">*RequestedState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0dc2b-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc2b-108">État demandé pour le système planifié.</span><span class="sxs-lookup"><span data-stu-id="0dc2b-108">The requested state for the planned system.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0dc2b-109">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-109">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0dc2b-110">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-110">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="0dc2b-111">**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-111">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="0dc2b-112">**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-112">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="0dc2b-113">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-113">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="0dc2b-114">**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-114">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="0dc2b-115">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-115">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="0dc2b-116">**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-116">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="0dc2b-117">**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-117">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0dc2b-118">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-118">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0dc2b-119">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0dc2b-119">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="0dc2b-120">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0dc2b-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc2b-121">Ce paramètre n’est pas utilisé et doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0dc2b-121">This parameter is not used and should be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0dc2b-122">*TimeoutPeriod* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0dc2b-122">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc2b-123">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0dc2b-123">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc2b-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0dc2b-124">Return value</span></span>

<span data-ttu-id="0dc2b-125">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0dc2b-125">This method returns one of the following values.</span></span>



| <span data-ttu-id="0dc2b-126">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0dc2b-126">Return code/value</span></span>                                                                                                                      | <span data-ttu-id="0dc2b-127">Description</span><span class="sxs-lookup"><span data-stu-id="0dc2b-127">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0dc2b-128"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-128"><dt></dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="0dc2b-129">Succès</span><span class="sxs-lookup"><span data-stu-id="0dc2b-129">Success</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="0dc2b-130"><dt></dt><dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-130"><dt></dt> <dt>4096</dt></span></span> </dl>  |                                                                                    |
| <dl> <span data-ttu-id="0dc2b-131"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-131"><dt></dt> <dt>32768</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="0dc2b-132"><dt></dt><dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-132"><dt></dt> <dt>32769</dt></span></span> </dl> | <span data-ttu-id="0dc2b-133">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0dc2b-133">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="0dc2b-134"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-134"><dt></dt> <dt>32770</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="0dc2b-135"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-135"><dt></dt> <dt>32771</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="0dc2b-136"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-136"><dt></dt> <dt>32772</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="0dc2b-137"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-137"><dt></dt> <dt>32773</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="0dc2b-138"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-138"><dt></dt> <dt>32774</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="0dc2b-139"><dt></dt><dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-139"><dt></dt> <dt>32775</dt></span></span> </dl> | <span data-ttu-id="0dc2b-140">La valeur spécifiée dans le paramètre *RequestedState* n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0dc2b-140">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="0dc2b-141"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-141"><dt></dt> <dt>32776</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="0dc2b-142"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-142"><dt></dt> <dt>32777</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="0dc2b-143"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-143"><dt></dt> <dt>32778</dt></span></span> </dl> |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="0dc2b-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0dc2b-144">Requirements</span></span>



| <span data-ttu-id="0dc2b-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0dc2b-145">Requirement</span></span> | <span data-ttu-id="0dc2b-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="0dc2b-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc2b-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc2b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc2b-148">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc2b-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0dc2b-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc2b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc2b-150">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc2b-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0dc2b-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0dc2b-151">Namespace</span></span><br/>                | <span data-ttu-id="0dc2b-152">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0dc2b-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0dc2b-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0dc2b-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0dc2b-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0dc2b-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0dc2b-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dc2b-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2b-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0dc2b-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dc2b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc2b-158">**MSVM \_ PlannedComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="0dc2b-158">**Msvm\_PlannedComputerSystem**</span></span>](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




