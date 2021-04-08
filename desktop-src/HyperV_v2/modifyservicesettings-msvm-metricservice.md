---
description: Modifie les données de paramètre pour le service.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Méthode ModifyServiceSettings de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752221"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="d8a57-103">Méthode ModifyServiceSettings de la \_ classe MetricService MSVM</span><span class="sxs-lookup"><span data-stu-id="d8a57-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="d8a57-104">Modifie les données de paramètre pour le service.</span><span class="sxs-lookup"><span data-stu-id="d8a57-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a57-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8a57-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d8a57-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8a57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8a57-107">*SettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8a57-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a57-108">Contient une instance incorporée de la classe [**MSVM \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) qui contient les données de paramètre modifiées pour le service.</span><span class="sxs-lookup"><span data-stu-id="d8a57-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="d8a57-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8a57-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8a57-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d8a57-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8a57-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8a57-111">Return value</span></span>

<span data-ttu-id="d8a57-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8a57-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="d8a57-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d8a57-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="d8a57-114">Description</span><span class="sxs-lookup"><span data-stu-id="d8a57-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="d8a57-115"><dt>**Terminé sans erreur**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="d8a57-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="d8a57-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="d8a57-117"><dt>**Paramètres de méthode activés-travail démarré**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="d8a57-118">Paramètres de méthode vérifiés, tâche démarrée.</span><span class="sxs-lookup"><span data-stu-id="d8a57-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="d8a57-119"><dt>**Échec**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="d8a57-120">Échec.</span><span class="sxs-lookup"><span data-stu-id="d8a57-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d8a57-121"><dt>**Accès refusé**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="d8a57-122">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="d8a57-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="d8a57-123"><dt>**Non pris en charge**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="d8a57-124">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d8a57-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="d8a57-125">L' <dt>**État est inconnu**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="d8a57-126">L’état est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d8a57-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="d8a57-127"><dt>**Délai d’expiration**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="d8a57-128">Délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="d8a57-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="d8a57-129"><dt>**Paramètre non valide**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="d8a57-130">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="d8a57-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="d8a57-131">Le <dt>**système est en cours d’utilisation**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="d8a57-132">Le système est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d8a57-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="d8a57-133"><dt>**État non valide pour cette opération**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="d8a57-134">État non valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="d8a57-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="d8a57-135"><dt>**Type de données incorrect**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="d8a57-136">Type de données incorrect.</span><span class="sxs-lookup"><span data-stu-id="d8a57-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="d8a57-137">Le <dt>**système n’est pas disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="d8a57-138">Le système n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d8a57-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="d8a57-139"><dt>**Mémoire Insuffisante**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="d8a57-140">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d8a57-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="d8a57-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8a57-141">Requirements</span></span>



| <span data-ttu-id="d8a57-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8a57-142">Requirement</span></span> | <span data-ttu-id="d8a57-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8a57-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a57-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8a57-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d8a57-145">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8a57-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d8a57-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8a57-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d8a57-147">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8a57-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8a57-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8a57-148">Namespace</span></span><br/>                | <span data-ttu-id="d8a57-149">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d8a57-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d8a57-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d8a57-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8a57-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8a57-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d8a57-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8a57-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8a57-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8a57-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8a57-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a57-155">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="d8a57-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

