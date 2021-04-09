---
description: Définit l’état d’alimentation de l’appareil. L’utilisation de cette méthode est dépréciée. Utilisez plutôt la méthode SetPowerState dans la classe PowerManagementService associée.
ms.assetid: 2f53a8bd-18a8-45aa-92ad-68a33b6a42ab
title: Méthode SetPowerState de la classe CIM_LogicalDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a29f71806747e6d63f53618acd09d472ac8bdea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952523"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="ffabf-105">Méthode SetPowerState de la classe CIM_LogicalDevice (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ffabf-105">SetPowerState method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="ffabf-106">Définit l’état d’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ffabf-106">Sets the power state of the Device.</span></span> <span data-ttu-id="ffabf-107">L’utilisation de cette méthode est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="ffabf-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="ffabf-108">Utilisez plutôt la méthode **SetPowerState** dans la classe **PowerManagementService** associée.</span><span class="sxs-lookup"><span data-stu-id="ffabf-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffabf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffabf-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="ffabf-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffabf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffabf-111">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ffabf-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffabf-112">État d’alimentation à définir.</span><span class="sxs-lookup"><span data-stu-id="ffabf-112">The power state to set.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="ffabf-113">**Pleine puissance** (1)</span><span class="sxs-lookup"><span data-stu-id="ffabf-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ffabf-114">Économie **d’énergie-mode faible puissance** (2)</span><span class="sxs-lookup"><span data-stu-id="ffabf-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ffabf-115">Économie **d’énergie-veille** (3)</span><span class="sxs-lookup"><span data-stu-id="ffabf-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="ffabf-116">Économie **d’énergie-autres** (4)</span><span class="sxs-lookup"><span data-stu-id="ffabf-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ffabf-117">**Cycle d’alimentation** (5)</span><span class="sxs-lookup"><span data-stu-id="ffabf-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ffabf-118">**Mise hors tension** (6)</span><span class="sxs-lookup"><span data-stu-id="ffabf-118">**Power Off** (6)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ffabf-119">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ffabf-119">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffabf-120">L’heure indique quand l’état de l’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="ffabf-120">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffabf-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ffabf-121">Return value</span></span>

<span data-ttu-id="ffabf-122">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="ffabf-122">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffabf-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffabf-123">Requirements</span></span>



| <span data-ttu-id="ffabf-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffabf-124">Requirement</span></span> | <span data-ttu-id="ffabf-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffabf-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffabf-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffabf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ffabf-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ffabf-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ffabf-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffabf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ffabf-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ffabf-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ffabf-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ffabf-130">Namespace</span></span><br/>                | <span data-ttu-id="ffabf-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ffabf-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ffabf-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ffabf-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffabf-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffabf-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffabf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ffabf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffabf-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffabf-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffabf-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffabf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffabf-137">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ffabf-137">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




