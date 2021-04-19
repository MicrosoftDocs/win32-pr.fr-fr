---
description: Supprime les paramètres de fonctionnalités d’un port commuté Ethernet.
ms.assetid: 3d45259e-34e4-417b-a895-4926b0eaaf59
title: Méthode RemoveFeatureSettings de la classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 919e2b69e2a0ef215a522c601088cb7aa2976a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534627"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="81651-103">Méthode RemoveFeatureSettings de la \_ classe VirtualEthernetSwitchManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="81651-103">RemoveFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="81651-104">Supprime les paramètres de fonctionnalités d’un port commuté Ethernet.</span><span class="sxs-lookup"><span data-stu-id="81651-104">Removes feature settings from an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="81651-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81651-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_FeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="81651-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81651-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81651-107">*FeatureSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81651-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81651-108">Tableau de références aux instances de la classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) qui représentent les paramètres de fonctionnalité à supprimer.</span><span class="sxs-lookup"><span data-stu-id="81651-108">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="81651-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="81651-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81651-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="81651-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81651-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81651-111">Return value</span></span>

<span data-ttu-id="81651-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="81651-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="81651-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="81651-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81651-114">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="81651-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="81651-115">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="81651-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81651-116">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="81651-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81651-117">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="81651-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="81651-118">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="81651-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="81651-119">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="81651-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="81651-120">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="81651-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="81651-121">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="81651-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="81651-122">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="81651-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="81651-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81651-123">Requirements</span></span>



| <span data-ttu-id="81651-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81651-124">Requirement</span></span> | <span data-ttu-id="81651-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="81651-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81651-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81651-126">Minimum supported client</span></span><br/> | <span data-ttu-id="81651-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81651-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="81651-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81651-128">Minimum supported server</span></span><br/> | <span data-ttu-id="81651-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81651-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81651-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="81651-130">Namespace</span></span><br/>                | <span data-ttu-id="81651-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="81651-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="81651-132">MOF</span><span class="sxs-lookup"><span data-stu-id="81651-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81651-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81651-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81651-134">DLL</span><span class="sxs-lookup"><span data-stu-id="81651-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81651-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81651-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81651-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81651-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81651-137">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="81651-137">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="81651-138">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="81651-138">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="81651-139">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="81651-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

