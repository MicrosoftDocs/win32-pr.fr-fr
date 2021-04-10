---
description: Ajoute des paramètres de fonctionnalité à la configuration d’un port commuté Ethernet.
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: Méthode AddFeatureSettings de la classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e3b46a26d3c67f5efce4944c8b2e874febced32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952055"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="60cab-103">Méthode AddFeatureSettings de la \_ classe VirtualEthernetSwitchManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="60cab-103">AddFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="60cab-104">Ajoute des paramètres de fonctionnalité à la configuration d’un port commuté Ethernet.</span><span class="sxs-lookup"><span data-stu-id="60cab-104">Adds feature settings to the configuration of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="60cab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60cab-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="60cab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60cab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60cab-107">*AffectedConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60cab-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60cab-108">Référence à une classe [**\_ dérivée CIM**](/previous-versions//cc136911(v=vs.85)) qui représente le port commuté Ethernet affecté ou la configuration du commutateur Ethernet.</span><span class="sxs-lookup"><span data-stu-id="60cab-108">A reference to a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) derived class that represents the affected Ethernet switch port or Ethernet switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="60cab-109">*FeatureSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60cab-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60cab-110">Tableau de chaînes qui contient une instance incorporée d’une classe dérivée de la classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) , qui décrit les paramètres de fonctionnalité à ajouter à la configuration du port commuté.</span><span class="sxs-lookup"><span data-stu-id="60cab-110">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the feature settings to be added to the switch port configuration.</span></span>

</dd> <dt>

<span data-ttu-id="60cab-111">*ResultingFeatureSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="60cab-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60cab-112">Tableau de références aux instances de la classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) qui représentent les paramètres de fonctionnalités ajoutés.</span><span class="sxs-lookup"><span data-stu-id="60cab-112">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="60cab-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="60cab-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60cab-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="60cab-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60cab-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60cab-115">Return value</span></span>

<span data-ttu-id="60cab-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="60cab-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="60cab-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="60cab-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60cab-118">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="60cab-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="60cab-119">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="60cab-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="60cab-120">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="60cab-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="60cab-121">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="60cab-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="60cab-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="60cab-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="60cab-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="60cab-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="60cab-124">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="60cab-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="60cab-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="60cab-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="60cab-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60cab-126">Requirements</span></span>



| <span data-ttu-id="60cab-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60cab-127">Requirement</span></span> | <span data-ttu-id="60cab-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="60cab-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60cab-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60cab-129">Minimum supported client</span></span><br/> | <span data-ttu-id="60cab-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60cab-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="60cab-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60cab-131">Minimum supported server</span></span><br/> | <span data-ttu-id="60cab-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60cab-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="60cab-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60cab-133">Namespace</span></span><br/>                | <span data-ttu-id="60cab-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="60cab-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="60cab-135">MOF</span><span class="sxs-lookup"><span data-stu-id="60cab-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60cab-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60cab-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60cab-137">DLL</span><span class="sxs-lookup"><span data-stu-id="60cab-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60cab-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60cab-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60cab-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60cab-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60cab-140">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="60cab-140">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="60cab-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="60cab-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="60cab-142">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="60cab-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

