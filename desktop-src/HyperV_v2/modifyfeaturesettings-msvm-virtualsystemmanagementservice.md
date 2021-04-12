---
description: Modifie les paramètres de fonctionnalité actuels d’une connexion Ethernet d’ordinateur virtuel.
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: Méthode ModifyFeatureSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c376158008c5ad0e611d3a05c7e73d2e7d1b44cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319402"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a4ee3-103">Méthode ModifyFeatureSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="a4ee3-103">ModifyFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a4ee3-104">Modifie les paramètres de fonctionnalité actuels d’une connexion Ethernet d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="a4ee3-104">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4ee3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4ee3-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a4ee3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4ee3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4ee3-107">*FeatureSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4ee3-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ee3-108">Tableau de chaînes qui contient une instance incorporée d’une classe dérivée de la classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) , qui décrit les modifications apportées aux paramètres de fonctionnalité actuels d’une connexion Ethernet existante.</span><span class="sxs-lookup"><span data-stu-id="a4ee3-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that describes modifications to the current feature settings of an existing Ethernet connection.</span></span> <span data-ttu-id="a4ee3-109">La propriété **InstanceID** de chacune de ces instances identifie les paramètres de fonctionnalité à modifier.</span><span class="sxs-lookup"><span data-stu-id="a4ee3-109">The **InstanceID** property of each of these instances identifies the feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="a4ee3-110">*ResultingFeatureSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a4ee3-110">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ee3-111">Tableau de références aux instances de la classe [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) qui représentent les paramètres de fonctionnalités modifiés.</span><span class="sxs-lookup"><span data-stu-id="a4ee3-111">An array of references to instances of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="a4ee3-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a4ee3-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ee3-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a4ee3-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4ee3-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4ee3-114">Return value</span></span>

<span data-ttu-id="a4ee3-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a4ee3-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a4ee3-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-118">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-120">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-121">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-122">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a4ee3-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a4ee3-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a4ee3-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4ee3-127">Requirements</span></span>



| <span data-ttu-id="a4ee3-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4ee3-128">Requirement</span></span> | <span data-ttu-id="a4ee3-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4ee3-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ee3-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4ee3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a4ee3-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4ee3-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a4ee3-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4ee3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a4ee3-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4ee3-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4ee3-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a4ee3-134">Namespace</span></span><br/>                | <span data-ttu-id="a4ee3-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a4ee3-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a4ee3-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a4ee3-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4ee3-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4ee3-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4ee3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a4ee3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4ee3-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4ee3-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a4ee3-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4ee3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4ee3-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a4ee3-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

