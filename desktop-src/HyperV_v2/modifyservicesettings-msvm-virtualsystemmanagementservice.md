---
description: Modifie les données de paramètre pour le service.
ms.assetid: 1CA49922-894D-4AA1-B741-6A0DC9F5654E
title: Méthode ModifyServiceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e93d86c454de4f214c72a6ed95a414d184419c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867058"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="39005-103">Méthode ModifyServiceSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="39005-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="39005-104">Modifie les données de paramètre pour le service.</span><span class="sxs-lookup"><span data-stu-id="39005-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="39005-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39005-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="39005-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39005-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39005-107">*SettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39005-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39005-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="39005-108">Type: **string**</span></span>

<span data-ttu-id="39005-109">Une instance incorporée de la classe [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) qui contient les aspects modifiés du service existant.</span><span class="sxs-lookup"><span data-stu-id="39005-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="39005-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="39005-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39005-111">Type : **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="39005-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="39005-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="39005-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39005-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39005-113">Return value</span></span>

<span data-ttu-id="39005-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39005-114">Type: **uint32**</span></span>

<span data-ttu-id="39005-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="39005-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="39005-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="39005-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39005-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="39005-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="39005-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="39005-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="39005-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="39005-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="39005-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="39005-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="39005-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="39005-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="39005-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="39005-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="39005-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="39005-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="39005-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="39005-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="39005-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="39005-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="39005-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="39005-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="39005-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="39005-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="39005-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="39005-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="39005-129">Notes</span><span class="sxs-lookup"><span data-stu-id="39005-129">Remarks</span></span>

<span data-ttu-id="39005-130">L’accès à la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="39005-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="39005-131">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="39005-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="39005-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39005-132">Requirements</span></span>



| <span data-ttu-id="39005-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39005-133">Requirement</span></span> | <span data-ttu-id="39005-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="39005-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39005-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39005-135">Minimum supported client</span></span><br/> | <span data-ttu-id="39005-136">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39005-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="39005-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39005-137">Minimum supported server</span></span><br/> | <span data-ttu-id="39005-138">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39005-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39005-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="39005-139">Namespace</span></span><br/>                | <span data-ttu-id="39005-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="39005-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="39005-141">MOF</span><span class="sxs-lookup"><span data-stu-id="39005-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39005-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39005-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39005-143">DLL</span><span class="sxs-lookup"><span data-stu-id="39005-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39005-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39005-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39005-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39005-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39005-146">**ModifyServiceSettings (v1)**</span><span class="sxs-lookup"><span data-stu-id="39005-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="39005-147">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="39005-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="39005-148">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39005-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 

