---
description: La méthode ResetCounter réinitialise les compteurs d’erreur et d’avertissement.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: Méthode ResetCounter de la classe CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860706"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a><span data-ttu-id="62b93-103">Méthode ResetCounter de la \_ classe CIM DeviceErrorCounts</span><span class="sxs-lookup"><span data-stu-id="62b93-103">ResetCounter method of the CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="62b93-104">La méthode **ResetCounter** réinitialise les compteurs d’erreur et d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="62b93-104">The **ResetCounter** method resets the error and warning counters.</span></span> <span data-ttu-id="62b93-105">Une méthode est utilisée afin que l’instrumentation de l’appareil logique, qui calcule les erreurs et les avertissements, puisse également réinitialiser son traitement interne et ses compteurs.</span><span class="sxs-lookup"><span data-stu-id="62b93-105">A method is used so that the logical device's instrumentation, which tabulates the errors and warnings, can also reset its internal processing and counters.</span></span> <span data-ttu-id="62b93-106">Dans une sous-classe, l’ensemble des codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="62b93-106">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="62b93-107">Les chaînes dans lesquelles le contenu **ValueMap** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="62b93-107">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62b93-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="62b93-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="62b93-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="62b93-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="62b93-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="62b93-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="62b93-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="62b93-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="62b93-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62b93-112">Syntax</span></span>


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a><span data-ttu-id="62b93-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62b93-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62b93-114">*SelectedCounter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="62b93-114">*SelectedCounter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62b93-115">Compteur d’erreurs à réinitialiser.</span><span class="sxs-lookup"><span data-stu-id="62b93-115">Error counter to reset.</span></span>

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

<span data-ttu-id="62b93-116">**Tout** (0)</span><span class="sxs-lookup"><span data-stu-id="62b93-116">**All** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

<span data-ttu-id="62b93-117">**Compteur d’erreurs indéterminé** (1)</span><span class="sxs-lookup"><span data-stu-id="62b93-117">**Indeterminate Error Counter** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

<span data-ttu-id="62b93-118">**Compteur d’erreurs critiques** (2)</span><span class="sxs-lookup"><span data-stu-id="62b93-118">**Critical Error Counter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

<span data-ttu-id="62b93-119">**Compteur d’erreurs majeures** (3)</span><span class="sxs-lookup"><span data-stu-id="62b93-119">**Major Error Counter** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

<span data-ttu-id="62b93-120">**Compteur d’erreurs mineures** (4)</span><span class="sxs-lookup"><span data-stu-id="62b93-120">**Minor Error Counter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

<span data-ttu-id="62b93-121">**Compteur d’avertissements** (5)</span><span class="sxs-lookup"><span data-stu-id="62b93-121">**Warning Counter** (5)</span></span>


<span data-ttu-id="62b93-122"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="62b93-122"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="62b93-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62b93-123">Return value</span></span>

<span data-ttu-id="62b93-124">Retourne 0 (zéro) en cas de réussite, 1 (un) s’il n’est pas pris en charge et toute autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="62b93-124">Returns 0 (zero) if successful, 1 (one) if not supported, and any other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="62b93-125">Notes</span><span class="sxs-lookup"><span data-stu-id="62b93-125">Remarks</span></span>

<span data-ttu-id="62b93-126">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="62b93-126">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="62b93-127">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="62b93-127">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="62b93-128">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="62b93-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="62b93-129">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="62b93-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="62b93-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62b93-130">Requirements</span></span>



| <span data-ttu-id="62b93-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62b93-131">Requirement</span></span> | <span data-ttu-id="62b93-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="62b93-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62b93-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62b93-133">Minimum supported client</span></span><br/> | <span data-ttu-id="62b93-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62b93-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62b93-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62b93-135">Minimum supported server</span></span><br/> | <span data-ttu-id="62b93-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62b93-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62b93-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="62b93-137">Namespace</span></span><br/>                | <span data-ttu-id="62b93-138">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="62b93-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62b93-139">MOF</span><span class="sxs-lookup"><span data-stu-id="62b93-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62b93-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62b93-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62b93-141">DLL</span><span class="sxs-lookup"><span data-stu-id="62b93-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62b93-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62b93-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b93-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62b93-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b93-144">\_DEVICEERRORCOUNTS CIM</span><span class="sxs-lookup"><span data-stu-id="62b93-144">CIM\_DeviceErrorCounts</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[<span data-ttu-id="62b93-145">**\_DEVICEERRORCOUNTS CIM**</span><span class="sxs-lookup"><span data-stu-id="62b93-145">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> </dl>

 

