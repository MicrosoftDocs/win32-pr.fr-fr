---
description: Lance une opération d’arrêt du système d’exploitation sur l’ordinateur virtuel enfant associé. Si la valeur zéro (0) est retournée, l’arrêt a été lancé avec succès. Tout autre code de retour indique une condition d’erreur.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Méthode InitiateShutdown de la classe Msvm_ShutdownComponent (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203601"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="903f9-105">Méthode InitiateShutdown de la \_ classe ShutdownComponent MSVM</span><span class="sxs-lookup"><span data-stu-id="903f9-105">InitiateShutdown method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="903f9-106">Lance une opération d’arrêt du système d’exploitation sur l’ordinateur virtuel enfant associé.</span><span class="sxs-lookup"><span data-stu-id="903f9-106">Initiates an operating system shutdown operation on the associated child virtual machine.</span></span> <span data-ttu-id="903f9-107">Si la valeur zéro (0) est retournée, l’arrêt a été lancé avec succès.</span><span class="sxs-lookup"><span data-stu-id="903f9-107">If zero (0) is returned, then the shutdown was initiated successfully.</span></span> <span data-ttu-id="903f9-108">Tout autre code de retour indique une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="903f9-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="903f9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="903f9-109">Syntax</span></span>


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="903f9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="903f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="903f9-111">*Force* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="903f9-111">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-112">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="903f9-112">Type: **boolean**</span></span>

<span data-ttu-id="903f9-113">Indicateur qui, si la **valeur est true**, force la fermeture des applications malgré la non-enregistrement des données.</span><span class="sxs-lookup"><span data-stu-id="903f9-113">A flag which, if **True**, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="903f9-114">*Raison* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="903f9-114">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903f9-115">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="903f9-115">Type: **string**</span></span>

<span data-ttu-id="903f9-116">Raison de l’opération d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="903f9-116">The reason for the shutdown operation.</span></span> <span data-ttu-id="903f9-117">Il s’agit d’une chaîne définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="903f9-117">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="903f9-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="903f9-118">Return value</span></span>

<span data-ttu-id="903f9-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="903f9-119">Type: **uint32**</span></span>

<dl> <dt>

<span data-ttu-id="903f9-120">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="903f9-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="903f9-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-122">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="903f9-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-123">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="903f9-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-124">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="903f9-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-125">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="903f9-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-126">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="903f9-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-127">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="903f9-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-128">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="903f9-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-129">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="903f9-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-130">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="903f9-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-131">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="903f9-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-132">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="903f9-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-133">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="903f9-133">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-134">**Le système n’est pas prêt** (32780)</span><span class="sxs-lookup"><span data-stu-id="903f9-134">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-135">**L’ordinateur est verrouillé et ne peut pas être arrêté sans l’option force** (32781)</span><span class="sxs-lookup"><span data-stu-id="903f9-135">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="903f9-136">**Un arrêt système est en cours** (32782)</span><span class="sxs-lookup"><span data-stu-id="903f9-136">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="903f9-137">Notes</span><span class="sxs-lookup"><span data-stu-id="903f9-137">Remarks</span></span>

<span data-ttu-id="903f9-138">L’accès à la classe [**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="903f9-138">Access to the [**Msvm\_ShutdownComponent**](msvm-shutdowncomponent.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="903f9-139">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="903f9-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="903f9-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="903f9-140">Requirements</span></span>



| <span data-ttu-id="903f9-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="903f9-141">Requirement</span></span> | <span data-ttu-id="903f9-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="903f9-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="903f9-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="903f9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="903f9-144">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="903f9-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="903f9-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="903f9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="903f9-146">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="903f9-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="903f9-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="903f9-147">Namespace</span></span><br/>                | <span data-ttu-id="903f9-148">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="903f9-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="903f9-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="903f9-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="903f9-150"><dt>Winreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-150"><dt>Winreg.h</dt></span></span> </dl>                     |
| <span data-ttu-id="903f9-151">MOF</span><span class="sxs-lookup"><span data-stu-id="903f9-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="903f9-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="903f9-153">DLL</span><span class="sxs-lookup"><span data-stu-id="903f9-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="903f9-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="903f9-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="903f9-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="903f9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="903f9-156">**MSVM \_ ShutdownComponent**</span><span class="sxs-lookup"><span data-stu-id="903f9-156">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

