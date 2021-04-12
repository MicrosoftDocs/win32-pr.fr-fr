---
description: Ajoute des paramètres de fonctionnalités Ethernet à la configuration d’une connexion Ethernet d’ordinateur virtuel.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Méthode AddFeatureSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319201"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="68641-103">Méthode AddFeatureSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="68641-103">AddFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="68641-104">Ajoute des paramètres de fonctionnalités Ethernet à la configuration d’une connexion Ethernet d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="68641-104">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="68641-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68641-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="68641-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68641-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68641-107">*AffectedConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68641-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68641-108">Référence à une instance de la classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) qui représente la connexion Ethernet affectée.</span><span class="sxs-lookup"><span data-stu-id="68641-108">Reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the affected Ethernet connection.</span></span>

</dd> <dt>

<span data-ttu-id="68641-109">*FeatureSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="68641-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68641-110">Tableau de chaînes qui contient une instance incorporée de la classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) qui décrit les paramètres de fonctionnalité à ajouter à la configuration de la connexion.</span><span class="sxs-lookup"><span data-stu-id="68641-110">An array of strings that contain one embedded instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that describes the feature settings to be added to the connection configuration.</span></span>

</dd> <dt>

<span data-ttu-id="68641-111">*ResultingFeatureSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="68641-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68641-112">Tableau de références aux instances de la classe [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) qui représente les paramètres de fonctionnalités ajoutés.</span><span class="sxs-lookup"><span data-stu-id="68641-112">An array of references to instances of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="68641-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="68641-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68641-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68641-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68641-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68641-115">Return value</span></span>

<span data-ttu-id="68641-116">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="68641-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="68641-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="68641-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="68641-118">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="68641-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="68641-119">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="68641-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="68641-120">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="68641-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="68641-121">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="68641-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="68641-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="68641-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="68641-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="68641-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="68641-124">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="68641-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="68641-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="68641-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="68641-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68641-126">Requirements</span></span>



| <span data-ttu-id="68641-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68641-127">Requirement</span></span> | <span data-ttu-id="68641-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="68641-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68641-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68641-129">Minimum supported client</span></span><br/> | <span data-ttu-id="68641-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68641-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="68641-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68641-131">Minimum supported server</span></span><br/> | <span data-ttu-id="68641-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68641-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68641-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68641-133">Namespace</span></span><br/>                | <span data-ttu-id="68641-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="68641-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="68641-135">MOF</span><span class="sxs-lookup"><span data-stu-id="68641-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68641-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68641-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="68641-137">DLL</span><span class="sxs-lookup"><span data-stu-id="68641-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68641-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68641-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="68641-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68641-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68641-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="68641-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

