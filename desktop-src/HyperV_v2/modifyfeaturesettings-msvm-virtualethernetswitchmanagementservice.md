---
description: Modifie les paramètres de fonctionnalité d’un port commuté Ethernet.
ms.assetid: 8c21a932-fffb-40fd-9166-d7e351329217
title: Méthode ModifyFeatureSettings de la classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0bee92019f9457a42a0c87ab619f7de1f7d203ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536703"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="5b160-103">Méthode ModifyFeatureSettings de la \_ classe VirtualEthernetSwitchManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="5b160-103">ModifyFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="5b160-104">Modifie les paramètres de fonctionnalité d’un port commuté Ethernet.</span><span class="sxs-lookup"><span data-stu-id="5b160-104">Modifies the feature settings of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b160-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b160-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5b160-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b160-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b160-107">*FeatureSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b160-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b160-108">Tableau de chaînes qui contient une instance incorporée d’une classe dérivée de la classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) , qui décrit les paramètres de la fonctionnalité de port de commutateur à modifier.</span><span class="sxs-lookup"><span data-stu-id="5b160-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the switch port feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="5b160-109">*ResultingFeatureSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5b160-109">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b160-110">Tableau de références aux instances de la classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) qui représentent les paramètres de fonctionnalités modifiés.</span><span class="sxs-lookup"><span data-stu-id="5b160-110">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="5b160-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5b160-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b160-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5b160-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b160-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b160-113">Return value</span></span>

<span data-ttu-id="5b160-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5b160-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5b160-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="5b160-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-116">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="5b160-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-117">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="5b160-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-118">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="5b160-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-119">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="5b160-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-120">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="5b160-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-121">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="5b160-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5b160-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="5b160-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-124">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5b160-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5b160-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5b160-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5b160-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b160-126">Requirements</span></span>



| <span data-ttu-id="5b160-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b160-127">Requirement</span></span> | <span data-ttu-id="5b160-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b160-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b160-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b160-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5b160-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b160-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5b160-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b160-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5b160-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b160-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5b160-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5b160-133">Namespace</span></span><br/>                | <span data-ttu-id="5b160-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5b160-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5b160-135">MOF</span><span class="sxs-lookup"><span data-stu-id="5b160-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b160-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b160-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b160-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5b160-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b160-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b160-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b160-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b160-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b160-140">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="5b160-140">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="5b160-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="5b160-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="5b160-142">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="5b160-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

