---
description: La méthode SetUrgency définit le niveau d’urgence souhaité pour une alarme.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Méthode SetUrgency de la classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950632"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="3779c-103">Méthode SetUrgency de la \_ classe CIM AlarmDevice</span><span class="sxs-lookup"><span data-stu-id="3779c-103">SetUrgency method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="3779c-104">La méthode **SetUrgency** définit le niveau d’urgence souhaité pour une alarme.</span><span class="sxs-lookup"><span data-stu-id="3779c-104">The **SetUrgency** method sets the desired urgency level for an alarm.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3779c-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3779c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3779c-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3779c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3779c-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3779c-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3779c-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3779c-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3779c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3779c-109">Syntax</span></span>


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a><span data-ttu-id="3779c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3779c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3779c-111">*RequestedUrgency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3779c-111">*RequestedUrgency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3779c-112">Fréquence relative à laquelle l’alarme clignote, vibre ou émet des tonalités audibles.</span><span class="sxs-lookup"><span data-stu-id="3779c-112">Relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span> <span data-ttu-id="3779c-113">Les valeurs suivantes proviennent de la propriété **urgence** dans [**CIM \_ AlarmDevice**](cim-alarmdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3779c-113">The following values are from the **Urgency** property in [**CIM\_AlarmDevice**](cim-alarmdevice.md).</span></span>

<dt>

<span data-ttu-id="3779c-114">0</span><span class="sxs-lookup"><span data-stu-id="3779c-114">0</span></span>
</dt> <dd>

<span data-ttu-id="3779c-115">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="3779c-115">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="3779c-116">1</span><span class="sxs-lookup"><span data-stu-id="3779c-116">1</span></span>
</dt> <dd>

<span data-ttu-id="3779c-117">Autre.</span><span class="sxs-lookup"><span data-stu-id="3779c-117">Other.</span></span>

</dd> <dt>

<span data-ttu-id="3779c-118">2</span><span class="sxs-lookup"><span data-stu-id="3779c-118">2</span></span>
</dt> <dd>

<span data-ttu-id="3779c-119">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3779c-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3779c-120">3</span><span class="sxs-lookup"><span data-stu-id="3779c-120">3</span></span>
</dt> <dd>

<span data-ttu-id="3779c-121">Informatif.</span><span class="sxs-lookup"><span data-stu-id="3779c-121">Informational.</span></span>

</dd> <dt>

<span data-ttu-id="3779c-122">4</span><span class="sxs-lookup"><span data-stu-id="3779c-122">4</span></span>
</dt> <dd>

<span data-ttu-id="3779c-123">Non critique.</span><span class="sxs-lookup"><span data-stu-id="3779c-123">Non-critical.</span></span>

</dd> <dt>

<span data-ttu-id="3779c-124">5</span><span class="sxs-lookup"><span data-stu-id="3779c-124">5</span></span>
</dt> <dd>

<span data-ttu-id="3779c-125">Critique.</span><span class="sxs-lookup"><span data-stu-id="3779c-125">Critical.</span></span>

</dd> <dt>

<span data-ttu-id="3779c-126">6</span><span class="sxs-lookup"><span data-stu-id="3779c-126">6</span></span>
</dt> <dd>

<span data-ttu-id="3779c-127">Irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="3779c-127">Unrecoverable.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3779c-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3779c-128">Return value</span></span>

<span data-ttu-id="3779c-129">Retourne la valeur 0 (zéro) en cas de réussite, 1 (un) si le niveau d’urgence demandé n’est pas pris en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="3779c-129">Returns a value of 0 (zero) on success, 1 (one) if the requested urgency level is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3779c-130">Notes</span><span class="sxs-lookup"><span data-stu-id="3779c-130">Remarks</span></span>

<span data-ttu-id="3779c-131">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="3779c-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3779c-132">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3779c-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3779c-133">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="3779c-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3779c-134">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3779c-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3779c-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3779c-135">Requirements</span></span>



| <span data-ttu-id="3779c-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3779c-136">Requirement</span></span> | <span data-ttu-id="3779c-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="3779c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3779c-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3779c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3779c-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3779c-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3779c-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3779c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3779c-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3779c-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3779c-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3779c-142">Namespace</span></span><br/>                | <span data-ttu-id="3779c-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3779c-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3779c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="3779c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3779c-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3779c-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3779c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="3779c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3779c-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3779c-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3779c-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3779c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3779c-149">\_ALARMDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="3779c-149">CIM\_AlarmDevice</span></span>](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="3779c-150">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3779c-150">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

