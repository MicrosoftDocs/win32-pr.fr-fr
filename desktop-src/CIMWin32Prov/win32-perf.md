---
description: Classe de base pour les classes de compteur de performance Win32 \_ PerfRawData et Win32 \_ PerfFormattedData.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Classe Win32_Perf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 13b339e95e175e4d2dff50c0a9674f8002933c1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512901"
---
# <a name="win32_perf-class"></a><span data-ttu-id="bb9b7-103">\_Classe de performances Win32</span><span class="sxs-lookup"><span data-stu-id="bb9b7-103">Win32\_Perf class</span></span>

<span data-ttu-id="bb9b7-104">Classe de base pour les classes de compteur de performance [**Win32 \_ PerfRawData**](win32-perfrawdata.md) et [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-104">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

<span data-ttu-id="bb9b7-105">**Win32 \_ Perf** définit les propriétés timestamp et Frequency nécessaires utilisées dans les [**algorithmes de la classe**](../wmisdk/countertype-qualifier.md) de compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-105">**Win32\_Perf** defines the required timestamp and frequency properties used in the [**CounterType**](../wmisdk/countertype-qualifier.md) algorithms for the performance counter classes.</span></span>

<span data-ttu-id="bb9b7-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bb9b7-107">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb9b7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb9b7-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

## <a name="members"></a><span data-ttu-id="bb9b7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="bb9b7-109">Members</span></span>

<span data-ttu-id="bb9b7-110">La classe de **\_ performance Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bb9b7-110">The **Win32\_Perf** class has these types of members:</span></span>

-   [<span data-ttu-id="bb9b7-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bb9b7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb9b7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bb9b7-112">Properties</span></span>

<span data-ttu-id="bb9b7-113">La classe de **\_ performance Win32** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-113">The **Win32\_Perf** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb9b7-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9b7-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb9b7-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-117">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="bb9b7-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bb9b7-118">Description textuelle courte pour la statistique ou la métrique.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="bb9b7-119">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9b7-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9b7-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb9b7-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9b7-123">Description textuelle de la statistique ou métrique.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="bb9b7-124">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9b7-125">**\_Objet Frequency**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9b7-126">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb9b7-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9b7-128">Fréquence en graduations par seconde de la propriété de l' **\_ objet timestamp** .</span><span class="sxs-lookup"><span data-stu-id="bb9b7-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="bb9b7-129">Lorsqu’il est sous-classé, le fournisseur définit cette propriété.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="bb9b7-130">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bb9b7-131">**Fréquence \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-131">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9b7-132">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb9b7-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9b7-134">Fréquence en graduations par seconde de la propriété **Frequency \_ PerfTime** .</span><span class="sxs-lookup"><span data-stu-id="bb9b7-134">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="bb9b7-135">Une valeur peut être obtenue en appelant la fonction Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-135">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="bb9b7-136">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bb9b7-137">**Fréquence \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-137">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9b7-138">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb9b7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9b7-140">Fréquence en graduations par seconde de la propriété **timestamp \_ Sys100NS** (10 millions).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-140">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="bb9b7-141">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bb9b7-142">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9b7-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb9b7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-145">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="bb9b7-145">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb9b7-146">Étiquette par laquelle la statistique ou la métrique est connue.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-146">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="bb9b7-147">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="bb9b7-148">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-148">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9b7-149">**Timestamp, \_ objet**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-149">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9b7-150">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb9b7-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9b7-152">Horodatage défini par l’objet.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-152">Object-defined timestamp.</span></span> <span data-ttu-id="bb9b7-153">Le fournisseur définit sa propriété.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-153">The provider defines his property.</span></span>

<span data-ttu-id="bb9b7-154">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bb9b7-155">**Horodateur \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-155">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9b7-156">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb9b7-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9b7-158">Horodateur du compteur de performances élevé.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-158">High Performance counter timestamp.</span></span> <span data-ttu-id="bb9b7-159">Une valeur peut être obtenue en appelant la fonction Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-159">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="bb9b7-160">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="bb9b7-161">**Horodateur \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-161">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9b7-162">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9b7-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bb9b7-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9b7-164">Valeur d’horodatage en unités de nanosecondes de 100.</span><span class="sxs-lookup"><span data-stu-id="bb9b7-164">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="bb9b7-165">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb9b7-166">Notes</span><span class="sxs-lookup"><span data-stu-id="bb9b7-166">Remarks</span></span>

<span data-ttu-id="bb9b7-167">La classe de **\_ performances Win32** dérive de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="bb9b7-167">The **Win32\_Perf** class derives from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb9b7-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb9b7-168">Requirements</span></span>



| <span data-ttu-id="bb9b7-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb9b7-169">Requirement</span></span> | <span data-ttu-id="bb9b7-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb9b7-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9b7-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb9b7-171">Minimum supported client</span></span><br/> | <span data-ttu-id="bb9b7-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb9b7-172">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="bb9b7-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb9b7-173">Minimum supported server</span></span><br/> | <span data-ttu-id="bb9b7-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb9b7-174">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="bb9b7-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bb9b7-175">Namespace</span></span><br/>                | <span data-ttu-id="bb9b7-176">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="bb9b7-176">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="bb9b7-177">DLL</span><span class="sxs-lookup"><span data-stu-id="bb9b7-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb9b7-178"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb9b7-178"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb9b7-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb9b7-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9b7-180">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="bb9b7-180">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dt>

[<span data-ttu-id="bb9b7-181">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="bb9b7-181">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="bb9b7-182">Accès aux classes de performance préinstallées par WMI</span><span class="sxs-lookup"><span data-stu-id="bb9b7-182">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="bb9b7-183">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="bb9b7-183">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="bb9b7-184">Accès aux données de performances dans le script</span><span class="sxs-lookup"><span data-stu-id="bb9b7-184">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
