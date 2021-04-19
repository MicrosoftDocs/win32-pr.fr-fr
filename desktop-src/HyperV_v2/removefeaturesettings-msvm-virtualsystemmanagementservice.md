---
description: Supprime les paramètres de fonctionnalité d’une connexion Ethernet d’ordinateur virtuel.
ms.assetid: 457056d0-7e69-47e4-8744-0136a1816f4a
title: Méthode RemoveFeatureSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c29151f6544d7eb803ec72ee49e455556d8b2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520037"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6bbc6-103">Méthode RemoveFeatureSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="6bbc6-103">RemoveFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6bbc6-104">Supprime les paramètres de fonctionnalité d’une connexion Ethernet d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6bbc6-104">Removes feature settings from a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bbc6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bbc6-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_EthernetSwitchPortFeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6bbc6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bbc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bbc6-107">*FeatureSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6bbc6-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbc6-108">Tableau de chaînes qui contient une instance incorporée d’une classe dérivée de la classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) , qui définit les paramètres de fonctionnalité à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6bbc6-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that defines the feature settings to be removed.</span></span> <span data-ttu-id="6bbc6-109">La propriété **InstanceID** de chacune de ces instances identifie les paramètres de fonctionnalité à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6bbc6-109">The **InstanceID** property of each of these instances identifies the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="6bbc6-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6bbc6-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbc6-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6bbc6-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bbc6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6bbc6-112">Return value</span></span>

<span data-ttu-id="6bbc6-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6bbc6-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6bbc6-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6bbc6-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6bbc6-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6bbc6-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6bbc6-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6bbc6-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6bbc6-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6bbc6-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6bbc6-122">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6bbc6-123">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6bbc6-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6bbc6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bbc6-124">Requirements</span></span>



| <span data-ttu-id="6bbc6-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bbc6-125">Requirement</span></span> | <span data-ttu-id="6bbc6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bbc6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbc6-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bbc6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6bbc6-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bbc6-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6bbc6-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6bbc6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6bbc6-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6bbc6-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6bbc6-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6bbc6-131">Namespace</span></span><br/>                | <span data-ttu-id="6bbc6-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6bbc6-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6bbc6-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6bbc6-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bbc6-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bbc6-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bbc6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6bbc6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bbc6-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6bbc6-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6bbc6-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bbc6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bbc6-138">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6bbc6-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

