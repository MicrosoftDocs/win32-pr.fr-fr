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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008249"
---
# <a name="obtaining-statistical-performance-data"></a>Obtention de données de performances statistiques

Dans WMI, vous pouvez définir des données de performances statistiques basées sur des données dans des classes de performance mises en forme dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Les statistiques disponibles sont Average, minimum, maximum, Range et variance, comme défini dans [types de compteurs statistiques](statistical-counter-types.md).

La liste suivante répertorie les types de compteurs statistiques spéciaux :

-   [moyenne de cuiseur \_](cooker-average.md)
-   [minimum de cuiseur \_](cooker-min.md)
-   [maximum de cuiseur \_](cooker-max.md)
-   [plage de cuiseur \_](cooker-range.md)
-   [VARIANCE de la cuiseur \_](cooker-variance.md)

Les exemples suivants montrent comment :

-   Créez un fichier MOF qui définit une classe de données calculées.
-   Écrivez un script qui crée une instance de la classe et actualise périodiquement les données de l’instance avec les valeurs statistiques recalculées.

## <a name="mof-file"></a>Fichier MOF

L’exemple de code MOF suivant crée une classe de données calculée nommée **Win32 \_ PerfFormattedData \_ AvailableMBytes**. Cette classe contient les données de la propriété **AvailableMBytes** de la classe brute [**Win32 \_ PerfRawData \_ perfos \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data). La **classe Win32 \_ PerfFormattedData \_ AvailableBytes** définit les propriétés **Average**, **min**, **Max**, **Range** et **variance**.

Le fichier MOF utilise les [**qualificateurs de propriété pour les classes de compteur de performance mises en forme**](property-qualifiers-for-performance-counter-classes.md) pour définir la source de données de propriété et la formule de calcul.

-   La propriété **moyenne** obtient des données brutes à partir de la [**\_ mémoire Win32 PerfRawData \_ perfos \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Propriété AvailableMBytes** .
-   Le **qualificateur** de compteur pour la propriété **moyenne** spécifie la source de données brutes.
-   Le qualificateur **CookingType** spécifie le nombre [ \_ minimal de cuiseurs](cooker-min.md) de la formule pour le calcul des données.
-   Le qualificateur **SampleWindow** spécifie le nombre d’échantillons à prendre avant d’effectuer le calcul.


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



## <a name="script"></a>Script

L’exemple de code de script suivant obtient des statistiques sur la mémoire disponible, en mégaoctets, à l’aide du fichier MOF créé précédemment. Le script utilise l’objet de script [**SWbemRefresher**](swbemrefresher.md) pour créer un actualisateur qui contient une instance de la classe Statistics créée par le fichier MOF, à savoir **Win32 \_ PerfFormattedData \_ MemoryStatistics**. Pour plus d’informations sur l’utilisation de scripts, consultez [actualisation des données WMI dans les scripts](refreshing-wmi-data-in-scripts.md). Si vous travaillez en C++, consultez [accès aux données de performances en c++](accessing-performance-data-in-c--.md).

> [!Note]  
> [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) doit être appelé après l’obtention de l’élément à partir de l’appel à [**SWbemRefresher. Add**](swbemrefresher-add.md) , sinon le script échoue. [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) doit être appelé avant d’entrer dans la boucle pour obtenir des valeurs de ligne de base, ou les propriétés statistiques sont égales à zéro (0) lors de la première passe.

 


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



## <a name="running-the-script"></a>Exécution du script

La procédure suivante décrit comment exécuter l’exemple.

**Pour exécuter l’exemple de script**

1.  Copiez le code MOF et le script dans les fichiers sur votre ordinateur.
2.  Donnez au fichier MOF une extension. mof et le fichier de script une description. vbs.
3.  Sur la ligne de commande, accédez au répertoire dans lequel les fichiers sont stockés, puis exécutez [**mofcomp**](mofcomp.md) sur le fichier MOF. Par exemple, si vous nommez le fichier *CalculatedData. mof*, la commande est **mofcomp** *CalculatedData. mof*
4.  Exécutez le script.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> <dt>

[Accès aux classes de performance préinstallées par WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[**Qualificateurs de propriété pour les classes de compteur de performance mises en forme**](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Types de compteurs statistiques](statistical-counter-types.md)
</dt> </dl>

 

 
