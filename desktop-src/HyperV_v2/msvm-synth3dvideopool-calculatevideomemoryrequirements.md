---
description: Calcule la quantité de mémoire vidéo requise pour une machine virtuelle RemoteFX.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Méthode CalculateVideoMemoryRequirements de la classe Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113630"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a><span data-ttu-id="d8743-103">Méthode CalculateVideoMemoryRequirements de la \_ classe Synth3dVideoPool MSVM</span><span class="sxs-lookup"><span data-stu-id="d8743-103">CalculateVideoMemoryRequirements method of the Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="d8743-104">Calcule la quantité de mémoire vidéo requise pour une machine virtuelle RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="d8743-104">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8743-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8743-105">Syntax</span></span>


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a><span data-ttu-id="d8743-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8743-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8743-107">*monitorResolution* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8743-107">*monitorResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8743-108">Résolution maximale de l’écran pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d8743-108">The maximum monitor resolution for the virtual machine.</span></span> <span data-ttu-id="d8743-109">Il doit s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8743-109">This must be one of the following values.</span></span>



| <span data-ttu-id="d8743-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8743-110">Value</span></span>                                                                        | <span data-ttu-id="d8743-111">Signification</span><span class="sxs-lookup"><span data-stu-id="d8743-111">Meaning</span></span>                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="d8743-112"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-112"><dt>0</dt></span></span> </dl> | <span data-ttu-id="d8743-113">La résolution maximale est de 1024 768.</span><span class="sxs-lookup"><span data-stu-id="d8743-113">The maximum resolution is 1024   768.</span></span><br/>  |
| <dl> <span data-ttu-id="d8743-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-114"><dt>1</dt></span></span> </dl> | <span data-ttu-id="d8743-115">La résolution maximale est de 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="d8743-115">The maximum resolution is 1280   1024.</span></span><br/> |
| <dl> <span data-ttu-id="d8743-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-116"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d8743-117">La résolution maximale est de 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="d8743-117">The maximum resolution is 1600   1200.</span></span><br/> |
| <dl> <span data-ttu-id="d8743-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d8743-119">La résolution maximale est de 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="d8743-119">The maximum resolution is 1920   1200.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d8743-120">*numberOfMonitors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8743-120">*numberOfMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8743-121">Nombre maximal d’analyses pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d8743-121">The maximum number of monitors for the virtual machine.</span></span> <span data-ttu-id="d8743-122">Le nombre minimal d’analyses est de 1 et la valeur maximale dépend de la résolution d’écran maximale.</span><span class="sxs-lookup"><span data-stu-id="d8743-122">The minimum number of monitors is one and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="d8743-123">Le tableau suivant définit le nombre maximal d’analyses autorisées pour différentes résolutions.</span><span class="sxs-lookup"><span data-stu-id="d8743-123">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="d8743-124">Résolution</span><span class="sxs-lookup"><span data-stu-id="d8743-124">Resolution</span></span>             | <span data-ttu-id="d8743-125">Nombre maximal d’écrans</span><span class="sxs-lookup"><span data-stu-id="d8743-125">Maximum monitors</span></span> |
|------------------------|------------------|
| <span data-ttu-id="d8743-126">1024 768</span><span class="sxs-lookup"><span data-stu-id="d8743-126">1024   768</span></span><br/>  | <span data-ttu-id="d8743-127">4</span><span class="sxs-lookup"><span data-stu-id="d8743-127">4</span></span><br/>     |
| <span data-ttu-id="d8743-128">1280 1024</span><span class="sxs-lookup"><span data-stu-id="d8743-128">1280   1024</span></span><br/> | <span data-ttu-id="d8743-129">4</span><span class="sxs-lookup"><span data-stu-id="d8743-129">4</span></span><br/>     |
| <span data-ttu-id="d8743-130">1600 1200</span><span class="sxs-lookup"><span data-stu-id="d8743-130">1600   1200</span></span><br/> | <span data-ttu-id="d8743-131">3</span><span class="sxs-lookup"><span data-stu-id="d8743-131">3</span></span><br/>     |
| <span data-ttu-id="d8743-132">1920 1200</span><span class="sxs-lookup"><span data-stu-id="d8743-132">1920   1200</span></span><br/> | <span data-ttu-id="d8743-133">2</span><span class="sxs-lookup"><span data-stu-id="d8743-133">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="d8743-134">*requiredVideoMemory* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8743-134">*requiredVideoMemory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8743-135">Reçoit la quantité de mémoire vidéo requise, en octets.</span><span class="sxs-lookup"><span data-stu-id="d8743-135">Receives the required amount of video memory, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8743-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8743-136">Return value</span></span>

<span data-ttu-id="d8743-137">Retourne un code d’État, qui peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8743-137">Returns a status code, which can be one of the following values.</span></span>



| <span data-ttu-id="d8743-138">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d8743-138">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="d8743-139">Description</span><span class="sxs-lookup"><span data-stu-id="d8743-139">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="d8743-140"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-140"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="d8743-141">Vendu.</span><span class="sxs-lookup"><span data-stu-id="d8743-141">Successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="d8743-142"><dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="d8743-143">Travail démarré.</span><span class="sxs-lookup"><span data-stu-id="d8743-143">Job started.</span></span><br/>                               |
| <dl> <span data-ttu-id="d8743-144"><dt>**Échec**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-144"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="d8743-145">Échec.</span><span class="sxs-lookup"><span data-stu-id="d8743-145">Failed.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d8743-146"><dt>**Accès refusé**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-146"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="d8743-147">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="d8743-147">Access denied.</span></span><br/>                             |
| <dl> <span data-ttu-id="d8743-148"><dt>**Non pris en charge**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-148"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="d8743-149">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d8743-149">Not supported.</span></span><br/>                             |
| <dl> <span data-ttu-id="d8743-150">L' <dt>**État est inconnu**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-150"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="d8743-151">L’état est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d8743-151">Status is unknown.</span></span><br/>                         |
| <dl> <span data-ttu-id="d8743-152"><dt>**Délai d’expiration**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-152"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="d8743-153">Délai d’expiration.</span><span class="sxs-lookup"><span data-stu-id="d8743-153">Timeout.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d8743-154"><dt>**Paramètre non valide**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-154"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="d8743-155">Un paramètre n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d8743-155">A parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="d8743-156">Le <dt>**système est en cours d’utilisation**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-156"><dt>**System is in used**</dt> <dt>32774</dt></span></span> </dl>                      | <span data-ttu-id="d8743-157">Le système est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d8743-157">System is in use.</span></span><br/>                          |
| <dl> <span data-ttu-id="d8743-158"><dt>**État non valide pour cette opération**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-158"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="d8743-159">L’État n’est pas valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="d8743-159">The state is not valid for this operation.</span></span><br/> |
| <dl> <span data-ttu-id="d8743-160"><dt>**Type de données incorrect**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-160"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="d8743-161">Type de données incorrect.</span><span class="sxs-lookup"><span data-stu-id="d8743-161">Incorrect data type.</span></span><br/>                       |
| <dl> <span data-ttu-id="d8743-162">Le <dt>**système n’est pas disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-162"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="d8743-163">Le système n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d8743-163">System is not available.</span></span><br/>                   |
| <dl> <span data-ttu-id="d8743-164"><dt>**Mémoire Insuffisante**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-164"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="d8743-165">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d8743-165">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="d8743-166">Notes</span><span class="sxs-lookup"><span data-stu-id="d8743-166">Remarks</span></span>

<span data-ttu-id="d8743-167">Cette méthode est généralement appelée sur le système hôte pour déterminer si l’ordinateur hôte dispose de suffisamment de mémoire vidéo pour héberger une machine virtuelle RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="d8743-167">This method is typically called on the host system to determine if the host has enough available video memory to host a RemoteFX virtual machine.</span></span> <span data-ttu-id="d8743-168">Pour ce faire, vous comparez la quantité de mémoire vidéo calculée par cette méthode avec la propriété [**MSVM \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) pour déterminer si l’ordinateur hôte dispose de suffisamment de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="d8743-168">To do this, you compare the amount of video memory calculated by this method with the [**Msvm\_PhysicalGPUInfo.AvailableVideoMemory**](msvm-physicalgpuinfo.md) property to determine if the host machine has enough available video memory.</span></span> <span data-ttu-id="d8743-169">Vous pouvez utiliser ces informations pour déterminer si une machine virtuelle peut être déplacée vers le système hôte.</span><span class="sxs-lookup"><span data-stu-id="d8743-169">You can use this information to determine if a virtual machine can be moved to the host system.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8743-170">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8743-170">Requirements</span></span>



| <span data-ttu-id="d8743-171">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8743-171">Requirement</span></span> | <span data-ttu-id="d8743-172">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8743-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8743-173">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8743-173">Minimum supported client</span></span><br/> | <span data-ttu-id="d8743-174">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8743-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d8743-175">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8743-175">Minimum supported server</span></span><br/> | <span data-ttu-id="d8743-176">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8743-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8743-177">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8743-177">Namespace</span></span><br/>                | <span data-ttu-id="d8743-178">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d8743-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d8743-179">MOF</span><span class="sxs-lookup"><span data-stu-id="d8743-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8743-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8743-181">DLL</span><span class="sxs-lookup"><span data-stu-id="d8743-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8743-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8743-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8743-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8743-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8743-184">**MSVM \_ PhysicalGPUInfo**</span><span class="sxs-lookup"><span data-stu-id="d8743-184">**Msvm\_PhysicalGPUInfo**</span></span>](msvm-physicalgpuinfo.md)
</dt> <dt>

[<span data-ttu-id="d8743-185">**MSVM \_ Synth3dVideoPool**</span><span class="sxs-lookup"><span data-stu-id="d8743-185">**Msvm\_Synth3dVideoPool**</span></span>](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




