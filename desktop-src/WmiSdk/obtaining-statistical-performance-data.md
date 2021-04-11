---
description: Dans WMI, vous pouvez définir des données de performances statistiques basées sur des données dans des classes de performance mises en forme dérivées de Win32 \_ PerfFormattedData. Les statistiques disponibles sont Average, minimum, maximum, Range et variance, comme défini dans types de compteurs statistiques.
ms.assetid: 5552d5fc-df8c-4353-8593-c106ee19dc84
ms.tgt_platform: multiple
title: Obtention de données de performances statistiques
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65892608e642b675440d81127ef9afa0badd1d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111959"
---
# <a name="obtaining-statistical-performance-data"></a><span data-ttu-id="19f9e-104">Obtention de données de performances statistiques</span><span class="sxs-lookup"><span data-stu-id="19f9e-104">Obtaining Statistical Performance Data</span></span>

<span data-ttu-id="19f9e-105">Dans WMI, vous pouvez définir des données de performances statistiques basées sur des données dans des classes de performance mises en forme dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="19f9e-105">In WMI, you can define statistical performance data based on data in formatted performance classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="19f9e-106">Les statistiques disponibles sont Average, minimum, maximum, Range et variance, comme défini dans [types de compteurs statistiques](statistical-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="19f9e-106">The available statistics are average, minimum, maximum, range, and variance, as defined in [Statistical Counter Types](statistical-counter-types.md).</span></span>

<span data-ttu-id="19f9e-107">La liste suivante répertorie les types de compteurs statistiques spéciaux :</span><span class="sxs-lookup"><span data-stu-id="19f9e-107">The following list includes the special statistical counter types:</span></span>

-   [<span data-ttu-id="19f9e-108">moyenne de cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="19f9e-108">COOKER\_AVERAGE</span></span>](cooker-average.md)
-   [<span data-ttu-id="19f9e-109">minimum de cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="19f9e-109">COOKER\_MIN</span></span>](cooker-min.md)
-   [<span data-ttu-id="19f9e-110">maximum de cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="19f9e-110">COOKER\_MAX</span></span>](cooker-max.md)
-   [<span data-ttu-id="19f9e-111">plage de cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="19f9e-111">COOKER\_RANGE</span></span>](cooker-range.md)
-   [<span data-ttu-id="19f9e-112">VARIANCE de la cuiseur \_</span><span class="sxs-lookup"><span data-stu-id="19f9e-112">COOKER\_VARIANCE</span></span>](cooker-variance.md)

<span data-ttu-id="19f9e-113">Les exemples suivants montrent comment :</span><span class="sxs-lookup"><span data-stu-id="19f9e-113">The following examples show how to:</span></span>

-   <span data-ttu-id="19f9e-114">Créez un fichier MOF qui définit une classe de données calculées.</span><span class="sxs-lookup"><span data-stu-id="19f9e-114">Create a MOF file that defines a class of calculated data.</span></span>
-   <span data-ttu-id="19f9e-115">Écrivez un script qui crée une instance de la classe et actualise périodiquement les données de l’instance avec les valeurs statistiques recalculées.</span><span class="sxs-lookup"><span data-stu-id="19f9e-115">Write a script that creates an instance of the class, and periodically refreshes the data in the instance with the recalculated statistical values.</span></span>

## <a name="mof-file"></a><span data-ttu-id="19f9e-116">Fichier MOF</span><span class="sxs-lookup"><span data-stu-id="19f9e-116">MOF File</span></span>

<span data-ttu-id="19f9e-117">L’exemple de code MOF suivant crée une classe de données calculée nommée **Win32 \_ PerfFormattedData \_ AvailableMBytes**.</span><span class="sxs-lookup"><span data-stu-id="19f9e-117">The following MOF code example creates a new calculated data class named **Win32\_PerfFormattedData\_AvailableMBytes**.</span></span> <span data-ttu-id="19f9e-118">Cette classe contient les données de la propriété **AvailableMBytes** de la classe brute [**Win32 \_ PerfRawData \_ perfos \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span><span class="sxs-lookup"><span data-stu-id="19f9e-118">This class contains data from the **AvailableMBytes** property of the raw class [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span></span> <span data-ttu-id="19f9e-119">La **classe Win32 \_ PerfFormattedData \_ AvailableBytes** définit les propriétés **Average**, **min**, **Max**, **Range** et **variance**.</span><span class="sxs-lookup"><span data-stu-id="19f9e-119">The **Win32\_PerfFormattedData\_AvailableBytes** class defines the properties **Average**, **Min**, **Max**, **Range**, and **Variance**.</span></span>

<span data-ttu-id="19f9e-120">Le fichier MOF utilise les [**qualificateurs de propriété pour les classes de compteur de performance mises en forme**](property-qualifiers-for-performance-counter-classes.md) pour définir la source de données de propriété et la formule de calcul.</span><span class="sxs-lookup"><span data-stu-id="19f9e-120">The MOF file uses the [**Property Qualifiers for Formatted Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md) to define the property data source and the calculation formula.</span></span>

-   <span data-ttu-id="19f9e-121">La propriété **moyenne** obtient des données brutes à partir de la [**\_ mémoire Win32 PerfRawData \_ perfos \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Propriété AvailableMBytes** .</span><span class="sxs-lookup"><span data-stu-id="19f9e-121">The **Average** property obtains raw data from the [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**AvailableMBytes** property.</span></span>
-   <span data-ttu-id="19f9e-122">Le **qualificateur** de compteur pour la propriété **moyenne** spécifie la source de données brutes.</span><span class="sxs-lookup"><span data-stu-id="19f9e-122">The Counter **qualifier** for the **Average** property specifies the raw data source.</span></span>
-   <span data-ttu-id="19f9e-123">Le qualificateur **CookingType** spécifie le nombre [ \_ minimal de cuiseurs](cooker-min.md) de la formule pour le calcul des données.</span><span class="sxs-lookup"><span data-stu-id="19f9e-123">The **CookingType** qualifier specifies the formula [COOKER\_MIN](cooker-min.md) for calculating the data.</span></span>
-   <span data-ttu-id="19f9e-124">Le qualificateur **SampleWindow** spécifie le nombre d’échantillons à prendre avant d’effectuer le calcul.</span><span class="sxs-lookup"><span data-stu-id="19f9e-124">The **SampleWindow** qualifier specifies how many samples to take before performing the calculation.</span></span>


```mof
// Store the new Win32_PerfFormattedData_MemoryStatistics
//     class in the Root\Cimv2 namespace
#pragma autorecover
#pragma namespace("\\\\.\\Root\\CimV2")

qualifier vendor:ToInstance;
qualifier guid:ToInstance;
qualifier displayname:ToInstance;
qualifier perfindex:ToInstance;
qualifier helpindex:ToInstance;
qualifier perfdetail:ToInstance;
qualifier countertype:ToInstance;
qualifier perfdefault:ToInstance;
qualifier defaultscale:ToInstance;

qualifier dynamic:ToInstance;
qualifier hiperf:ToInstance;
qualifier AutoCook:ToInstance;
qualifier AutoCook_RawClass:ToInstance;
qualifier CookingType:ToInstance;
qualifier Counter:ToInstance;


// Define the Win32_PerFormattedData_MemoryStatistics
//     class, derived from Win32_PerfFormattedData
[
  dynamic,
  // Name of formatted data provider: "WMIPerfInst" for Vista 
  //   and later
  provider("HiPerfCooker_v1"), 
  // Text that will identify new counter in Perfmon
  displayname("My Calculated Counter"),                            
  // A high performance class     
  Hiperf,
  // Contains calculated data 
  Cooked, 
  // Value must be 1 
  AutoCook(1), 
  // Raw performance class to get data for calculations
  AutoCook_RawClass("Win32_PerfRawData_PerfOS_Memory"),
  // Value must be 1        
  AutoCook_RawDefault(1),
  // Name of raw class property to use for timestamp in formulas 
  PerfSysTimeStamp("Timestamp_PerfTime"), 
  // Name of raw class property to use for frequency in formulas
  PerfSysTimeFreq("Frequency_PerfTime"), 
  // Name of raw class property to use for timestamp in formulas
  Perf100NSTimeStamp("Timestamp_Sys100NS"),
  // Name of raw class property to use for frequency in formulas
  Perf100NSTimeFreq("Frequency_Sys100NS"),
  // Name of raw class property to use for timestamp in formulas
  PerfObjTimeStamp("Timestamp_Object"),
  // Name of raw class property to use for frequency in formulas 
  PerfObjTimeFreq("Frequency_Object"),
  // Only one instance of class allowed in namespace
  singleton                                                   
]

class Win32_PerfFormattedData_MemoryStatistics
          : Win32_PerfFormattedData
{

// Define the properties for the class. 
// All the properties perform different
//     statistical operations on the same
//     property, AvailableMBytes, in the raw class

// Define the Average property,
//     which uses the "COOKER_AVERAGE" counter type and 
//     gets its data from the AvailableMBytes 
//     property in the raw class

    [
     CookingType("COOKER_AVERAGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Average = 0;

// Define the Min property, which uses
//     the "COOKER_MIN" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_MIN"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Min = 0;

// Define the Max property, which uses
//     the "COOKER_MAX" counter type and 
//     gets its data from the
//     AvailableMBytes property in the raw class

    [
     CookingType("COOKER_MAX"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Max = 0;

// Define the Range property, which uses
//     the "COOKER_RANGE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_RANGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Range = 0;

// Define the Variance property, which uses
//     the "COOKER_VARIANCE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_VARIANCE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Variance = 0;
};
```



## <a name="script"></a><span data-ttu-id="19f9e-125">Script</span><span class="sxs-lookup"><span data-stu-id="19f9e-125">Script</span></span>

<span data-ttu-id="19f9e-126">L’exemple de code de script suivant obtient des statistiques sur la mémoire disponible, en mégaoctets, à l’aide du fichier MOF créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="19f9e-126">The following script code example obtains statistics about available memory, in megabytes, using the MOF created previously.</span></span> <span data-ttu-id="19f9e-127">Le script utilise l’objet de script [**SWbemRefresher**](swbemrefresher.md) pour créer un actualisateur qui contient une instance de la classe Statistics créée par le fichier MOF, à savoir **Win32 \_ PerfFormattedData \_ MemoryStatistics**.</span><span class="sxs-lookup"><span data-stu-id="19f9e-127">The script uses the [**SWbemRefresher**](swbemrefresher.md) scripting object to create a refresher that contains one instance of the statistics class that the MOF file creates, which is **Win32\_PerfFormattedData\_MemoryStatistics**.</span></span> <span data-ttu-id="19f9e-128">Pour plus d’informations sur l’utilisation de scripts, consultez [actualisation des données WMI dans les scripts](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="19f9e-128">For more information about using scripts, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span> <span data-ttu-id="19f9e-129">Si vous travaillez en C++, consultez [accès aux données de performances en c++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="19f9e-129">If working in C++, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="19f9e-130">[**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) doit être appelé après l’obtention de l’élément à partir de l’appel à [**SWbemRefresher. Add**](swbemrefresher-add.md) , sinon le script échoue.</span><span class="sxs-lookup"><span data-stu-id="19f9e-130">[**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) must be called after obtaining the item from the call to [**SWbemRefresher.Add**](swbemrefresher-add.md) or the script will fail.</span></span> <span data-ttu-id="19f9e-131">[**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) doit être appelé avant d’entrer dans la boucle pour obtenir des valeurs de ligne de base, ou les propriétés statistiques sont égales à zéro (0) lors de la première passe.</span><span class="sxs-lookup"><span data-stu-id="19f9e-131">[**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) must be called before entering the loop to obtain baseline values, or the statistical properties is zero (0) on the first pass.</span></span>

 


```VB
' Connect to the Root\Cimv2 namespace
strComputer = "."
Set objService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Create a refresher
Set Refresher = CreateObject("WbemScripting.SWbemRefresher")
If Err <> 0 Then
WScript.Echo Err
WScript.Quit
End If

' Add the single instance of the statistics
'    class to the refresher
Set obMemoryStatistics = Refresher.Add(objService, _
    "Win32_PerfFormattedData_MemoryStatistics=@").Object

' Refresh once to obtain base values for cooking calculations
Refresher.Refresh

Const REFRESH_INTERVAL = 10

' Refresh every REFRESH_INTERVAL seconds 
For I=1 to 3
  WScript.Sleep REFRESH_INTERVAL * 1000
  Refresher.Refresh

  WScript.Echo "System memory statistics" _
      & "(Available Megabytes) " _
      & "for the past 100 seconds - pass " & i 
  WScript.Echo "Average = " _
     & obMemoryStatistics.Average & VBNewLine & "Max = " _
     & obMemoryStatistics.Max & VBNewLine & "Min = " _
     & obMemoryStatistics.Min & VBNewLine & "Range = " _ 
     & obMemoryStatistics.Range & VBNewLine & "Variance = " _
     & obMemoryStatistics.Variance 
Next
```



## <a name="running-the-script"></a><span data-ttu-id="19f9e-132">Exécution du script</span><span class="sxs-lookup"><span data-stu-id="19f9e-132">Running the Script</span></span>

<span data-ttu-id="19f9e-133">La procédure suivante décrit comment exécuter l’exemple.</span><span class="sxs-lookup"><span data-stu-id="19f9e-133">The following procedure describes how to run the example.</span></span>

<span data-ttu-id="19f9e-134">**Pour exécuter l’exemple de script**</span><span class="sxs-lookup"><span data-stu-id="19f9e-134">**To run the example script**</span></span>

1.  <span data-ttu-id="19f9e-135">Copiez le code MOF et le script dans les fichiers sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="19f9e-135">Copy both the MOF code and script to files on your computer.</span></span>
2.  <span data-ttu-id="19f9e-136">Donnez au fichier MOF une extension. mof et le fichier de script une description. vbs.</span><span class="sxs-lookup"><span data-stu-id="19f9e-136">Give the MOF file a .mof extension and the script file a .vbs description.</span></span>
3.  <span data-ttu-id="19f9e-137">Sur la ligne de commande, accédez au répertoire dans lequel les fichiers sont stockés, puis exécutez [**mofcomp**](mofcomp.md) sur le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="19f9e-137">On the command line, change to the directory where the files are stored, and run [**Mofcomp**](mofcomp.md) on the MOF file.</span></span> <span data-ttu-id="19f9e-138">Par exemple, si vous nommez le fichier *CalculatedData. mof*, la commande est **mofcomp** *CalculatedData. mof*</span><span class="sxs-lookup"><span data-stu-id="19f9e-138">For example, if you name the file *CalculatedData.mof*, then the command is **Mofcomp** *CalculatedData.mof*</span></span>
4.  <span data-ttu-id="19f9e-139">Exécutez le script.</span><span class="sxs-lookup"><span data-stu-id="19f9e-139">Run the script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19f9e-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="19f9e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19f9e-141">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="19f9e-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="19f9e-142">Accès aux classes de performance préinstallées par WMI</span><span class="sxs-lookup"><span data-stu-id="19f9e-142">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="19f9e-143">**Qualificateurs de propriété pour les classes de compteur de performance mises en forme**</span><span class="sxs-lookup"><span data-stu-id="19f9e-143">**Property Qualifiers for Formatted Performance Counter Classes**</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="19f9e-144">Types de compteurs statistiques</span><span class="sxs-lookup"><span data-stu-id="19f9e-144">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> </dl>

 

 
