---
description: Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.
ms.assetid: 7b36a987-d4c9-4cdc-8703-cf3f713e0c4a
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e42be975b7764039bec603928ef5a27bc38997b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513325"
---
# <a name="setpowerstate-method-of-the-win32_diskpartition-class"></a><span data-ttu-id="d12f7-103">Méthode SetPowerState de la \_ classe DiskPartition Win32</span><span class="sxs-lookup"><span data-stu-id="d12f7-103">SetPowerState method of the Win32\_DiskPartition class</span></span>

<span data-ttu-id="d12f7-104">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="d12f7-104">Sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="d12f7-105">Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="d12f7-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="d12f7-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="d12f7-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d12f7-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d12f7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d12f7-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d12f7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d12f7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d12f7-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="d12f7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d12f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d12f7-111">*PowerState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d12f7-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d12f7-112">Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour cet appareil logique.</span><span class="sxs-lookup"><span data-stu-id="d12f7-112">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="d12f7-113">1</span><span class="sxs-lookup"><span data-stu-id="d12f7-113">1</span></span>
</dt> <dd>

<span data-ttu-id="d12f7-114">Toute la puissance.</span><span class="sxs-lookup"><span data-stu-id="d12f7-114">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="d12f7-115">2</span><span class="sxs-lookup"><span data-stu-id="d12f7-115">2</span></span>
</dt> <dd>

<span data-ttu-id="d12f7-116">Économie d’énergie en mode faible consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="d12f7-116">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="d12f7-117">3</span><span class="sxs-lookup"><span data-stu-id="d12f7-117">3</span></span>
</dt> <dd>

<span data-ttu-id="d12f7-118">Économie d’énergie en veille.</span><span class="sxs-lookup"><span data-stu-id="d12f7-118">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="d12f7-119">4</span><span class="sxs-lookup"><span data-stu-id="d12f7-119">4</span></span>
</dt> <dd>

<span data-ttu-id="d12f7-120">Économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="d12f7-120">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="d12f7-121">5</span><span class="sxs-lookup"><span data-stu-id="d12f7-121">5</span></span>
</dt> <dd>

<span data-ttu-id="d12f7-122">Cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="d12f7-122">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="d12f7-123">6</span><span class="sxs-lookup"><span data-stu-id="d12f7-123">6</span></span>
</dt> <dd>

<span data-ttu-id="d12f7-124">Mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="d12f7-124">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d12f7-125">*Heure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d12f7-125">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d12f7-126">Spécifie quand l’état d’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu).</span><span class="sxs-lookup"><span data-stu-id="d12f7-126">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="d12f7-127">Lorsque le paramètre *PowerState* est égal à 5 (« Power cycle »), le paramètre *Time* indique quand l’appareil doit se rallumer.</span><span class="sxs-lookup"><span data-stu-id="d12f7-127">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="d12f7-128">La mise hors tension est immédiate.</span><span class="sxs-lookup"><span data-stu-id="d12f7-128">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d12f7-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d12f7-129">Return value</span></span>

<span data-ttu-id="d12f7-130">Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d12f7-130">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="d12f7-131">Notes</span><span class="sxs-lookup"><span data-stu-id="d12f7-131">Remarks</span></span>

<span data-ttu-id="d12f7-132">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="d12f7-132">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d12f7-133">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d12f7-133">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d12f7-134">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d12f7-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d12f7-135">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d12f7-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d12f7-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d12f7-136">Requirements</span></span>



| <span data-ttu-id="d12f7-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d12f7-137">Requirement</span></span> | <span data-ttu-id="d12f7-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="d12f7-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d12f7-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d12f7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d12f7-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d12f7-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d12f7-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d12f7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d12f7-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d12f7-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d12f7-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d12f7-143">Namespace</span></span><br/>                | <span data-ttu-id="d12f7-144">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d12f7-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d12f7-145">MOF</span><span class="sxs-lookup"><span data-stu-id="d12f7-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d12f7-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d12f7-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d12f7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d12f7-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d12f7-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d12f7-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d12f7-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d12f7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d12f7-150">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="d12f7-150">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="d12f7-151">**\_DiskPartition Win32**</span><span class="sxs-lookup"><span data-stu-id="d12f7-151">**Win32\_DiskPartition**</span></span>](win32-diskpartition.md)
</dt> </dl>

 

 




