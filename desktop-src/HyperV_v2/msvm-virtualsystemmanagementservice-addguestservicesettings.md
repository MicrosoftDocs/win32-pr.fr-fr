---
description: Ajoute des paramètres de service invité à une configuration de système virtuel.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Méthode AddGuestServiceSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5bcdfd8c159e92efe633c04e22af5bceb9d003e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525209"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="18c41-103">Méthode AddGuestServiceSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="18c41-103">AddGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="18c41-104">Ajoute des paramètres de service invité à une configuration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="18c41-104">Adds guest service settings to a virtual system configuration.</span></span>

<span data-ttu-id="18c41-105">En cas d’application à des parties d’une configuration de système virtuel « en cours », les services invités secondaires du système virtuel actif peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="18c41-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="18c41-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18c41-106">Syntax</span></span>


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="18c41-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18c41-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18c41-108">*AffectedConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18c41-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c41-109">Référence à un [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) qui décrit la configuration affectée.</span><span class="sxs-lookup"><span data-stu-id="18c41-109">Reference to a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that describes the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="18c41-110">*GuestServiceSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18c41-110">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18c41-111">Tableau contenant les paramètres du service invité.</span><span class="sxs-lookup"><span data-stu-id="18c41-111">An array containing the guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="18c41-112">*ResultingGuestServiceSettings* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18c41-112">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18c41-113">En cas de réussite, contient une référence à un [**\_ SettingData CIM**](cim-settingdata.md) qui décrit les paramètres de service invité résultants.</span><span class="sxs-lookup"><span data-stu-id="18c41-113">On success, contains a reference to a [**CIM\_SettingData**](cim-settingdata.md) that describes the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="18c41-114">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="18c41-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18c41-115">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18c41-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18c41-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18c41-116">Return value</span></span>

<span data-ttu-id="18c41-117">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="18c41-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="18c41-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="18c41-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18c41-119">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="18c41-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18c41-120">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="18c41-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18c41-121">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="18c41-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18c41-122">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="18c41-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18c41-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="18c41-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18c41-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="18c41-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="18c41-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="18c41-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="18c41-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="18c41-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="18c41-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18c41-127">Requirements</span></span>



| <span data-ttu-id="18c41-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18c41-128">Requirement</span></span> | <span data-ttu-id="18c41-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="18c41-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18c41-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18c41-130">Minimum supported client</span></span><br/> | <span data-ttu-id="18c41-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18c41-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="18c41-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18c41-132">Minimum supported server</span></span><br/> | <span data-ttu-id="18c41-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="18c41-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="18c41-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18c41-134">Namespace</span></span><br/>                | <span data-ttu-id="18c41-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="18c41-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="18c41-136">MOF</span><span class="sxs-lookup"><span data-stu-id="18c41-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18c41-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18c41-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18c41-138">DLL</span><span class="sxs-lookup"><span data-stu-id="18c41-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18c41-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18c41-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18c41-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18c41-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c41-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="18c41-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

