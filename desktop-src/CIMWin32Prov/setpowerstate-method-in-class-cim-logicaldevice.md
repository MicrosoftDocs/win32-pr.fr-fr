---
description: La méthode SetPowerState de la \_ classe LOGICALDEVICE CIM définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.
ms.assetid: 0d9678e0-a956-45d3-ac41-5c1604478fd7
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe CIM_LogicalDevice (fournisseurs WMI CIMWin32)
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
- CIMWin32.dll
ms.openlocfilehash: dd258a4372c16a7f98f2fe3ea8b84bbfef44f69e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515361"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="ef373-103">Méthode SetPowerState de la classe CIM_LogicalDevice (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ef373-103">SetPowerState method of the CIM_LogicalDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ef373-104">La méthode **SetPowerState** de la \_ classe LogicalDevice CIM définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="ef373-104">The **SetPowerState** method of the CIM\_LogicalDevice class sets the desired power state for a logical device and when a device should be put into that state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef373-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ef373-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ef373-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ef373-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ef373-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef373-107">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="ef373-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef373-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef373-109">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef373-109">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef373-110">Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour cet appareil logique.</span><span class="sxs-lookup"><span data-stu-id="ef373-110">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="ef373-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Pleine puissance** (1)</span><span class="sxs-lookup"><span data-stu-id="ef373-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ef373-112">Toute la puissance.</span><span class="sxs-lookup"><span data-stu-id="ef373-112">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ef373-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (2)</span><span class="sxs-lookup"><span data-stu-id="ef373-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ef373-114">Économie d’énergie en mode faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="ef373-114">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ef373-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (3)</span><span class="sxs-lookup"><span data-stu-id="ef373-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ef373-116">Économie d’énergie en veille.</span><span class="sxs-lookup"><span data-stu-id="ef373-116">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="ef373-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>Économie **d’énergie-autres** (4)</span><span class="sxs-lookup"><span data-stu-id="ef373-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ef373-118">Économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="ef373-118">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ef373-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (5)</span><span class="sxs-lookup"><span data-stu-id="ef373-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ef373-120">Cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="ef373-120">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ef373-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (6)</span><span class="sxs-lookup"><span data-stu-id="ef373-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ef373-122">Mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="ef373-122">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ef373-123">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef373-123">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef373-124">Spécifie quand l’état d’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="ef373-124">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="ef373-125">Lorsque le paramètre *PowerState* est égal à 5 (« Power cycle »), le paramètre *Time* indique quand l’appareil doit se rallumer.</span><span class="sxs-lookup"><span data-stu-id="ef373-125">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="ef373-126">La mise hors tension est immédiate.</span><span class="sxs-lookup"><span data-stu-id="ef373-126">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef373-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef373-127">Return value</span></span>

<span data-ttu-id="ef373-128">Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ef373-128">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef373-129">Notes</span><span class="sxs-lookup"><span data-stu-id="ef373-129">Remarks</span></span>

<span data-ttu-id="ef373-130">Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="ef373-130">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="ef373-131">Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="ef373-131">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="ef373-132">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ef373-132">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ef373-133">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="ef373-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ef373-134">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ef373-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ef373-135">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ef373-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ef373-136">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ef373-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef373-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef373-137">Requirements</span></span>



| <span data-ttu-id="ef373-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef373-138">Requirement</span></span> | <span data-ttu-id="ef373-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef373-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef373-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef373-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ef373-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef373-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef373-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef373-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ef373-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef373-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef373-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef373-144">Namespace</span></span><br/>                | <span data-ttu-id="ef373-145">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ef373-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef373-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ef373-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef373-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef373-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef373-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ef373-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef373-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef373-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef373-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef373-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef373-151">\_LOGICALDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="ef373-151">CIM\_LogicalDevice</span></span>](setpowerstate-method-in-class-cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="ef373-152">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ef373-152">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




