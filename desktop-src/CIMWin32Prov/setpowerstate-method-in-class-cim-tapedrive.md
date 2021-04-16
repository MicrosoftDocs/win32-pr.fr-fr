---
description: La méthode SetPowerState de la classe CIM CIM \_ définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.
ms.assetid: 73f98d08-49da-4b21-91c4-cbe420c648e4
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6efcfe08dfddca3477081f65fac35780f713005
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524151"
---
# <a name="setpowerstate-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="f1034-103">Méthode SetPowerState de la classe CIM CIM \_</span><span class="sxs-lookup"><span data-stu-id="f1034-103">SetPowerState method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="f1034-104">La méthode **SetPowerState** de la classe CIM CIM \_ définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="f1034-104">The **SetPowerState** method of the CIM\_TapeDrive class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f1034-105">Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="f1034-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="f1034-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="f1034-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="f1034-107">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f1034-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1034-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1034-108">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="f1034-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1034-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1034-110">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1034-110">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1034-111">Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour cet appareil logique.</span><span class="sxs-lookup"><span data-stu-id="f1034-111">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="f1034-112">1</span><span class="sxs-lookup"><span data-stu-id="f1034-112">1</span></span>
</dt> <dd>

<span data-ttu-id="f1034-113">Toute la puissance.</span><span class="sxs-lookup"><span data-stu-id="f1034-113">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="f1034-114">2</span><span class="sxs-lookup"><span data-stu-id="f1034-114">2</span></span>
</dt> <dd>

<span data-ttu-id="f1034-115">Économie d’énergie en mode faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="f1034-115">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="f1034-116">3</span><span class="sxs-lookup"><span data-stu-id="f1034-116">3</span></span>
</dt> <dd>

<span data-ttu-id="f1034-117">Économie d’énergie en veille.</span><span class="sxs-lookup"><span data-stu-id="f1034-117">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="f1034-118">4</span><span class="sxs-lookup"><span data-stu-id="f1034-118">4</span></span>
</dt> <dd>

<span data-ttu-id="f1034-119">Économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="f1034-119">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="f1034-120">5</span><span class="sxs-lookup"><span data-stu-id="f1034-120">5</span></span>
</dt> <dd>

<span data-ttu-id="f1034-121">Cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="f1034-121">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="f1034-122">6</span><span class="sxs-lookup"><span data-stu-id="f1034-122">6</span></span>
</dt> <dd>

<span data-ttu-id="f1034-123">Mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="f1034-123">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f1034-124">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1034-124">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1034-125">Spécifie quand l’état d’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="f1034-125">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="f1034-126">Lorsque le paramètre *PowerState* est égal à 5 (« Power cycle »), le paramètre *Time* indique quand l’appareil doit se rallumer.</span><span class="sxs-lookup"><span data-stu-id="f1034-126">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="f1034-127">La mise hors tension est immédiate.</span><span class="sxs-lookup"><span data-stu-id="f1034-127">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1034-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1034-128">Return value</span></span>

<span data-ttu-id="f1034-129">Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f1034-129">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1034-130">Notes</span><span class="sxs-lookup"><span data-stu-id="f1034-130">Remarks</span></span>

<span data-ttu-id="f1034-131">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="f1034-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f1034-132">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f1034-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f1034-133">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="f1034-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f1034-134">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="f1034-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1034-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1034-135">Requirements</span></span>



| <span data-ttu-id="f1034-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1034-136">Requirement</span></span> | <span data-ttu-id="f1034-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1034-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1034-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1034-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f1034-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1034-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1034-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1034-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f1034-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1034-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1034-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f1034-142">Namespace</span></span><br/>                | <span data-ttu-id="f1034-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f1034-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1034-144">MOF</span><span class="sxs-lookup"><span data-stu-id="f1034-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1034-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1034-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1034-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f1034-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1034-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1034-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1034-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1034-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1034-149">CIM \_ CIM</span><span class="sxs-lookup"><span data-stu-id="f1034-149">CIM\_TapeDrive</span></span>](setpowerstate-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="f1034-150">**CIM \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="f1034-150">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




