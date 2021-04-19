---
description: Spécifiez les informations relatives à l’objet de performance auquel la classe de compteur de performance WMI est mappée.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Qualificateurs de classe pour les classes de compteurs de performances
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536761"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="427a8-103">Qualificateurs de classe pour les classes de compteurs de performances</span><span class="sxs-lookup"><span data-stu-id="427a8-103">Class Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="427a8-104">Les qualificateurs de classe spécifient des informations sur l’objet de performance auquel la [classe de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI est mappée.</span><span class="sxs-lookup"><span data-stu-id="427a8-104">Class qualifiers specify information about the performance object to which the WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) is mapped.</span></span> <span data-ttu-id="427a8-105">Pour plus d’informations, consultez [analyse des données de performances](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="427a8-105">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

-   [<span data-ttu-id="427a8-106">Qualificateurs pour les PerformanceClasses bruts et mis en forme</span><span class="sxs-lookup"><span data-stu-id="427a8-106">Qualifiers for Raw and Formatted PerformanceClasses</span></span>](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [<span data-ttu-id="427a8-107">Qualificateurs pour les classes de performances brutes</span><span class="sxs-lookup"><span data-stu-id="427a8-107">Qualifiers for Raw Performance Classes</span></span>](#)
-   [<span data-ttu-id="427a8-108">Qualificateurs pour les classes de performance mises en forme</span><span class="sxs-lookup"><span data-stu-id="427a8-108">Qualifiers for Formatted Performance Classes</span></span>](#)
-   [<span data-ttu-id="427a8-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="427a8-109">Related topics</span></span>](#related-topics)


<span data-ttu-id="427a8-110">Compteur de performances : les qualificateurs spécifiques sont automatiquement attachés par le fournisseur « WbemPerfClass » aux classes et propriétés [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) dans le \\ cimv2 racine.</span><span class="sxs-lookup"><span data-stu-id="427a8-110">Performance counter–specific qualifiers are automatically attached by the "WbemPerfClass" provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="427a8-111">Ces informations s’appliquent à toutes les instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="427a8-111">This information applies to all instances of the class.</span></span> <span data-ttu-id="427a8-112">Certains qualificateurs avec des valeurs **booléennes** qui ont toujours la **valeur false** peuvent ne pas être présents sur des classes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="427a8-112">Some qualifiers with **Boolean** values that are always **False** may not be present on specific classes.</span></span>

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a><span data-ttu-id="427a8-113">Qualificateurs pour les PerformanceClasses bruts et mis en forme</span><span class="sxs-lookup"><span data-stu-id="427a8-113">Qualifiers for Raw and Formatted PerformanceClasses</span></span>

<span data-ttu-id="427a8-114">Les qualificateurs suivants s’appliquent à toutes les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="427a8-114">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="427a8-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cuisson**</span><span class="sxs-lookup"><span data-stu-id="427a8-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cooked**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-116">**boolean**</span><span class="sxs-lookup"><span data-stu-id="427a8-116">**boolean**</span></span>

<span data-ttu-id="427a8-117">Indique si la classe contient des données cuisinées.</span><span class="sxs-lookup"><span data-stu-id="427a8-117">Indicates whether the class contains cooked data.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="427a8-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-119">**string**</span><span class="sxs-lookup"><span data-stu-id="427a8-119">**string**</span></span>

<span data-ttu-id="427a8-120">Nom de l’objet de performance.</span><span class="sxs-lookup"><span data-stu-id="427a8-120">Performance object name.</span></span> <span data-ttu-id="427a8-121">Pour plus d’informations, consultez [Compteurs de performances](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="427a8-121">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="427a8-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="427a8-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="427a8-123">**sint32**</span></span>

<span data-ttu-id="427a8-124">Ne fournit pas de données de détail.</span><span class="sxs-lookup"><span data-stu-id="427a8-124">Does not provide detail data.</span></span> <span data-ttu-id="427a8-125">Contient toujours la valeur 100.</span><span class="sxs-lookup"><span data-stu-id="427a8-125">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamique**</span><span class="sxs-lookup"><span data-stu-id="427a8-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-127">**boolean**</span><span class="sxs-lookup"><span data-stu-id="427a8-127">**boolean**</span></span>

<span data-ttu-id="427a8-128">Toujours défini sur **true** , car les instances sont toujours dynamiques.</span><span class="sxs-lookup"><span data-stu-id="427a8-128">Always set to **True** because instances are always dynamic.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span><span class="sxs-lookup"><span data-stu-id="427a8-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-130">**boolean**</span><span class="sxs-lookup"><span data-stu-id="427a8-130">**boolean**</span></span>

<span data-ttu-id="427a8-131">Indique si la classe provient d’une bibliothèque de performance héritée.</span><span class="sxs-lookup"><span data-stu-id="427a8-131">Indicates whether the class comes from a legacy performance library.</span></span> <span data-ttu-id="427a8-132">Toujours défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="427a8-132">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="427a8-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-134">**sint32**</span><span class="sxs-lookup"><span data-stu-id="427a8-134">**sint32**</span></span>

<span data-ttu-id="427a8-135">Les index ne sont plus valides.</span><span class="sxs-lookup"><span data-stu-id="427a8-135">Indexes are no longer valid.</span></span> <span data-ttu-id="427a8-136">Ce qualificateur est toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="427a8-136">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="427a8-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span></span> 
</dt> <dd>

<span data-ttu-id="427a8-138">**boolean**</span><span class="sxs-lookup"><span data-stu-id="427a8-138">**boolean**</span></span>

<span data-ttu-id="427a8-139">Indique que la classe est une classe haute performance.</span><span class="sxs-lookup"><span data-stu-id="427a8-139">Indicates that the class is a high-performance class.</span></span> <span data-ttu-id="427a8-140">Toujours défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="427a8-140">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Paramètres régionaux**</span><span class="sxs-lookup"><span data-stu-id="427a8-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="427a8-142">**sint32**</span></span>

<span data-ttu-id="427a8-143">Identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="427a8-143">Locale identifier.</span></span> <span data-ttu-id="427a8-144">La valeur est toujours 1033 (anglais des États-Unis).</span><span class="sxs-lookup"><span data-stu-id="427a8-144">Value is always 1033 (U.S. English).</span></span>

</dd> <dt>

<span data-ttu-id="427a8-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="427a8-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-146">**int32**</span><span class="sxs-lookup"><span data-stu-id="427a8-146">**int32**</span></span>

<span data-ttu-id="427a8-147">Les index ne sont plus valides.</span><span class="sxs-lookup"><span data-stu-id="427a8-147">Indexes are no longer valid.</span></span> <span data-ttu-id="427a8-148">Ce qualificateur est toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="427a8-148">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Moteur**</span><span class="sxs-lookup"><span data-stu-id="427a8-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-150">**string**</span><span class="sxs-lookup"><span data-stu-id="427a8-150">**string**</span></span>

<span data-ttu-id="427a8-151">Nom du fournisseur d’instance.</span><span class="sxs-lookup"><span data-stu-id="427a8-151">Name of the instance provider.</span></span> <span data-ttu-id="427a8-152">La valeur est « WbemPerfV2 ».</span><span class="sxs-lookup"><span data-stu-id="427a8-152">Value is "WbemPerfV2".</span></span>

</dd> <dt>

<span data-ttu-id="427a8-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span><span class="sxs-lookup"><span data-stu-id="427a8-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-154">**string**</span><span class="sxs-lookup"><span data-stu-id="427a8-154">**string**</span></span>

<span data-ttu-id="427a8-155">Nom du pilote dans la clé **de \_ \_ \\ CurrentControlSet \\ services de l’ordinateur local** , sous laquelle la clé de performance peut être localisée.</span><span class="sxs-lookup"><span data-stu-id="427a8-155">Name of the driver in the **HKEY\_LOCAL\_MACHINE\\CurrentControlSet\\Services** key, under which the performance key can be located.</span></span> <span data-ttu-id="427a8-156">Ce nom est également le nom du service qui fournit le compteur de performance.</span><span class="sxs-lookup"><span data-stu-id="427a8-156">This name is also the name of the service that provides the performance counter.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span><span class="sxs-lookup"><span data-stu-id="427a8-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-158">**boolean**</span><span class="sxs-lookup"><span data-stu-id="427a8-158">**boolean**</span></span>

<span data-ttu-id="427a8-159">Si la **valeur est true**, indique qu’il n’existe qu’une seule instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="427a8-159">If **True**, indicates that only a single instance of the class exists.</span></span>

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a><span data-ttu-id="427a8-160">Qualificateurs pour les classes de performances brutes</span><span class="sxs-lookup"><span data-stu-id="427a8-160">Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="427a8-161">Les qualificateurs suivants s’appliquent à toutes les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="427a8-161">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="427a8-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Réduis**</span><span class="sxs-lookup"><span data-stu-id="427a8-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costly**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-163">**boolean**</span><span class="sxs-lookup"><span data-stu-id="427a8-163">**boolean**</span></span>

<span data-ttu-id="427a8-164">Indique si l’obtention d’instances de cette classe est une opération coûteuse.</span><span class="sxs-lookup"><span data-stu-id="427a8-164">Indicates whether obtaining instances of this class is a costly operation.</span></span> <span data-ttu-id="427a8-165">Affectez toujours la valeur **true** pour les classes avec « \_ coûteux » ajouté à la fin du nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="427a8-165">Always set to **True** for classes with "\_Costly" appended to the end of the class name.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="427a8-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-167">**uint32**</span><span class="sxs-lookup"><span data-stu-id="427a8-167">**uint32**</span></span>

<span data-ttu-id="427a8-168">Ne fournit pas de données de détail.</span><span class="sxs-lookup"><span data-stu-id="427a8-168">Does not provide detail data.</span></span> <span data-ttu-id="427a8-169">Contient toujours la valeur 100.</span><span class="sxs-lookup"><span data-stu-id="427a8-169">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="427a8-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-171">**boolean**</span><span class="sxs-lookup"><span data-stu-id="427a8-171">**boolean**</span></span>

<span data-ttu-id="427a8-172">La valeur est toujours **false**.</span><span class="sxs-lookup"><span data-stu-id="427a8-172">Value is always **False**.</span></span>

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="427a8-173">Qualificateurs pour les classes de performance mises en forme</span><span class="sxs-lookup"><span data-stu-id="427a8-173">Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="427a8-174">Les qualificateurs suivants s’appliquent à toutes les classes dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="427a8-174">The following qualifiers apply to all classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="427a8-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Cook automatique**</span><span class="sxs-lookup"><span data-stu-id="427a8-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-176">**int32**</span><span class="sxs-lookup"><span data-stu-id="427a8-176">**int32**</span></span>

<span data-ttu-id="427a8-177">Indique que les valeurs des instances de classe sont calculées automatiquement à partir de la classe de données brutes correspondante.</span><span class="sxs-lookup"><span data-stu-id="427a8-177">Indicates that the values in class instances are automatically calculated from the corresponding raw data class.</span></span> <span data-ttu-id="427a8-178">La valeur est toujours 1.</span><span class="sxs-lookup"><span data-stu-id="427a8-178">Value is always 1.</span></span>

</dd> <dt>

<span data-ttu-id="427a8-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**RawClass autocook \_**</span><span class="sxs-lookup"><span data-stu-id="427a8-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook\_RawClass**</span></span>
</dt> <dd>

<span data-ttu-id="427a8-180">**string**</span><span class="sxs-lookup"><span data-stu-id="427a8-180">**string**</span></span>

<span data-ttu-id="427a8-181">Nom de la classe brute à utiliser pour le calcul de la classe mise en forme.</span><span class="sxs-lookup"><span data-stu-id="427a8-181">Name of the raw class to use for calculation for the formatted class.</span></span> <span data-ttu-id="427a8-182">Ce qualificateur est requis.</span><span class="sxs-lookup"><span data-stu-id="427a8-182">This qualifier is required.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="427a8-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="427a8-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="427a8-184">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="427a8-184">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="427a8-185">Qualificateurs spécifiques aux classes de performance WMI</span><span class="sxs-lookup"><span data-stu-id="427a8-185">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="427a8-186">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="427a8-186">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="427a8-187">Accès aux classes de performance préinstallées par WMI</span><span class="sxs-lookup"><span data-stu-id="427a8-187">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="427a8-188">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="427a8-188">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
