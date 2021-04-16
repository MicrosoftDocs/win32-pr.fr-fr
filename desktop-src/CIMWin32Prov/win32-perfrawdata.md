---
description: Classe de base abstraite pour toutes les classes de compteur de performances brutes concrètes.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Classe Win32_PerfRawData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524271"
---
# <a name="win32_perfrawdata-class"></a><span data-ttu-id="ffdef-103">\_Classe PerfRawData Win32</span><span class="sxs-lookup"><span data-stu-id="ffdef-103">Win32\_PerfRawData class</span></span>

<span data-ttu-id="ffdef-104">Classe de base abstraite pour toutes les classes de compteur de performances brutes concrètes.</span><span class="sxs-lookup"><span data-stu-id="ffdef-104">The abstract base class for all concrete raw performance counter classes.</span></span>

<span data-ttu-id="ffdef-105">Pour apparaître dans le moniteur système, les classes de compteur de performance doivent être ajoutées à l' \\ espace de noms CIMV2 racine et dérivées de **Win32 \_ PerfRawData**.</span><span class="sxs-lookup"><span data-stu-id="ffdef-105">To appear in System Monitor, performance counter classes must be added to the root\\cimv2 namespace and derived from **Win32\_PerfRawData**.</span></span> <span data-ttu-id="ffdef-106">Les données de ces classes sont fournies par le fournisseur de [compteurs de performances](../wmisdk/performance-counter-provider.md)hautes performances.</span><span class="sxs-lookup"><span data-stu-id="ffdef-106">Data in these classes are provided by the high-performance [Performance Counter Provider](../wmisdk/performance-counter-provider.md).</span></span>

<span data-ttu-id="ffdef-107">Les propriétés suivantes sont héritées lorsqu’une classe est dérivée de **Win32 \_ PerfRawData**:</span><span class="sxs-lookup"><span data-stu-id="ffdef-107">The following properties are inherited when a class is derived from **Win32\_PerfRawData**:</span></span>

-   <span data-ttu-id="ffdef-108">**Horodateur \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="ffdef-108">**Timestamp\_PerfTime**</span></span>
-   <span data-ttu-id="ffdef-109">**Horodateur \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="ffdef-109">**Timestamp\_Sys100NS**</span></span>
-   <span data-ttu-id="ffdef-110">**Timestamp, \_ objet**</span><span class="sxs-lookup"><span data-stu-id="ffdef-110">**Timestamp\_Object**</span></span>
-   <span data-ttu-id="ffdef-111">**Fréquence \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="ffdef-111">**Frequency\_PerfTime**</span></span>
-   <span data-ttu-id="ffdef-112">**Fréquence \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="ffdef-112">**Frequency\_Sys100NS**</span></span>
-   <span data-ttu-id="ffdef-113">**\_Objet Frequency**</span><span class="sxs-lookup"><span data-stu-id="ffdef-113">**Frequency\_Object**</span></span>

<span data-ttu-id="ffdef-114">Dans chaque cas, les propriétés doivent être remplies par le fournisseur ou la classe ne peut pas être affichée dans le moniteur système.</span><span class="sxs-lookup"><span data-stu-id="ffdef-114">In each case, the properties must be filled out by the provider or the class cannot be displayed in System Monitor.</span></span> <span data-ttu-id="ffdef-115">Ces propriétés sont utilisées pour calculer des formules de type de compteur par les consommateurs de données de performances.</span><span class="sxs-lookup"><span data-stu-id="ffdef-115">These properties are used to compute counter type formulas by consumers of performance data.</span></span>

<span data-ttu-id="ffdef-116">La syntaxe suivante est simplifiée à partir du code MOF et montre toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ffdef-116">The following syntax is simplified from MOF code and shows all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffdef-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffdef-117">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

## <a name="members"></a><span data-ttu-id="ffdef-118">Membres</span><span class="sxs-lookup"><span data-stu-id="ffdef-118">Members</span></span>

<span data-ttu-id="ffdef-119">La classe **Win32 \_ PerfRawData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffdef-119">The **Win32\_PerfRawData** class has these types of members:</span></span>

-   [<span data-ttu-id="ffdef-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ffdef-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffdef-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ffdef-121">Properties</span></span>

<span data-ttu-id="ffdef-122">La classe **Win32 \_ PerfRawData** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ffdef-122">The **Win32\_PerfRawData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffdef-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ffdef-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffdef-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ffdef-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffdef-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-126">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="ffdef-126">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ffdef-127">Description textuelle courte pour la statistique ou la métrique.</span><span class="sxs-lookup"><span data-stu-id="ffdef-127">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="ffdef-128">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-128">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffdef-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="ffdef-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffdef-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ffdef-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffdef-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffdef-132">Description textuelle de la statistique ou métrique.</span><span class="sxs-lookup"><span data-stu-id="ffdef-132">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="ffdef-133">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-133">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffdef-134">**\_Objet Frequency**</span><span class="sxs-lookup"><span data-stu-id="ffdef-134">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffdef-135">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ffdef-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffdef-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffdef-137">Fréquence en graduations par seconde de la propriété de l' **\_ objet timestamp** .</span><span class="sxs-lookup"><span data-stu-id="ffdef-137">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="ffdef-138">Lorsqu’il est sous-classé, le fournisseur définit cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ffdef-138">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="ffdef-139">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffdef-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="ffdef-140">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-140">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffdef-141">**Fréquence \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="ffdef-141">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffdef-142">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ffdef-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffdef-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffdef-144">Fréquence en graduations par seconde de la propriété **Frequency \_ PerfTime** .</span><span class="sxs-lookup"><span data-stu-id="ffdef-144">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="ffdef-145">Une valeur peut être obtenue en appelant la fonction Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="ffdef-145">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="ffdef-146">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffdef-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="ffdef-147">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-147">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffdef-148">**Fréquence \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="ffdef-148">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffdef-149">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ffdef-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffdef-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffdef-151">Fréquence en graduations par seconde de la propriété **timestamp \_ Sys100NS** (10 millions).</span><span class="sxs-lookup"><span data-stu-id="ffdef-151">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="ffdef-152">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffdef-152">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="ffdef-153">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-153">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffdef-154">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ffdef-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffdef-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ffdef-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffdef-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-157">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="ffdef-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ffdef-158">Étiquette par laquelle la statistique ou la métrique est connue.</span><span class="sxs-lookup"><span data-stu-id="ffdef-158">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="ffdef-159">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="ffdef-159">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ffdef-160">Cette propriété est héritée de la [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-160">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffdef-161">**Timestamp, \_ objet**</span><span class="sxs-lookup"><span data-stu-id="ffdef-161">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffdef-162">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ffdef-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffdef-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffdef-164">Horodatage défini par l’objet.</span><span class="sxs-lookup"><span data-stu-id="ffdef-164">Object-defined timestamp.</span></span> <span data-ttu-id="ffdef-165">Le fournisseur définit sa propriété.</span><span class="sxs-lookup"><span data-stu-id="ffdef-165">The provider defines his property.</span></span>

<span data-ttu-id="ffdef-166">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffdef-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="ffdef-167">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-167">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffdef-168">**Horodateur \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="ffdef-168">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffdef-169">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ffdef-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffdef-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffdef-171">Horodateur du compteur de performances élevé.</span><span class="sxs-lookup"><span data-stu-id="ffdef-171">High Performance counter timestamp.</span></span> <span data-ttu-id="ffdef-172">Une valeur peut être obtenue en appelant la fonction Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="ffdef-172">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="ffdef-173">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffdef-173">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="ffdef-174">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-174">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffdef-175">**Horodateur \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="ffdef-175">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffdef-176">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ffdef-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ffdef-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ffdef-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffdef-178">Valeur d’horodatage en unités de nanosecondes de 100.</span><span class="sxs-lookup"><span data-stu-id="ffdef-178">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="ffdef-179">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffdef-179">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="ffdef-180">Cette propriété est héritée de la [**\_ performance Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-180">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffdef-181">Notes</span><span class="sxs-lookup"><span data-stu-id="ffdef-181">Remarks</span></span>

<span data-ttu-id="ffdef-182">La classe **Win32 \_ PerfRawData** est dérivée de la [**\_ performance Win32**](win32-perf.md), qui est dérivée de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-182">The **Win32\_PerfRawData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

<span data-ttu-id="ffdef-183">Toutes les classes dérivées de la [**\_ performance Win32**](win32-perf.md) sont conçues pour être utilisées avec un objet [*actualisateur*](../wmisdk/gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="ffdef-183">All classes derived from [**Win32\_Perf**](win32-perf.md) are designed to be used with a [*refresher*](../wmisdk/gloss-r.md) object.</span></span> <span data-ttu-id="ffdef-184">Pour plus d’informations sur la création et l’utilisation d’un objet actualisateur dans le langage de programmation C++, consultez [accès aux données de performances en c++](../wmisdk/accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-184">For more information about how to create and use a refresher object in the C++ programming language, see [Accessing Performance Data in C++](../wmisdk/accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="ffdef-185">Pour plus d’informations sur la création et l’utilisation d’un objet actualisateur dans un langage de programmation de scripts, consultez [actualisation des données WMI dans des scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="ffdef-185">For more information about how to create and use a refresher object in a script programming language, see [Refreshing WMI Data in Scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffdef-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffdef-186">Requirements</span></span>



| <span data-ttu-id="ffdef-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffdef-187">Requirement</span></span> | <span data-ttu-id="ffdef-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffdef-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffdef-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffdef-189">Minimum supported client</span></span><br/> | <span data-ttu-id="ffdef-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffdef-190">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="ffdef-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffdef-191">Minimum supported server</span></span><br/> | <span data-ttu-id="ffdef-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffdef-192">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="ffdef-193">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ffdef-193">Namespace</span></span><br/>                | <span data-ttu-id="ffdef-194">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ffdef-194">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="ffdef-195">MOF</span><span class="sxs-lookup"><span data-stu-id="ffdef-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffdef-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffdef-196"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="ffdef-197">DLL</span><span class="sxs-lookup"><span data-stu-id="ffdef-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffdef-198"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffdef-198"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffdef-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffdef-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffdef-200">**\_Performances Win32**</span><span class="sxs-lookup"><span data-stu-id="ffdef-200">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="ffdef-201">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="ffdef-201">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="ffdef-202">Accès aux classes de performance préinstallées par WMI</span><span class="sxs-lookup"><span data-stu-id="ffdef-202">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="ffdef-203">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="ffdef-203">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="ffdef-204">Accès aux données de performances dans le script</span><span class="sxs-lookup"><span data-stu-id="ffdef-204">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
