---
description: Modifie les paramètres du service invité.
ms.assetid: a308aa59-bd43-4dd5-a690-c435102e8043
title: Méthode ModifyGuestServiceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bc0af24346c445022ba3f8725ea6102c61dc9c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862062"
---
# <a name="modifyguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="9e892-103">Méthode ModifyGuestServiceSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="9e892-103">ModifyGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="9e892-104">Modifie les paramètres du service invité.</span><span class="sxs-lookup"><span data-stu-id="9e892-104">Modifies guest service settings.</span></span>

<span data-ttu-id="9e892-105">En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="9e892-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e892-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e892-106">Syntax</span></span>


```mof
uint32 ModifyGuestServiceSettings(
  [in]  string              GuestServiceSettings[],
  [out] CIM_SettingData REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9e892-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e892-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e892-108">*GuestServiceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9e892-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e892-109">Tableau qui contient les nouveaux paramètres de service invité.</span><span class="sxs-lookup"><span data-stu-id="9e892-109">An array that contains the new guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="9e892-110">*ResultingGuestServiceSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9e892-110">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e892-111">En cas de réussite, contiains un tableau de [**\_ SettingData CIM**](cim-settingdata.md) qui référence les paramètres de service invité résultants.</span><span class="sxs-lookup"><span data-stu-id="9e892-111">On success, contiains an array of [**CIM\_SettingData**](cim-settingdata.md) that reference the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="9e892-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9e892-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e892-113">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9e892-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e892-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e892-114">Return value</span></span>

<span data-ttu-id="9e892-115">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e892-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="9e892-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="9e892-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="9e892-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-118">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="9e892-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="9e892-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-120">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="9e892-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-121">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="9e892-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-122">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="9e892-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="9e892-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="9e892-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="9e892-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9e892-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9e892-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9e892-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e892-127">Requirements</span></span>



| <span data-ttu-id="9e892-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e892-128">Requirement</span></span> | <span data-ttu-id="9e892-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e892-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e892-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e892-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9e892-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e892-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9e892-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e892-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9e892-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9e892-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9e892-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9e892-134">Namespace</span></span><br/>                | <span data-ttu-id="9e892-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9e892-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9e892-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9e892-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e892-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e892-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e892-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9e892-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e892-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9e892-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9e892-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e892-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e892-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="9e892-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

