---
description: Supprime les paramètres de service invité d’une configuration de système virtuel.
ms.assetid: 33e55d74-adfd-4174-8f05-14e797a33806
title: Méthode RemoveGuestServiceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0aee1f8f9d729c093bff2a580e054d93fa7fc033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533589"
---
# <a name="removeguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6c1b6-103">Méthode RemoveGuestServiceSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="6c1b6-103">RemoveGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6c1b6-104">Supprime les paramètres de service invité d’une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="6c1b6-104">Removes guest service settings from a virtual system configuration.</span></span>

<span data-ttu-id="6c1b6-105">En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="6c1b6-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c1b6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c1b6-106">Syntax</span></span>


```mof
uint32 RemoveGuestServiceSettings(
  [in]  CIM_SettingData REF GuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6c1b6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c1b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c1b6-108">*GuestServiceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c1b6-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1b6-109">Référence à un tableau de [**\_ SettingData CIM**](cim-settingdata.md) qui décrit le paramètre de service invité à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6c1b6-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the guest service setting to remove.</span></span>

</dd> <dt>

<span data-ttu-id="6c1b6-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6c1b6-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1b6-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6c1b6-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c1b6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c1b6-112">Return value</span></span>

<span data-ttu-id="6c1b6-113">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6c1b6-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6c1b6-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6c1b6-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6c1b6-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6c1b6-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6c1b6-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6c1b6-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6c1b6-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6c1b6-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6c1b6-122">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6c1b6-123">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6c1b6-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6c1b6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c1b6-124">Requirements</span></span>



| <span data-ttu-id="6c1b6-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c1b6-125">Requirement</span></span> | <span data-ttu-id="6c1b6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c1b6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c1b6-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c1b6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6c1b6-128">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c1b6-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6c1b6-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c1b6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6c1b6-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6c1b6-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6c1b6-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6c1b6-131">Namespace</span></span><br/>                | <span data-ttu-id="6c1b6-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6c1b6-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6c1b6-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6c1b6-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c1b6-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c1b6-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c1b6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6c1b6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c1b6-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c1b6-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c1b6-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c1b6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c1b6-138">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6c1b6-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

