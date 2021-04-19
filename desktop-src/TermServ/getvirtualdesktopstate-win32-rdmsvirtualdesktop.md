---
title: Méthode GetVirtualDesktopState de la classe Win32_RDMSVirtualDesktop
description: Récupère l’état du bureau virtuel.
ms.assetid: 176096ba-2b5f-428c-9216-02e3e97be64e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetVirtualDesktopState
- Services Bureau à distance de la méthode GetVirtualDesktopState, classe Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de la classe Services Bureau à distance, méthode GetVirtualDesktopState
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674e9646f0f41166fbfdc9e4ad35df697023329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509706"
---
# <a name="getvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="281f7-106">Méthode GetVirtualDesktopState de la \_ classe Win32 RDMSVirtualDesktop</span><span class="sxs-lookup"><span data-stu-id="281f7-106">GetVirtualDesktopState method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="281f7-107">Récupère l’état du bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="281f7-107">Retrieves the state of the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="281f7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="281f7-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopState(
  [out] uint32 VMState
);
```



## <a name="parameters"></a><span data-ttu-id="281f7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="281f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="281f7-110">*VMState* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="281f7-110">*VMState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="281f7-111">Reçoit une valeur qui indique l’état de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="281f7-111">Receives a value that indicates the state of the virtual machine.</span></span>

<span data-ttu-id="281f7-112">Ce paramètre peut être défini sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="281f7-112">This parameter can bet set to one of the following values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="281f7-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0 (par défaut))</span><span class="sxs-lookup"><span data-stu-id="281f7-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (Default))</span></span>


</dt> <dd>

<span data-ttu-id="281f7-114">L’état de la machine virtuelle n’a pas pu être déterminé.</span><span class="sxs-lookup"><span data-stu-id="281f7-114">The state of the virtual machine could not be determined.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="281f7-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="281f7-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="281f7-116">La machine virtuelle est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="281f7-116">The virtual machine is running.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="281f7-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="281f7-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="281f7-118">La machine virtuelle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="281f7-118">The virtual machine is turned off.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="281f7-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (32768)</span><span class="sxs-lookup"><span data-stu-id="281f7-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="281f7-120">L’ordinateur virtuel est en pause.</span><span class="sxs-lookup"><span data-stu-id="281f7-120">The virtual machine is paused.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="281f7-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendu** (32769)</span><span class="sxs-lookup"><span data-stu-id="281f7-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="281f7-122">L’ordinateur virtuel est dans un état enregistré.</span><span class="sxs-lookup"><span data-stu-id="281f7-122">The virtual machine is in a saved state.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="281f7-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** en cours (32770)</span><span class="sxs-lookup"><span data-stu-id="281f7-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="281f7-124">L’ordinateur virtuel est en cours de démarrage.</span><span class="sxs-lookup"><span data-stu-id="281f7-124">The virtual machine is starting.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="281f7-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Enregistrement** (32773)</span><span class="sxs-lookup"><span data-stu-id="281f7-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="281f7-126">L’ordinateur virtuel enregistre son état.</span><span class="sxs-lookup"><span data-stu-id="281f7-126">The virtual machine is saving its state.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="281f7-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (32774)</span><span class="sxs-lookup"><span data-stu-id="281f7-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (32774)</span></span>


</dt> <dd>

<span data-ttu-id="281f7-128">L’ordinateur virtuel est en arrêt.</span><span class="sxs-lookup"><span data-stu-id="281f7-128">The virtual machine is turning off.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="281f7-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Suspension** (32776)</span><span class="sxs-lookup"><span data-stu-id="281f7-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="281f7-130">L’ordinateur virtuel est en cours de suspension.</span><span class="sxs-lookup"><span data-stu-id="281f7-130">The virtual machine is pausing.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="281f7-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Reprise** (32777)</span><span class="sxs-lookup"><span data-stu-id="281f7-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="281f7-132">L’ordinateur virtuel reprend à l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="281f7-132">The virtual machine is resuming from a paused state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="281f7-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="281f7-133">Return value</span></span>

<span data-ttu-id="281f7-134">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="281f7-134">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="281f7-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="281f7-135">Requirements</span></span>



| <span data-ttu-id="281f7-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="281f7-136">Requirement</span></span> | <span data-ttu-id="281f7-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="281f7-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="281f7-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="281f7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="281f7-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="281f7-139">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="281f7-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="281f7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="281f7-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="281f7-141">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="281f7-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="281f7-142">Namespace</span></span><br/>                | <span data-ttu-id="281f7-143">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="281f7-143">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="281f7-144">MOF</span><span class="sxs-lookup"><span data-stu-id="281f7-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="281f7-145"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="281f7-145"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="281f7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="281f7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="281f7-147"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="281f7-147"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="281f7-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="281f7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281f7-149">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="281f7-149">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





