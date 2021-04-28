---
description: Méthode RemoveBootSourceSettings de la classe Msvm_VirtualSystemManagementService-supprime les paramètres de ressources virtuelles d’une configuration de système virtuel.
ms.assetid: 0deb7719-e605-4ba5-9bb2-037d0cafee24
title: Méthode RemoveBootSourceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5407e56b761dd545d20b89e0a28742f9c542b15a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109397"
---
# <a name="removebootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="bfa17-103">Méthode RemoveBootSourceSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="bfa17-103">RemoveBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="bfa17-104">Supprime les paramètres de ressources virtuelles d’une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="bfa17-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="bfa17-105">En cas d’application à des parties d’une configuration de système virtuel « en cours », les ressources d’effets secondaires du système virtuel actif peuvent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="bfa17-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa17-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfa17-106">Syntax</span></span>


```mof
uint32 RemoveBootSourceSettings(
  [in]  CIM_SettingData REF BootSourceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bfa17-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfa17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa17-108">*BootSourceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfa17-108">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa17-109">Référence à un tableau de [**\_ SettingData CIM**](cim-settingdata.md) qui décrit les paramètres de la source de démarrage à supprimer.</span><span class="sxs-lookup"><span data-stu-id="bfa17-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the boot source settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="bfa17-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bfa17-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa17-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bfa17-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa17-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bfa17-112">Return value</span></span>

<span data-ttu-id="bfa17-113">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bfa17-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bfa17-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="bfa17-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bfa17-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="bfa17-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bfa17-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="bfa17-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bfa17-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="bfa17-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bfa17-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="bfa17-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bfa17-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="bfa17-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bfa17-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="bfa17-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bfa17-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="bfa17-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bfa17-122">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="bfa17-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="bfa17-123">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="bfa17-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bfa17-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfa17-124">Requirements</span></span>



| <span data-ttu-id="bfa17-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfa17-125">Requirement</span></span> | <span data-ttu-id="bfa17-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfa17-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa17-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfa17-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa17-128">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfa17-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bfa17-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfa17-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa17-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bfa17-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bfa17-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bfa17-131">Namespace</span></span><br/>                | <span data-ttu-id="bfa17-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bfa17-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bfa17-133">MOF</span><span class="sxs-lookup"><span data-stu-id="bfa17-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfa17-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfa17-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfa17-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bfa17-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfa17-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bfa17-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bfa17-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfa17-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa17-138">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="bfa17-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

