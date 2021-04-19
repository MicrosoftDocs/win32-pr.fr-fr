---
description: La méthode SetPowerState de la \_ classe CIM InfraredController définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.
ms.assetid: dce688f3-b7c2-4e43-a26f-7318ce0011b8
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe CIM_InfraredController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InfraredController.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730071111d1ebf86af229236826647626ca8f71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514933"
---
# <a name="setpowerstate-method-of-the-cim_infraredcontroller-class"></a><span data-ttu-id="d3548-103">Méthode SetPowerState de la \_ classe CIM InfraredController</span><span class="sxs-lookup"><span data-stu-id="d3548-103">SetPowerState method of the CIM\_InfraredController class</span></span>

<span data-ttu-id="d3548-104">La méthode **SetPowerState** de la \_ classe CIM InfraredController définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="d3548-104">The **SetPowerState** method of the CIM\_InfraredController class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="d3548-105">Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="d3548-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="d3548-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="d3548-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="d3548-107">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d3548-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3548-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d3548-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d3548-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d3548-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d3548-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3548-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="d3548-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3548-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3548-112">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3548-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3548-113">Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="d3548-113">A **ValueMap** value that specifies the desired power state for the logical device.</span></span>

<dt>

<span data-ttu-id="d3548-114">1</span><span class="sxs-lookup"><span data-stu-id="d3548-114">1</span></span>
</dt> <dd>

<span data-ttu-id="d3548-115">Toute la puissance.</span><span class="sxs-lookup"><span data-stu-id="d3548-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="d3548-116">2</span><span class="sxs-lookup"><span data-stu-id="d3548-116">2</span></span>
</dt> <dd>

<span data-ttu-id="d3548-117">Économie d’énergie en mode faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="d3548-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="d3548-118">3</span><span class="sxs-lookup"><span data-stu-id="d3548-118">3</span></span>
</dt> <dd>

<span data-ttu-id="d3548-119">Économie d’énergie en veille.</span><span class="sxs-lookup"><span data-stu-id="d3548-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="d3548-120">4</span><span class="sxs-lookup"><span data-stu-id="d3548-120">4</span></span>
</dt> <dd>

<span data-ttu-id="d3548-121">Économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="d3548-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="d3548-122">5</span><span class="sxs-lookup"><span data-stu-id="d3548-122">5</span></span>
</dt> <dd>

<span data-ttu-id="d3548-123">Cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="d3548-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="d3548-124">6</span><span class="sxs-lookup"><span data-stu-id="d3548-124">6</span></span>
</dt> <dd>

<span data-ttu-id="d3548-125">Mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="d3548-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d3548-126">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3548-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3548-127">Spécifie quand l’état d’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="d3548-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="d3548-128">Lorsque le paramètre *PowerState* est égal à 5 (« Power cycle »), le paramètre *Time* indique quand l’appareil doit se rallumer.</span><span class="sxs-lookup"><span data-stu-id="d3548-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="d3548-129">La mise hors tension est immédiate.</span><span class="sxs-lookup"><span data-stu-id="d3548-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3548-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3548-130">Return value</span></span>

<span data-ttu-id="d3548-131">Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d3548-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3548-132">Notes</span><span class="sxs-lookup"><span data-stu-id="d3548-132">Remarks</span></span>

<span data-ttu-id="d3548-133">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="d3548-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d3548-134">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d3548-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d3548-135">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d3548-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d3548-136">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d3548-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3548-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3548-137">Requirements</span></span>



| <span data-ttu-id="d3548-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3548-138">Requirement</span></span> | <span data-ttu-id="d3548-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3548-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3548-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3548-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d3548-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3548-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3548-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3548-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d3548-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3548-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3548-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3548-144">Namespace</span></span><br/>                | <span data-ttu-id="d3548-145">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d3548-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d3548-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d3548-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3548-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3548-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3548-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d3548-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3548-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3548-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3548-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3548-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3548-151">\_INFRAREDCONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="d3548-151">CIM\_InfraredController</span></span>](setpowerstate-method-in-class-cim-infraredcontroller.md)
</dt> <dt>

[<span data-ttu-id="d3548-152">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="d3548-152">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> </dl>

 

 




