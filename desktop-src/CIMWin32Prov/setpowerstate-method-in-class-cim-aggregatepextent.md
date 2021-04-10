---
description: La méthode SetPowerState définit l’état d’alimentation souhaité pour un périphérique logique et le moment où l’appareil doit être placé dans cet État.
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe CIM_AggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47c97f30da1c8b6f2fe9a6032ef9be9ae87a7d6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950678"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a><span data-ttu-id="acddd-103">Méthode SetPowerState de la \_ classe CIM AggregatePExtent</span><span class="sxs-lookup"><span data-stu-id="acddd-103">SetPowerState method of the CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="acddd-104">La méthode **SetPowerState** définit l’état d’alimentation souhaité pour un périphérique logique et le moment où l’appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="acddd-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="acddd-105">Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="acddd-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="acddd-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="acddd-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="acddd-107">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="acddd-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="acddd-108">Pour plus d’informations sur l’utilisation de cette méthode avec C/C++, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="acddd-108">For more information about using this method with C/C++, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="acddd-109">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="acddd-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="acddd-110">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="acddd-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="acddd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acddd-111">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="acddd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acddd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acddd-113">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acddd-113">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acddd-114">Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour cet appareil logique.</span><span class="sxs-lookup"><span data-stu-id="acddd-114">The **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="acddd-115">1</span><span class="sxs-lookup"><span data-stu-id="acddd-115">1</span></span>
</dt> <dd>

<span data-ttu-id="acddd-116">Pleine puissance</span><span class="sxs-lookup"><span data-stu-id="acddd-116">Full power</span></span>

</dd> <dt>

<span data-ttu-id="acddd-117">2</span><span class="sxs-lookup"><span data-stu-id="acddd-117">2</span></span>
</dt> <dd>

<span data-ttu-id="acddd-118">Économie d’énergie en mode faible puissance</span><span class="sxs-lookup"><span data-stu-id="acddd-118">Power-save   low-power mode</span></span>

</dd> <dt>

<span data-ttu-id="acddd-119">3</span><span class="sxs-lookup"><span data-stu-id="acddd-119">3</span></span>
</dt> <dd>

<span data-ttu-id="acddd-120">Économie d’énergie en veille</span><span class="sxs-lookup"><span data-stu-id="acddd-120">Power-save   standby</span></span>

</dd> <dt>

<span data-ttu-id="acddd-121">4</span><span class="sxs-lookup"><span data-stu-id="acddd-121">4</span></span>
</dt> <dd>

<span data-ttu-id="acddd-122">Économie d’énergie</span><span class="sxs-lookup"><span data-stu-id="acddd-122">Power-save   other</span></span>

</dd> <dt>

<span data-ttu-id="acddd-123">5</span><span class="sxs-lookup"><span data-stu-id="acddd-123">5</span></span>
</dt> <dd>

<span data-ttu-id="acddd-124">Cycle d’alimentation</span><span class="sxs-lookup"><span data-stu-id="acddd-124">Power cycle</span></span>

</dd> <dt>

<span data-ttu-id="acddd-125">6</span><span class="sxs-lookup"><span data-stu-id="acddd-125">6</span></span>
</dt> <dd>

<span data-ttu-id="acddd-126">Mise hors tension</span><span class="sxs-lookup"><span data-stu-id="acddd-126">Power off</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="acddd-127">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="acddd-127">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acddd-128">Lorsque l’état d’alimentation doit être défini, soit comme valeur de date et d’heure régulière, soit comme valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="acddd-128">When the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="acddd-129">Lorsque le paramètre *PowerState* est égal à 5 (cycle d’alimentation), le paramètre *Time* indique quand l’appareil doit se mettre à nouveau sous tension.</span><span class="sxs-lookup"><span data-stu-id="acddd-129">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="acddd-130">La mise hors tension est immédiate.</span><span class="sxs-lookup"><span data-stu-id="acddd-130">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acddd-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acddd-131">Return value</span></span>

<span data-ttu-id="acddd-132">Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="acddd-132">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="acddd-133">Notes</span><span class="sxs-lookup"><span data-stu-id="acddd-133">Remarks</span></span>

<span data-ttu-id="acddd-134">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="acddd-134">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="acddd-135">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="acddd-135">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="acddd-136">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="acddd-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="acddd-137">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="acddd-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="acddd-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acddd-138">Requirements</span></span>



| <span data-ttu-id="acddd-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acddd-139">Requirement</span></span> | <span data-ttu-id="acddd-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="acddd-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acddd-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acddd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="acddd-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acddd-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="acddd-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acddd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="acddd-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acddd-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="acddd-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="acddd-145">Namespace</span></span><br/>                | <span data-ttu-id="acddd-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="acddd-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="acddd-147">MOF</span><span class="sxs-lookup"><span data-stu-id="acddd-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acddd-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acddd-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="acddd-149">DLL</span><span class="sxs-lookup"><span data-stu-id="acddd-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acddd-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acddd-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acddd-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acddd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acddd-152">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="acddd-152">**CIM\_AggregatePExtent**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[<span data-ttu-id="acddd-153">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="acddd-153">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> </dl>

 

