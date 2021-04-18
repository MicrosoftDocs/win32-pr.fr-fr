---
description: Modifie les paramètres de l’ordinateur virtuel.
ms.assetid: 3266bd0d-398b-4d3b-9248-e29c069aab11
title: Méthode ModifySystemSettings de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4e6bf40b3dd206affcdc014e98554bfa8f88b4c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536525"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="20beb-103">Méthode ModifySystemSettings de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="20beb-103">ModifySystemSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="20beb-104">Modifie les paramètres de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="20beb-104">Modifies virtual machine settings.</span></span> <span data-ttu-id="20beb-105">En cas d’application aux paramètres système d’une configuration d’ordinateur virtuel « en cours », l’instance de machine virtuelle peut être modifiée en tant qu’effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="20beb-105">When applied to the system settings of a "current" virtual machine configuration, as a side effect the virtual machine instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="20beb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20beb-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="20beb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20beb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20beb-108">*SystemSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20beb-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20beb-109">Une instance incorporée de la classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui contient les aspects modifiés de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="20beb-109">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that contains the modified aspects of the virtual machine.</span></span> <span data-ttu-id="20beb-110">La propriété **InstanceID** identifie le paramètre d’ordinateur virtuel à modifier.</span><span class="sxs-lookup"><span data-stu-id="20beb-110">The **InstanceID** property identifies the virtual machine setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="20beb-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20beb-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20beb-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="20beb-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20beb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20beb-113">Return value</span></span>

<span data-ttu-id="20beb-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="20beb-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="20beb-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="20beb-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-116">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="20beb-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-117">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="20beb-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-118">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="20beb-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-119">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="20beb-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-120">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="20beb-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-121">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="20beb-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="20beb-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="20beb-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-124">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="20beb-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="20beb-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="20beb-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="20beb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20beb-126">Requirements</span></span>



| <span data-ttu-id="20beb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20beb-127">Requirement</span></span> | <span data-ttu-id="20beb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="20beb-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20beb-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20beb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="20beb-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20beb-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="20beb-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20beb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="20beb-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20beb-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20beb-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="20beb-133">Namespace</span></span><br/>                | <span data-ttu-id="20beb-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="20beb-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="20beb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="20beb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20beb-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20beb-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20beb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="20beb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20beb-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20beb-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20beb-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20beb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20beb-140">**ModifyVirtualSystem (v1)**</span><span class="sxs-lookup"><span data-stu-id="20beb-140">**ModifyVirtualSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystem-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="20beb-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="20beb-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

