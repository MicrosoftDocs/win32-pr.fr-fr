---
description: La méthode SetPowerState définit l’état d’alimentation souhaité pour un périphérique logique et le moment où l’appareil doit être placé dans cet État.
ms.assetid: 3194c363-4db7-4928-b47a-7e9c8a5339d7
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b50511fee41382ba635b72dd7c3326e7789cb22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846965"
---
# <a name="setpowerstate-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="ad0ad-103">Méthode SetPowerState de la \_ classe CIM AlarmDevice</span><span class="sxs-lookup"><span data-stu-id="ad0ad-103">SetPowerState method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="ad0ad-104">La méthode **SetPowerState** définit l’état d’alimentation souhaité pour un périphérique logique et le moment où l’appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="ad0ad-105">Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="ad0ad-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="ad0ad-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="ad0ad-107">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ad0ad-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad0ad-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ad0ad-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ad0ad-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ad0ad-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad0ad-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="ad0ad-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad0ad-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad0ad-112">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad0ad-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad0ad-113">Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-113">A **ValueMap** value that specifies the desired power state for the logical device.</span></span>

<dt>

<span data-ttu-id="ad0ad-114">1</span><span class="sxs-lookup"><span data-stu-id="ad0ad-114">1</span></span>
</dt> <dd>

<span data-ttu-id="ad0ad-115">Toute la puissance.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="ad0ad-116">2</span><span class="sxs-lookup"><span data-stu-id="ad0ad-116">2</span></span>
</dt> <dd>

<span data-ttu-id="ad0ad-117">Économie d’énergie en mode faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="ad0ad-118">3</span><span class="sxs-lookup"><span data-stu-id="ad0ad-118">3</span></span>
</dt> <dd>

<span data-ttu-id="ad0ad-119">Économie d’énergie en veille.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="ad0ad-120">4</span><span class="sxs-lookup"><span data-stu-id="ad0ad-120">4</span></span>
</dt> <dd>

<span data-ttu-id="ad0ad-121">Économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="ad0ad-122">5</span><span class="sxs-lookup"><span data-stu-id="ad0ad-122">5</span></span>
</dt> <dd>

<span data-ttu-id="ad0ad-123">Cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="ad0ad-124">6</span><span class="sxs-lookup"><span data-stu-id="ad0ad-124">6</span></span>
</dt> <dd>

<span data-ttu-id="ad0ad-125">Mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ad0ad-126">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad0ad-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad0ad-127">Spécifie quand l’état d’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="ad0ad-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="ad0ad-128">Lorsque le paramètre *PowerState* est égal à 5 (cycle d’alimentation), le paramètre *Time* indique à quel moment l’appareil doit être mis sous tension.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-128">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="ad0ad-129">La mise hors tension est immédiate.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-129">Power off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad0ad-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad0ad-130">Return value</span></span>

<span data-ttu-id="ad0ad-131">Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad0ad-132">Notes</span><span class="sxs-lookup"><span data-stu-id="ad0ad-132">Remarks</span></span>

<span data-ttu-id="ad0ad-133">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ad0ad-134">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ad0ad-135">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ad0ad-136">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ad0ad-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad0ad-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad0ad-137">Requirements</span></span>



| <span data-ttu-id="ad0ad-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad0ad-138">Requirement</span></span> | <span data-ttu-id="ad0ad-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad0ad-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0ad-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad0ad-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ad0ad-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad0ad-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad0ad-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad0ad-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ad0ad-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad0ad-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad0ad-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ad0ad-144">Namespace</span></span><br/>                | <span data-ttu-id="ad0ad-145">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ad0ad-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad0ad-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ad0ad-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad0ad-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad0ad-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad0ad-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ad0ad-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad0ad-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad0ad-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad0ad-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad0ad-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad0ad-151">\_ALARMDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="ad0ad-151">CIM\_AlarmDevice</span></span>](setpowerstate-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="ad0ad-152">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ad0ad-152">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

 




