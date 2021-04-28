---
description: Méthode SetPowerState de la classe CIM_NonVolatileStorage-la méthode SetPowerState définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.
ms.assetid: fdc7dbcb-e2ef-44aa-9a4c-dcae618c5630
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe CIM_NonVolatileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af733cf695ac7ac0bcccf7270929ae3b1bc08b8a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100097"
---
# <a name="setpowerstate-method-of-the-cim_nonvolatilestorage-class"></a><span data-ttu-id="010bc-103">Méthode SetPowerState de la \_ classe CIM NonVolatileStorage</span><span class="sxs-lookup"><span data-stu-id="010bc-103">SetPowerState method of the CIM\_NonVolatileStorage class</span></span>

<span data-ttu-id="010bc-104">La méthode **SetPowerState** définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="010bc-104">The **SetPowerState** method sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="010bc-105">Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="010bc-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="010bc-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="010bc-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="010bc-107">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="010bc-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="010bc-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="010bc-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="010bc-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="010bc-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="010bc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="010bc-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="010bc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="010bc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010bc-112">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="010bc-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="010bc-113">Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour cet appareil logique.</span><span class="sxs-lookup"><span data-stu-id="010bc-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="010bc-114">1</span><span class="sxs-lookup"><span data-stu-id="010bc-114">1</span></span>
</dt> <dd>

<span data-ttu-id="010bc-115">Toute la puissance.</span><span class="sxs-lookup"><span data-stu-id="010bc-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="010bc-116">2</span><span class="sxs-lookup"><span data-stu-id="010bc-116">2</span></span>
</dt> <dd>

<span data-ttu-id="010bc-117">Économie d’énergie en mode faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="010bc-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="010bc-118">3</span><span class="sxs-lookup"><span data-stu-id="010bc-118">3</span></span>
</dt> <dd>

<span data-ttu-id="010bc-119">Économie d’énergie en veille.</span><span class="sxs-lookup"><span data-stu-id="010bc-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="010bc-120">4</span><span class="sxs-lookup"><span data-stu-id="010bc-120">4</span></span>
</dt> <dd>

<span data-ttu-id="010bc-121">Économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="010bc-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="010bc-122">5</span><span class="sxs-lookup"><span data-stu-id="010bc-122">5</span></span>
</dt> <dd>

<span data-ttu-id="010bc-123">Cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="010bc-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="010bc-124">6</span><span class="sxs-lookup"><span data-stu-id="010bc-124">6</span></span>
</dt> <dd>

<span data-ttu-id="010bc-125">Mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="010bc-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="010bc-126">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="010bc-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="010bc-127">Spécifie quand l’état d’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="010bc-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="010bc-128">Lorsque le paramètre *PowerState* est égal à 5 (« Power cycle »), le paramètre *Time* indique quand l’appareil doit se rallumer.</span><span class="sxs-lookup"><span data-stu-id="010bc-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="010bc-129">La mise hors tension est immédiate.</span><span class="sxs-lookup"><span data-stu-id="010bc-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="010bc-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="010bc-130">Return value</span></span>

<span data-ttu-id="010bc-131">Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="010bc-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="010bc-132">Notes </span><span class="sxs-lookup"><span data-stu-id="010bc-132">Remarks</span></span>

<span data-ttu-id="010bc-133">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="010bc-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="010bc-134">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="010bc-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="010bc-135">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="010bc-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="010bc-136">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="010bc-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="010bc-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="010bc-137">Requirements</span></span>



| <span data-ttu-id="010bc-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="010bc-138">Requirement</span></span> | <span data-ttu-id="010bc-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="010bc-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="010bc-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="010bc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="010bc-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="010bc-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="010bc-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="010bc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="010bc-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="010bc-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="010bc-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="010bc-144">Namespace</span></span><br/>                | <span data-ttu-id="010bc-145">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="010bc-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="010bc-146">MOF</span><span class="sxs-lookup"><span data-stu-id="010bc-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="010bc-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="010bc-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="010bc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="010bc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="010bc-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="010bc-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010bc-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="010bc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010bc-151">\_NONVOLATILESTORAGE CIM</span><span class="sxs-lookup"><span data-stu-id="010bc-151">CIM\_NonVolatileStorage</span></span>](setpowerstate-method-in-class-cim-nonvolatilestorage.md)
</dt> <dt>

[<span data-ttu-id="010bc-152">**\_NONVOLATILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="010bc-152">**CIM\_NonVolatileStorage**</span></span>](cim-nonvolatilestorage.md)
</dt> </dl>

 

 




