---
description: Définit l’état d’alimentation de l’ordinateur. L’utilisation de cette méthode est dépréciée. Utilisez plutôt la méthode SetPowerState dans la classe PowerManagementService associée.
ms.assetid: c2196f35-f687-4d82-a068-f8499f77473a
title: Méthode SetPowerState de la classe CIM_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c9e264e8ec62c1e49e92226d1abc8ac902c0b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034658"
---
# <a name="setpowerstate-method-of-the-cim_computersystem-class"></a><span data-ttu-id="e0289-105">Méthode SetPowerState de la \_ classe ComputerSystem CIM</span><span class="sxs-lookup"><span data-stu-id="e0289-105">SetPowerState method of the CIM\_ComputerSystem class</span></span>

<span data-ttu-id="e0289-106">Définit l’état d’alimentation de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e0289-106">Sets the power state of the computer.</span></span> <span data-ttu-id="e0289-107">L’utilisation de cette méthode est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="e0289-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="e0289-108">Utilisez plutôt la méthode **SetPowerState** dans la classe **PowerManagementService** associée.</span><span class="sxs-lookup"><span data-stu-id="e0289-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0289-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0289-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint32   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="e0289-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0289-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0289-111">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e0289-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0289-112">État souhaité pour le système informatique.</span><span class="sxs-lookup"><span data-stu-id="e0289-112">The desired state for the computer system.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="e0289-113">**Pleine puissance** (1)</span><span class="sxs-lookup"><span data-stu-id="e0289-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e0289-114">Économie **d’énergie-mode faible puissance** (2)</span><span class="sxs-lookup"><span data-stu-id="e0289-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e0289-115">Économie **d’énergie-veille** (3)</span><span class="sxs-lookup"><span data-stu-id="e0289-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="e0289-116">Économie **d’énergie-autres** (4)</span><span class="sxs-lookup"><span data-stu-id="e0289-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e0289-117">**Cycle d’alimentation** (5)</span><span class="sxs-lookup"><span data-stu-id="e0289-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e0289-118">**Mise hors tension** (6)</span><span class="sxs-lookup"><span data-stu-id="e0289-118">**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="e0289-119">**Mise en veille prolongée** (7)</span><span class="sxs-lookup"><span data-stu-id="e0289-119">**Hibernate** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="e0289-120">**Désactivé** (8)</span><span class="sxs-lookup"><span data-stu-id="e0289-120">**Soft Off** (8)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e0289-121">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e0289-121">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0289-122">L’heure indique quand l’état de l’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="e0289-122">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0289-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0289-123">Requirements</span></span>



| <span data-ttu-id="e0289-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0289-124">Requirement</span></span> | <span data-ttu-id="e0289-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0289-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0289-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0289-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e0289-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e0289-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e0289-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0289-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e0289-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e0289-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e0289-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e0289-130">Namespace</span></span><br/>                | <span data-ttu-id="e0289-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e0289-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e0289-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e0289-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0289-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0289-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0289-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e0289-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0289-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e0289-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e0289-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0289-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0289-137">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="e0289-137">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




