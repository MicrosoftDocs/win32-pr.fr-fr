---
description: Modifie les paramètres du commutateur virtuel.
ms.assetid: 8d323578-990f-483c-8515-8a21479767b1
title: Méthode ModifySystemSettings de la classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3512debfd6d49e3c09cb8a508a7f0d748ab128e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534011"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="0e967-103">Méthode ModifySystemSettings de la \_ classe VirtualEthernetSwitchManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="0e967-103">ModifySystemSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="0e967-104">Modifie les paramètres du commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e967-104">Modifies virtual switch settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e967-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e967-105">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0e967-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e967-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e967-107">*SystemSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e967-107">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e967-108">Une instance incorporée de la classe [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) qui contient les aspects modifiés du commutateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e967-108">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that contains the modified aspects of the virtual switch.</span></span> <span data-ttu-id="0e967-109">La propriété **InstanceID** identifie le paramètre de commutateur virtuel à modifier.</span><span class="sxs-lookup"><span data-stu-id="0e967-109">The **InstanceID** property identifies the virtual switch setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="0e967-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0e967-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e967-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e967-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e967-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e967-112">Return value</span></span>

<span data-ttu-id="0e967-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e967-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0e967-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="0e967-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="0e967-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="0e967-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="0e967-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="0e967-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="0e967-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-120">**Paramètres incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="0e967-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0e967-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-122">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="0e967-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-123">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0e967-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0e967-124">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0e967-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0e967-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e967-125">Requirements</span></span>



| <span data-ttu-id="0e967-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e967-126">Requirement</span></span> | <span data-ttu-id="0e967-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e967-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e967-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e967-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0e967-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e967-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0e967-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e967-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0e967-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e967-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e967-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e967-132">Namespace</span></span><br/>                | <span data-ttu-id="0e967-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e967-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0e967-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0e967-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e967-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e967-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e967-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0e967-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e967-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e967-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e967-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e967-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e967-139">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="0e967-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

