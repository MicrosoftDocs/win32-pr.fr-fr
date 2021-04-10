---
description: Classe de base abstraite pour les classes de données calculées préinstallées.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Classe Win32_PerfFormattedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950786"
---
# <a name="win32_perfformatteddata-class"></a><span data-ttu-id="2b0ce-103">\_Classe PerfFormattedData Win32</span><span class="sxs-lookup"><span data-stu-id="2b0ce-103">Win32\_PerfFormattedData class</span></span>

<span data-ttu-id="2b0ce-104">Classe de base abstraite pour les classes de données calculées préinstallées.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-104">An abstract base class for the preinstalled, calculated data classes.</span></span> <span data-ttu-id="2b0ce-105">Un exemple d’une telle classe est [**le \_ \_ \_ disque logique Win32 PerfFormattedData Perfdisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-105">An example of such a class is [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="2b0ce-106">Ces classes contiennent des valeurs calculées fournies par le Fournisseur de données de performances haute performance [mis en forme](../wmisdk/formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-106">These classes contain calculated values provided by the high-performance [Formatted Performance Data Provider](../wmisdk/formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="2b0ce-107">La syntaxe suivante est simplifiée à partir du code MOF et montre toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-107">The following syntax is simplified from MOF code and shows all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b0ce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b0ce-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a><span data-ttu-id="2b0ce-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2b0ce-109">Members</span></span>

<span data-ttu-id="2b0ce-110">La classe **Win32 \_ PerfFormattedData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2b0ce-110">The **Win32\_PerfFormattedData** class has these types of members:</span></span>

-   [<span data-ttu-id="2b0ce-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b0ce-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b0ce-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b0ce-112">Properties</span></span>

<span data-ttu-id="2b0ce-113">La classe **Win32 \_ PerfFormattedData** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-113">The **Win32\_PerfFormattedData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b0ce-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0ce-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0ce-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-117">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="2b0ce-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2b0ce-118">Description textuelle courte pour la statistique ou la métrique.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="2b0ce-119">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0ce-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0ce-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0ce-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0ce-123">Description textuelle de la statistique ou métrique.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="2b0ce-124">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0ce-125">**\_Objet Frequency**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0ce-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0ce-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0ce-128">Fréquence en graduations par seconde de la propriété de l' **\_ objet timestamp** .</span><span class="sxs-lookup"><span data-stu-id="2b0ce-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="2b0ce-129">Lorsqu’il est sous-classé, le fournisseur définit cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="2b0ce-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="2b0ce-131">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-131">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0ce-132">**Fréquence \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-132">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0ce-133">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0ce-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0ce-135">Fréquence en graduations par seconde de la propriété **Frequency \_ PerfTime** .</span><span class="sxs-lookup"><span data-stu-id="2b0ce-135">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="2b0ce-136">Une valeur peut être obtenue en appelant la fonction Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-136">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="2b0ce-137">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="2b0ce-138">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-138">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0ce-139">**Fréquence \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-139">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0ce-140">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0ce-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0ce-142">Fréquence en graduations par seconde de la propriété **timestamp \_ Sys100NS** (10 millions).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-142">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="2b0ce-143">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="2b0ce-144">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-144">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0ce-145">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0ce-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0ce-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-148">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="2b0ce-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2b0ce-149">Étiquette par laquelle la statistique ou la métrique est connue.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-149">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="2b0ce-150">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-150">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2b0ce-151">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-151">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0ce-152">**Timestamp, \_ objet**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-152">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0ce-153">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0ce-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0ce-155">Horodatage défini par l’objet.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-155">Object-defined timestamp.</span></span> <span data-ttu-id="2b0ce-156">Le fournisseur définit sa propriété.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-156">The provider defines his property.</span></span>

<span data-ttu-id="2b0ce-157">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="2b0ce-158">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-158">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0ce-159">**Horodateur \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-159">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0ce-160">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0ce-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0ce-162">Horodateur du compteur de performances élevé.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-162">High Performance counter timestamp.</span></span> <span data-ttu-id="2b0ce-163">Une valeur peut être obtenue en appelant la fonction Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-163">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="2b0ce-164">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="2b0ce-165">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-165">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0ce-166">**Horodateur \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-166">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0ce-167">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b0ce-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0ce-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0ce-169">Valeur d’horodatage en unités de nanosecondes de 100.</span><span class="sxs-lookup"><span data-stu-id="2b0ce-169">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="2b0ce-170">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-170">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="2b0ce-171">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-171">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b0ce-172">Notes</span><span class="sxs-lookup"><span data-stu-id="2b0ce-172">Remarks</span></span>

<span data-ttu-id="2b0ce-173">La classe **Win32 \_ PerfFormattedData** est dérivée de la [**\_ performance Win32**](win32-perf.md), qui est dérivée de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="2b0ce-173">The **Win32\_PerfFormattedData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span> <span data-ttu-id="2b0ce-174">La classe se trouve dans l’espace de noms **\\ cimv2 racine** .</span><span class="sxs-lookup"><span data-stu-id="2b0ce-174">The class is found in the **root\\cimv2** namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b0ce-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b0ce-175">Requirements</span></span>



| <span data-ttu-id="2b0ce-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b0ce-176">Requirement</span></span> | <span data-ttu-id="2b0ce-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b0ce-177">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b0ce-178">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b0ce-178">Minimum supported client</span></span><br/> | <span data-ttu-id="2b0ce-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b0ce-179">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="2b0ce-180">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b0ce-180">Minimum supported server</span></span><br/> | <span data-ttu-id="2b0ce-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b0ce-181">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="2b0ce-182">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2b0ce-182">Namespace</span></span><br/>                | <span data-ttu-id="2b0ce-183">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2b0ce-183">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="2b0ce-184">MOF</span><span class="sxs-lookup"><span data-stu-id="2b0ce-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b0ce-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ce-185"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2b0ce-186">DLL</span><span class="sxs-lookup"><span data-stu-id="2b0ce-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b0ce-187"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b0ce-187"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b0ce-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b0ce-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b0ce-189">**\_Performances Win32**</span><span class="sxs-lookup"><span data-stu-id="2b0ce-189">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="2b0ce-190">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="2b0ce-190">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="2b0ce-191">Accès aux classes de performance préinstallées par WMI</span><span class="sxs-lookup"><span data-stu-id="2b0ce-191">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="2b0ce-192">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="2b0ce-192">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="2b0ce-193">Accès aux données de performances dans le script</span><span class="sxs-lookup"><span data-stu-id="2b0ce-193">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
