---
description: Les qualificateurs de propriété spécifient des informations sur le compteur de performance mappé à la propriété.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Qualificateurs de propriété pour les classes de compteur de performance
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e060d072c34d248f9faf634aec7710f5638721b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210420"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="17e01-103">Qualificateurs de propriété pour les classes de compteur de performance</span><span class="sxs-lookup"><span data-stu-id="17e01-103">Property Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="17e01-104">Les qualificateurs de propriété spécifient des informations sur le compteur de performance mappé à la propriété.</span><span class="sxs-lookup"><span data-stu-id="17e01-104">Property qualifiers specify information about the performance counter to which the property maps.</span></span>

-   [<span data-ttu-id="17e01-105">Qualificateurs de propriété pour les classes de performance brutes et mises en forme</span><span class="sxs-lookup"><span data-stu-id="17e01-105">Property Qualifiers for Raw and Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="17e01-106">Qualificateurs de propriété pour les classes de performance brutes</span><span class="sxs-lookup"><span data-stu-id="17e01-106">Property Qualifiers for Raw Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="17e01-107">Qualificateurs de propriété pour les classes de performance mises en forme</span><span class="sxs-lookup"><span data-stu-id="17e01-107">Property Qualifiers for Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="17e01-108">Comment interpréter les qualificateurs de propriété</span><span class="sxs-lookup"><span data-stu-id="17e01-108">How to Interpret Property Qualifiers</span></span>](#how-to-interpret-property-qualifiers)
-   [<span data-ttu-id="17e01-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17e01-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="17e01-110">Le compteur de performance fait partie d’un objet de performance représenté par un compteur de performance de la [classe compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI. les qualificateurs spécifiques sont automatiquement attachés par le fournisseur WbemPerfClass aux classes et propriétés [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) dans le \\ cimv2 racine.</span><span class="sxs-lookup"><span data-stu-id="17e01-110">The performance counter is part of a performance object represented by a WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) Performance counter–specific qualifiers are automatically attached by the WbemPerfClass provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="17e01-111">Ces informations s’appliquent à toutes les instances de la classe de performance.</span><span class="sxs-lookup"><span data-stu-id="17e01-111">This information applies to all instances of the performance class.</span></span> <span data-ttu-id="17e01-112">Certains qualificateurs avec des valeurs **booléennes** qui ont toujours la valeur false peuvent ne pas être présents sur des classes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="17e01-112">Some qualifiers with **Boolean** values that are always false may not be present on specific classes.</span></span>

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a><span data-ttu-id="17e01-113">Qualificateurs de propriété pour les classes de performance brutes et mises en forme</span><span class="sxs-lookup"><span data-stu-id="17e01-113">Property Qualifiers for Raw and Formatted Performance Classes</span></span>

<span data-ttu-id="17e01-114">La liste suivante répertorie les qualificateurs qui s’appliquent aux propriétés dans les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) ou [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="17e01-114">The following list lists qualifiers that apply to properties in classes that are derived either from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) or [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="17e01-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="17e01-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="17e01-116">**sint32**</span><span class="sxs-lookup"><span data-stu-id="17e01-116">**sint32**</span></span>

<span data-ttu-id="17e01-117">Valeur entière dans l’énumération de type de compteur, telle que définie dans Winperf. h ou Perflib. h.</span><span class="sxs-lookup"><span data-stu-id="17e01-117">Integer value in the counter type enumeration, as defined in Winperf.h or Perflib.h.</span></span> <span data-ttu-id="17e01-118">Le [**qualificateur de l’identificateur**](countertype-qualifier.md)de l’ordinateur indique la formule ou l’algorithme utilisé pour calculer la valeur affichée dans le moniteur système pour le compteur que la propriété représente.</span><span class="sxs-lookup"><span data-stu-id="17e01-118">The [**CounterType**](countertype-qualifier.md)qualifier indicates the formula or algorithm used to calculate the value shown in System Monitor for the counter which the property represents.</span></span>

</dd> <dt>

<span data-ttu-id="17e01-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="17e01-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="17e01-120">**string**</span><span class="sxs-lookup"><span data-stu-id="17e01-120">**string**</span></span>

<span data-ttu-id="17e01-121">Nom du compteur de performance, tel que spécifié par le programme d’assistance des données de performances (PDH).</span><span class="sxs-lookup"><span data-stu-id="17e01-121">The performance Counter name, as specified by Performance Data Helper (PDH).</span></span>

</dd> <dt>

<span data-ttu-id="17e01-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="17e01-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="17e01-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="17e01-123">**sint32**</span></span>

<span data-ttu-id="17e01-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="17e01-124">Not used.</span></span> <span data-ttu-id="17e01-125">Contient toujours la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="17e01-125">Always contains 0.</span></span>

</dd> <dt>

<span data-ttu-id="17e01-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="17e01-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="17e01-127">**sint32**</span><span class="sxs-lookup"><span data-stu-id="17e01-127">**sint32**</span></span>

<span data-ttu-id="17e01-128">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="17e01-128">Not used.</span></span> <span data-ttu-id="17e01-129">Contient toujours la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="17e01-129">Always contains 0.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a><span data-ttu-id="17e01-130">Qualificateurs de propriété pour les classes de performance brutes</span><span class="sxs-lookup"><span data-stu-id="17e01-130">Property Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="17e01-131">La liste suivante répertorie les qualificateurs qui s’appliquent à toutes les propriétés des classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="17e01-131">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="17e01-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="17e01-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="17e01-133">**boolean**</span><span class="sxs-lookup"><span data-stu-id="17e01-133">**boolean**</span></span>

<span data-ttu-id="17e01-134">Indique si cette propriété est le compteur par défaut à utiliser dans les zones de liste.</span><span class="sxs-lookup"><span data-stu-id="17e01-134">Indicates whether this property is the default counter to use in list boxes.</span></span> <span data-ttu-id="17e01-135">Ce qualificateur a pour valeur par défaut **false** pour les compteurs de Performance version 6,0, car ils ne fournissent pas de données pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="17e01-135">This qualifier defaults to **False** for Performance Counters Version 6.0 because they do not supply data for it.</span></span> <span data-ttu-id="17e01-136">Pour plus d’informations, consultez [Compteurs de performances](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="17e01-136">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="17e01-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="17e01-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span></span>
</dt> <dd>

<span data-ttu-id="17e01-138">**sint32**</span><span class="sxs-lookup"><span data-stu-id="17e01-138">**sint32**</span></span>

<span data-ttu-id="17e01-139">Puissance de 10 à utiliser pour l’affichage du compteur.</span><span class="sxs-lookup"><span data-stu-id="17e01-139">Power of 10 to use for display of the counter.</span></span> <span data-ttu-id="17e01-140">Pour zéro, la valeur maximale estimée est 10 ^ 0, ou 1.</span><span class="sxs-lookup"><span data-stu-id="17e01-140">For zero, the estimated maximum is 10^0, or 1.</span></span>

</dd> <dt>

<span data-ttu-id="17e01-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="17e01-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="17e01-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="17e01-142">**sint32**</span></span>

<span data-ttu-id="17e01-143">Niveau de connaissance de l’audience.</span><span class="sxs-lookup"><span data-stu-id="17e01-143">Audience level of knowledge.</span></span> <span data-ttu-id="17e01-144">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="17e01-144">Not used.</span></span> <span data-ttu-id="17e01-145">La valeur est toujours 100.</span><span class="sxs-lookup"><span data-stu-id="17e01-145">The value is always 100.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="17e01-146">Qualificateurs de propriété pour les classes de performance mises en forme</span><span class="sxs-lookup"><span data-stu-id="17e01-146">Property Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="17e01-147">La liste suivante répertorie les qualificateurs qui s’appliquent à toutes les propriétés des classes dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="17e01-147">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="17e01-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span><span class="sxs-lookup"><span data-stu-id="17e01-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span></span>
</dt> <dd>

<span data-ttu-id="17e01-149">**string**</span><span class="sxs-lookup"><span data-stu-id="17e01-149">**string**</span></span>

<span data-ttu-id="17e01-150">Type de formule utilisé pour produire le résultat.</span><span class="sxs-lookup"><span data-stu-id="17e01-150">Formula type used to produce the result.</span></span> <span data-ttu-id="17e01-151">Chaque type de compteur utilise les autres qualificateurs de propriété pour calculer le résultat affiché comme valeur de la propriété actuelle.</span><span class="sxs-lookup"><span data-stu-id="17e01-151">Each counter type uses the other property qualifiers to calculate the result shown as the value of the current property.</span></span> <span data-ttu-id="17e01-152">Les qualificateurs **Counter**, **PerfTimeStamp** et **PerfTimeFreq** sont mappés aux propriétés dans une classe brute qui fournit les données.</span><span class="sxs-lookup"><span data-stu-id="17e01-152">The **Counter**, **PerfTimeStamp**, and **PerfTimeFreq** qualifiers map to properties in a raw class which supply the data.</span></span>

<span data-ttu-id="17e01-153">Pour plus d’informations, consultez la rubrique sur le [qualificateur](countertype-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="17e01-153">For more information, see [CounterType Qualifier](countertype-qualifier.md).</span></span>

</dd> <dt>

<span data-ttu-id="17e01-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**)**</span><span class="sxs-lookup"><span data-stu-id="17e01-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter**</span></span>
</dt> <dd>

<span data-ttu-id="17e01-155">**string**</span><span class="sxs-lookup"><span data-stu-id="17e01-155">**string**</span></span>

<span data-ttu-id="17e01-156">Nom d’une propriété requise dans la classe brute correspondante à utiliser comme valeur de compteur dans la formule de cuisson.</span><span class="sxs-lookup"><span data-stu-id="17e01-156">Name of a required property in the corresponding raw class to use as the counter value in the cooking formula.</span></span> <span data-ttu-id="17e01-157">La valeur doit être le nom de propriété de la propriété de source de données dans la classe brute correspondante.</span><span class="sxs-lookup"><span data-stu-id="17e01-157">The value must be the property name of the data source property in the corresponding raw class.</span></span>

</dd> <dt>

<span data-ttu-id="17e01-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="17e01-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="17e01-159">**string**</span><span class="sxs-lookup"><span data-stu-id="17e01-159">**string**</span></span>

<span data-ttu-id="17e01-160">Nom d’une propriété dans une classe brute à utiliser comme fréquence dans la formule de cuisson.</span><span class="sxs-lookup"><span data-stu-id="17e01-160">Name of a property in a raw class to use as a frequency in the cooking formula.</span></span> <span data-ttu-id="17e01-161">La valeur par défaut appropriée au niveau de la classe sera utilisée si ce qualificateur n’est pas présent pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="17e01-161">The appropriate default value at the class level will be used if this qualifier is not present for the property.</span></span> <span data-ttu-id="17e01-162">La fréquence représente les graduations par seconde de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="17e01-162">The frequency represents the ticks per second of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="17e01-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="17e01-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span></span>
</dt> <dd>

<span data-ttu-id="17e01-164">**string**</span><span class="sxs-lookup"><span data-stu-id="17e01-164">**string**</span></span>

<span data-ttu-id="17e01-165">Nom d’une propriété dans une classe brute à utiliser comme horodateur dans la formule de cuisson.</span><span class="sxs-lookup"><span data-stu-id="17e01-165">Name of a property in a raw class to use as a timestamp in the cooking formula.</span></span> <span data-ttu-id="17e01-166">La valeur par défaut appropriée au niveau de la classe est utilisée si ce qualificateur n’est pas présent pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="17e01-166">The appropriate default value at the class level is used if this qualifier is not present for the property.</span></span> <span data-ttu-id="17e01-167">Un horodatage généré automatiquement peut introduire une erreur dans un calcul, car l’horodatage est une approximation et ne prend pas en compte la surcharge engendrée par le marshaling et la collecte de données réelle.</span><span class="sxs-lookup"><span data-stu-id="17e01-167">An automatically generated time stamp may introduce error in a calculation because the timestamp is an approximation and does not account for overhead incurred by marshaling and actual data collection.</span></span>

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a><span data-ttu-id="17e01-168">Comment interpréter les qualificateurs de propriété</span><span class="sxs-lookup"><span data-stu-id="17e01-168">How to Interpret Property Qualifiers</span></span>

<span data-ttu-id="17e01-169">Les propriétés dans les classes [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contiennent les données calculées fournies par le [fournisseur de données de performance mis en forme](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="17e01-169">Properties in the [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data supplied by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span> <span data-ttu-id="17e01-170">La valeur de la propriété est le résultat final calculé.</span><span class="sxs-lookup"><span data-stu-id="17e01-170">The property value is the final calculated result.</span></span> <span data-ttu-id="17e01-171">Les qualificateurs fournissent une recette.</span><span class="sxs-lookup"><span data-stu-id="17e01-171">The qualifiers supply a recipe.</span></span>

<span data-ttu-id="17e01-172">Les qualificateurs **Counter** et **base** pointent vers les sources de données et **CookingType** spécifie la formule utilisée pour produire le résultat.</span><span class="sxs-lookup"><span data-stu-id="17e01-172">The **Counter** and **Base** qualifiers point to the sources of data and **CookingType** specifies the formula used to produce the result.</span></span> <span data-ttu-id="17e01-173">L’horodateur et la fréquence d’échantillonnage proviennent également de la classe brute correspondante et sont nommés dans **PerfTimeStamp** et **PerfTimeFreq**.</span><span class="sxs-lookup"><span data-stu-id="17e01-173">The timestamp and sample frequency also come from the corresponding raw class and are named in **PerfTimeStamp** and **PerfTimeFreq**.</span></span>

<span data-ttu-id="17e01-174">Par exemple, l’une des classes mises en forme fournies par WMI, [**Win32 \_ PerfFormattedData \_ Perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contient une propriété nommée **AvgDiskBytesPerRead**.</span><span class="sxs-lookup"><span data-stu-id="17e01-174">For example, one of the formatted classes supplied by WMI, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contains a property named **AvgDiskBytesPerRead**.</span></span> <span data-ttu-id="17e01-175">Le nom de la propriété dans la classe mise en forme doit être identique à la propriété de la classe brute.</span><span class="sxs-lookup"><span data-stu-id="17e01-175">The name of the property in the formatted class must be the same as the property in the raw class.</span></span> <span data-ttu-id="17e01-176">La propriété **AvgDiskBytesPerRead** a les qualificateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="17e01-176">The **AvgDiskBytesPerRead** property has the following qualifiers.</span></span>

<span data-ttu-id="17e01-177">La liste suivante répertorie les qualificateurs de propriété disponibles pour les propriétés de toutes les classes dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="17e01-177">The following list lists the available property qualifiers for properties of all classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>



| <span data-ttu-id="17e01-178">Qualificateur</span><span class="sxs-lookup"><span data-stu-id="17e01-178">Qualifier</span></span>         | <span data-ttu-id="17e01-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="17e01-179">Value</span></span>                     |
|-------------------|---------------------------|
| <span data-ttu-id="17e01-180">**CookingType**</span><span class="sxs-lookup"><span data-stu-id="17e01-180">**CookingType**</span></span>   | <span data-ttu-id="17e01-181">moyenne de performances \_ \_ en bloc</span><span class="sxs-lookup"><span data-stu-id="17e01-181">PERF\_AVERAGE\_BULK</span></span>       |
| <span data-ttu-id="17e01-182">**Compteur**</span><span class="sxs-lookup"><span data-stu-id="17e01-182">**Counter**</span></span>       | <span data-ttu-id="17e01-183">AvgDiskBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="17e01-183">AvgDiskBytesPerRead</span></span>       |
| <span data-ttu-id="17e01-184">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="17e01-184">**PerfTimeStamp**</span></span> | <span data-ttu-id="17e01-185">Horodateur \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="17e01-185">Timestamp\_PerfTime</span></span>       |
| <span data-ttu-id="17e01-186">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="17e01-186">**PerfTimeFreq**</span></span>  | <span data-ttu-id="17e01-187">Fréquence \_ PerfTime</span><span class="sxs-lookup"><span data-stu-id="17e01-187">Frequency\_PerfTime</span></span>       |
| <span data-ttu-id="17e01-188">**PerfIndex**</span><span class="sxs-lookup"><span data-stu-id="17e01-188">**PerfIndex**</span></span>     | <span data-ttu-id="17e01-189">408</span><span class="sxs-lookup"><span data-stu-id="17e01-189">408</span></span>                       |
| <span data-ttu-id="17e01-190">**HelpIndex**</span><span class="sxs-lookup"><span data-stu-id="17e01-190">**HelpIndex**</span></span>     | <span data-ttu-id="17e01-191">409</span><span class="sxs-lookup"><span data-stu-id="17e01-191">409</span></span>                       |
| <span data-ttu-id="17e01-192">**Base**</span><span class="sxs-lookup"><span data-stu-id="17e01-192">**Base**</span></span>          | <span data-ttu-id="17e01-193">\_Base AvgDiskBytesPerRead</span><span class="sxs-lookup"><span data-stu-id="17e01-193">AvgDiskBytesPerRead\_Base</span></span> |



 

<span data-ttu-id="17e01-194">La propriété **AvgDiskBytesPerRead** indique le nombre moyen d’octets transférés à partir du disque pendant les opérations de lecture.</span><span class="sxs-lookup"><span data-stu-id="17e01-194">The **AvgDiskBytesPerRead** property reports the average number of bytes transferred from the disk during read operations.</span></span> <span data-ttu-id="17e01-195">La formule de la \_ moyenne des performances \_ est la suivante :</span><span class="sxs-lookup"><span data-stu-id="17e01-195">The formula for PERF\_AVERAGE\_BULK is:</span></span>

<span data-ttu-id="17e01-196">(Sample2-sample1)/(base sample2-base sample1)</span><span class="sxs-lookup"><span data-stu-id="17e01-196">(Sample2 - Sample1) / (Base Sample2 - Base Sample1)</span></span>

<span data-ttu-id="17e01-197">L’opération de lecture est échantillonnée à la fréquence spécifiée par **PerfTimeFreq** avec la valeur **PerfTimeStamp** indiquant l’exemple le plus récent.</span><span class="sxs-lookup"><span data-stu-id="17e01-197">The read operation is sampled at the frequency specified by **PerfTimeFreq** with the **PerfTimeStamp** value indicating the most recent sample.</span></span> <span data-ttu-id="17e01-198">Les données de compteur brutes en octets sont extraites de la propriété **AvgDiskBytesPerRead** de la classe [**\_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) .</span><span class="sxs-lookup"><span data-stu-id="17e01-198">The raw counter data in bytes is taken from the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class.</span></span> <span data-ttu-id="17e01-199">Le nombre de base de données d’opérations est extrait de la propriété de **\_ base AvgDiskBytesPerRead** dans cette même classe.</span><span class="sxs-lookup"><span data-stu-id="17e01-199">The base number of operations data is taken from the **AvgDiskBytesPerRead\_Base** property in that same class.</span></span>

<span data-ttu-id="17e01-200">Pour plus d’informations, consultez [obtention de données de performances statistiques](obtaining-statistical-performance-data.md) et [analyse des données de performances](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="17e01-200">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="17e01-201">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17e01-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17e01-202">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="17e01-202">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="17e01-203">Qualificateurs spécifiques aux classes de performance WMI</span><span class="sxs-lookup"><span data-stu-id="17e01-203">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="17e01-204">Classes du compteur de performances</span><span class="sxs-lookup"><span data-stu-id="17e01-204">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="17e01-205">Accès aux classes de performance préinstallées par WMI</span><span class="sxs-lookup"><span data-stu-id="17e01-205">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="17e01-206">Tâches WMI : analyse des performances</span><span class="sxs-lookup"><span data-stu-id="17e01-206">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
