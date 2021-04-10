---
description: La méthode SetPowerState de la \_ classe CIM UnitaryComputerSystem définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.
ms.assetid: a02991d5-3c93-4579-b1f5-f70ad7c7052b
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d9b69306c7bb362dceaee254be5dae8f5d37a52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950395"
---
# <a name="setpowerstate-method-of-the-cim_unitarycomputersystem-class"></a><span data-ttu-id="1a10a-103">Méthode SetPowerState de la \_ classe CIM UnitaryComputerSystem</span><span class="sxs-lookup"><span data-stu-id="1a10a-103">SetPowerState method of the CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="1a10a-104">La méthode **SetPowerState** de la \_ classe CIM UnitaryComputerSystem définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="1a10a-104">The **SetPowerState** method of the CIM\_UnitaryComputerSystem class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="1a10a-105">Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="1a10a-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="1a10a-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="1a10a-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="1a10a-107">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1a10a-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a10a-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1a10a-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1a10a-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1a10a-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1a10a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a10a-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="1a10a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a10a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a10a-112">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a10a-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a10a-113">Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour cet appareil logique.</span><span class="sxs-lookup"><span data-stu-id="1a10a-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="1a10a-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Pleine puissance** (1)</span><span class="sxs-lookup"><span data-stu-id="1a10a-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1a10a-115">Toute la puissance.</span><span class="sxs-lookup"><span data-stu-id="1a10a-115">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1a10a-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (2)</span><span class="sxs-lookup"><span data-stu-id="1a10a-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1a10a-117">Économie d’énergie en mode faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="1a10a-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1a10a-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (3)</span><span class="sxs-lookup"><span data-stu-id="1a10a-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1a10a-119">Économie d’énergie en veille.</span><span class="sxs-lookup"><span data-stu-id="1a10a-119">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="1a10a-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>Économie **d’énergie-autres** (4)</span><span class="sxs-lookup"><span data-stu-id="1a10a-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1a10a-121">Économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="1a10a-121">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1a10a-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (5)</span><span class="sxs-lookup"><span data-stu-id="1a10a-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1a10a-123">Cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="1a10a-123">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1a10a-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (6)</span><span class="sxs-lookup"><span data-stu-id="1a10a-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1a10a-125">Mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="1a10a-125">Power off.</span></span>

</dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="1a10a-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Mise en veille prolongée** (7)</span><span class="sxs-lookup"><span data-stu-id="1a10a-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Hibernate** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1a10a-127">Veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="1a10a-127">Hibernate.</span></span>

</dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="1a10a-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Désactivé** (8)</span><span class="sxs-lookup"><span data-stu-id="1a10a-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft Off** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1a10a-129">Désactivé.</span><span class="sxs-lookup"><span data-stu-id="1a10a-129">Soft off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1a10a-130">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a10a-130">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a10a-131">Spécifie quand l’état d’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="1a10a-131">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="1a10a-132">Lorsque le paramètre *PowerState* est égal à 5 (« Power cycle »), le paramètre *Time* indique quand l’appareil doit se rallumer.</span><span class="sxs-lookup"><span data-stu-id="1a10a-132">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="1a10a-133">La mise hors tension est immédiate.</span><span class="sxs-lookup"><span data-stu-id="1a10a-133">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a10a-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a10a-134">Return value</span></span>

<span data-ttu-id="1a10a-135">Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1a10a-135">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a10a-136">Notes</span><span class="sxs-lookup"><span data-stu-id="1a10a-136">Remarks</span></span>

<span data-ttu-id="1a10a-137">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="1a10a-137">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1a10a-138">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1a10a-138">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1a10a-139">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1a10a-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1a10a-140">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1a10a-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a10a-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a10a-141">Requirements</span></span>



| <span data-ttu-id="1a10a-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a10a-142">Requirement</span></span> | <span data-ttu-id="1a10a-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a10a-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a10a-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a10a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1a10a-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a10a-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a10a-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a10a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1a10a-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a10a-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a10a-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1a10a-148">Namespace</span></span><br/>                | <span data-ttu-id="1a10a-149">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1a10a-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a10a-150">MOF</span><span class="sxs-lookup"><span data-stu-id="1a10a-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a10a-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a10a-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a10a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1a10a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a10a-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a10a-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a10a-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a10a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a10a-155">\_UNITARYCOMPUTERSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="1a10a-155">CIM\_UnitaryComputerSystem</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md)
</dt> <dt>

[<span data-ttu-id="1a10a-156">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="1a10a-156">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> </dl>

 

 




