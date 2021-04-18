---
description: L’énumération est l’action consistant à passer par un ensemble d’objets et éventuellement à modifier chaque objet au fur et à mesure.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Énumération de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519038"
---
# <a name="enumerating-wmi"></a><span data-ttu-id="e15b2-103">Énumération de WMI</span><span class="sxs-lookup"><span data-stu-id="e15b2-103">Enumerating WMI</span></span>

<span data-ttu-id="e15b2-104">L’énumération est l’action consistant à passer par un ensemble d’objets et éventuellement à modifier chaque objet au fur et à mesure.</span><span class="sxs-lookup"><span data-stu-id="e15b2-104">Enumeration is the act of moving through a set of objects and possibly modifying each object as you do so.</span></span> <span data-ttu-id="e15b2-105">Par exemple, vous pouvez énumérer un ensemble d’objets [**\_ DiskDrive Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive) pour rechercher un numéro de série particulier.</span><span class="sxs-lookup"><span data-stu-id="e15b2-105">For example, you can enumerate through a set of [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) objects to find a particular serial number.</span></span> <span data-ttu-id="e15b2-106">Notez que même si vous pouvez énumérer n’importe quel objet, WMI retourne uniquement les objets pour lesquels vous disposez d’un accès de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e15b2-106">Note that although you can enumerate any object, WMI only returns objects to which you have security access.</span></span>

<span data-ttu-id="e15b2-107">Les énumérations de jeux de données volumineux peuvent nécessiter une grande quantité de ressources et nuire aux performances.</span><span class="sxs-lookup"><span data-stu-id="e15b2-107">Enumerations of large data sets can require a large amount of resources and degrade performance.</span></span> <span data-ttu-id="e15b2-108">Pour plus d’informations, consultez amélioration des performances de l' [énumération](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-108">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span> <span data-ttu-id="e15b2-109">Vous pouvez également demander des données avec une requête plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="e15b2-109">You also can request data with a more specific query.</span></span> <span data-ttu-id="e15b2-110">Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-110">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="e15b2-111">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="e15b2-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="e15b2-112">Énumération de WMI à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="e15b2-112">Enumerating WMI Using PowerShell</span></span>](#enumerating-wmi-using-powershell)
-   [<span data-ttu-id="e15b2-113">Énumération de WMI à l’aide de C# (Microsoft. Management. infrastructure)</span><span class="sxs-lookup"><span data-stu-id="e15b2-113">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [<span data-ttu-id="e15b2-114">Énumération de WMI à l’aide de C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="e15b2-114">Enumerating WMI Using C# (System.Management)</span></span>](#enumerating-wmi-using-c-systemmanagement)
-   [<span data-ttu-id="e15b2-115">Énumération de WMI à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="e15b2-115">Enumerating WMI Using VBScript</span></span>](#enumerating-wmi-using-vbscript)
-   [<span data-ttu-id="e15b2-116">Énumération de WMI à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="e15b2-116">Enumerating WMI Using C++</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a><span data-ttu-id="e15b2-117">Énumération de WMI à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="e15b2-117">Enumerating WMI Using PowerShell</span></span>

<span data-ttu-id="e15b2-118">Si vous ne connaissez pas le chemin d’accès de l’objet pour une instance spécifique, ou si vous souhaitez récupérer toutes les instances d’une classe spécifique [, utilisez la](https://technet.microsoft.com/library/dd315379.aspx)fonction de mise à niveau de l’objet avec le nom de la classe dans le paramètre *-Class* .</span><span class="sxs-lookup"><span data-stu-id="e15b2-118">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), with the name of the class in the *-class* parameter.</span></span> <span data-ttu-id="e15b2-119">Si vous souhaitez utiliser une requête, vous pouvez utiliser le paramètre *-query* .</span><span class="sxs-lookup"><span data-stu-id="e15b2-119">If you want to use a query, you can use the *-query* parameter.</span></span>

<span data-ttu-id="e15b2-120">La procédure suivante décrit comment énumérer les instances d’une classe à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e15b2-120">The following procedure describes how to enumerate the instances of a class using PowerShell.</span></span>

<span data-ttu-id="e15b2-121">**Pour énumérer les instances d’une classe à l’aide de PowerShell**</span><span class="sxs-lookup"><span data-stu-id="e15b2-121">**To enumerate the instances of a class using PowerShell**</span></span>

1.  <span data-ttu-id="e15b2-122">Énumérez les instances avec un appel à l’applet de commande [« obtenir-WmiObject »](https://technet.microsoft.com/library/dd315379.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e15b2-122">Enumerate the instances with a call to [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

    <span data-ttu-id="e15b2-123">L’accès [en fonction](https://technet.microsoft.com/library/dd315379.aspx) de la méthode obtient une collection d’un ou de plusieurs objets WMI par le biais desquels vous pouvez effectuer l’énumération.</span><span class="sxs-lookup"><span data-stu-id="e15b2-123">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) returns a collection of one or more WMI objects, through which you can enumerate.</span></span> <span data-ttu-id="e15b2-124">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-124">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

    <span data-ttu-id="e15b2-125">Si vous souhaitez récupérer une instance de classe WMI dans un autre espace de noms ou sur un autre ordinateur, spécifiez l’ordinateur et l’espace de noms respectivement dans les paramètres *-Computer* et *-namespace* .</span><span class="sxs-lookup"><span data-stu-id="e15b2-125">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *-computer* and *-namespace* parameters, respectively.</span></span> <span data-ttu-id="e15b2-126">Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="e15b2-127">Cela ne fonctionne que si vous disposez des privilèges d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="e15b2-127">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="e15b2-128">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md) et [exécution des opérations privilégiées](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-128">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="e15b2-129">Récupérez les instances individuelles que vous souhaitez à l’aide des membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="e15b2-129">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="e15b2-130">L’exemple de code suivant récupère une collection PowerShell, puis affiche la propriété Size pour toutes les instances de lecteurs logiques sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e15b2-130">The following code example retrieves an PowerShell collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a><span data-ttu-id="e15b2-131">Énumération de WMI à l’aide de C# (Microsoft. Management. infrastructure)</span><span class="sxs-lookup"><span data-stu-id="e15b2-131">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>

1.  <span data-ttu-id="e15b2-132">Ajoutez une référence à l’assembly de référence **Microsoft. Management. infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="e15b2-132">Add a reference to the **Microsoft.Management.Infrastructure** reference assembly.</span></span> <span data-ttu-id="e15b2-133">(Cet assembly est fourni avec le [Kit de développement logiciel (SDK) Windows pour Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)</span><span class="sxs-lookup"><span data-stu-id="e15b2-133">(This assembly ships as part of the [Windows Software Development Kit (SDK) for Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)</span></span>
2.  <span data-ttu-id="e15b2-134">Ajoutez une instruction **using** pour l’espace de noms **Microsoft. Management. infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="e15b2-134">Add a **using** statement for the **Microsoft.Management.Infrastructure** namespace.</span></span>

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  <span data-ttu-id="e15b2-135">Instanciez un objet [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e15b2-135">Instantiate a [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object.</span></span> <span data-ttu-id="e15b2-136">L’extrait de code suivant utilise la valeur standard « localhost » pour la méthode [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e15b2-136">The following snippet uses the standard "localhost" value for the [**CimSession.Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) method.</span></span>

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  <span data-ttu-id="e15b2-137">Appelez la méthode [**CimSession. QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) en passant l’espace de noms CIM souhaité et WQL à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e15b2-137">Call the [**CimSession.QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) method passing the desired CIM namespace and WQL to use.</span></span> <span data-ttu-id="e15b2-138">L’extrait de code suivant retourne deux instances représentant deux processus Windows standard où la propriété handle (représentant un ID de processus, ou PID) a la valeur 0 ou 4.</span><span class="sxs-lookup"><span data-stu-id="e15b2-138">The following snippet will return two instances representing two standard Windows processes where the handle property (representing a process ID, or PID) has a value of either 0 or 4.</span></span>

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  <span data-ttu-id="e15b2-139">Parcourez les objets [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) retournés.</span><span class="sxs-lookup"><span data-stu-id="e15b2-139">Loop through the returned [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) objects.</span></span>

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

<span data-ttu-id="e15b2-140">L’exemple de code suivant énumère toutes les instances de la classe [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) (qui représentent les processus actifs) sur l’ordinateur local et imprime le nom de chaque processus.</span><span class="sxs-lookup"><span data-stu-id="e15b2-140">The following code sample enumerates all instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class (which represents active processes) on the local machine, and prints the name of each process.</span></span>

> [!Note]  
> <span data-ttu-id="e15b2-141">Dans une application réelle, vous devez définir comme paramètres le nom de l’ordinateur (« localhost ») et l’espace de noms CIM (« root \\ cimv2 »).</span><span class="sxs-lookup"><span data-stu-id="e15b2-141">In a real application you would define as parameters the computer name ("localhost") and CIM namespace ("root\\cimv2").</span></span> <span data-ttu-id="e15b2-142">À des fins de simplicité, elles ont été codées en dur dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="e15b2-142">For purposes of simplicity, these have been hardcoded in this example.</span></span>

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a><span data-ttu-id="e15b2-143">Énumération de WMI à l’aide de C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="e15b2-143">Enumerating WMI Using C# (System.Management)</span></span>

<span data-ttu-id="e15b2-144">Si vous ne connaissez pas le chemin d’accès de l’objet pour une instance spécifique, ou si vous souhaitez récupérer toutes les instances d’une classe spécifique, utilisez l’objet [ManagementClass](/dotnet/api/system.management.managementclass) pour récupérer un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) qui contient toutes les instances d’une classe donnée dans l’espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="e15b2-144">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [ManagementClass](/dotnet/api/system.management.managementclass) object to retrieve a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains all instances of a given class in the WMI namespace.</span></span> <span data-ttu-id="e15b2-145">Vous pouvez également interroger WMI via un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) pour obtenir le même jeu d’objets.</span><span class="sxs-lookup"><span data-stu-id="e15b2-145">Alternately, you can query WMI through a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) to obtain the same set of objects.</span></span>

> [!Note]  
> <span data-ttu-id="e15b2-146">**System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.</span><span class="sxs-lookup"><span data-stu-id="e15b2-146">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="e15b2-147">La procédure suivante décrit comment énumérer les instances d’une classe à l’aide de C#.</span><span class="sxs-lookup"><span data-stu-id="e15b2-147">The following procedure describes how to enumerate the instances of a class using C#.</span></span>

<span data-ttu-id="e15b2-148">**Pour énumérer les instances d’une classe à l’aide de C #**</span><span class="sxs-lookup"><span data-stu-id="e15b2-148">**To enumerate the instances of a class using C#**</span></span>

1.  <span data-ttu-id="e15b2-149">Énumérez les instances avec un appel à [ManagementClass. GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span><span class="sxs-lookup"><span data-stu-id="e15b2-149">Enumerate the instances with a call to [ManagementClass.GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span></span>

    <span data-ttu-id="e15b2-150">La méthode [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) retourne une collection ou un ensemble d’objets par le biais desquels vous pouvez effectuer l’énumération.</span><span class="sxs-lookup"><span data-stu-id="e15b2-150">The [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="e15b2-151">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-151">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="e15b2-152">La collection retournée est en fait un objet [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) , de sorte que toutes les méthodes de cet objet peuvent être appelées.</span><span class="sxs-lookup"><span data-stu-id="e15b2-152">The returned collection is actually an [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="e15b2-153">Si vous souhaitez récupérer une instance de classe WMI dans un autre espace de noms ou sur un autre ordinateur, spécifiez l’ordinateur et l’espace de noms dans le paramètre *path* .</span><span class="sxs-lookup"><span data-stu-id="e15b2-153">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *path* parameter.</span></span> <span data-ttu-id="e15b2-154">Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-154">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="e15b2-155">Cela ne fonctionne que si vous disposez des privilèges d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="e15b2-155">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="e15b2-156">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md) et [exécution des opérations privilégiées](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-156">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="e15b2-157">Récupérez les instances individuelles que vous souhaitez à l’aide des membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="e15b2-157">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="e15b2-158">L’exemple de code suivant récupère une collection C#, puis affiche la propriété Size pour toutes les instances de lecteurs logiques sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e15b2-158">The following code example retrieves an C# collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a><span data-ttu-id="e15b2-159">Énumération de WMI à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="e15b2-159">Enumerating WMI Using VBScript</span></span>

<span data-ttu-id="e15b2-160">Si vous ne connaissez pas le chemin d’accès de l’objet pour une instance spécifique, ou si vous souhaitez récupérer toutes les instances d’une classe spécifique, utilisez la méthode [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) pour retourner une énumération [**SWbemObjectSet**](swbemobjectset.md) de toutes les instances d’une classe.</span><span class="sxs-lookup"><span data-stu-id="e15b2-160">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method to return an [**SWbemObjectSet**](swbemobjectset.md) enumeration of all the instances of a class.</span></span> <span data-ttu-id="e15b2-161">Vous pouvez également interroger WMI via [**SWbemServices.ExecQuery**](swbemservices-execquery.md) pour obtenir le même jeu d’objets.</span><span class="sxs-lookup"><span data-stu-id="e15b2-161">Alternatively you can query WMI through [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to obtain the same set of objects.</span></span>

<span data-ttu-id="e15b2-162">La procédure suivante décrit comment énumérer les instances d’une classe à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="e15b2-162">The following procedure describes how to enumerate the instances of a class using VBScript.</span></span>

<span data-ttu-id="e15b2-163">**Pour énumérer les instances d’une classe à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="e15b2-163">**To enumerate the instances of a class using VBScript**</span></span>

1.  <span data-ttu-id="e15b2-164">Énumérez les instances avec un appel à la méthode [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) .</span><span class="sxs-lookup"><span data-stu-id="e15b2-164">Enumerate the instances with a call to the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method.</span></span>

    <span data-ttu-id="e15b2-165">La méthode [**InstancesOf**](swbemservices-instancesof.md) retourne une collection ou un ensemble d’objets par le biais desquels vous pouvez effectuer l’énumération.</span><span class="sxs-lookup"><span data-stu-id="e15b2-165">The [**InstancesOf**](swbemservices-instancesof.md) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="e15b2-166">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-166">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="e15b2-167">La collection retournée est en fait un objet [**SWbemObjectSet**](swbemobjectset.md) , de sorte que toutes les méthodes de cet objet peuvent être appelées.</span><span class="sxs-lookup"><span data-stu-id="e15b2-167">The returned collection is actually an [**SWbemObjectSet**](swbemobjectset.md) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="e15b2-168">Si vous souhaitez récupérer une instance de classe WMI dans un autre espace de noms ou sur un autre ordinateur, spécifiez l’ordinateur et l’espace de noms dans le moniker.</span><span class="sxs-lookup"><span data-stu-id="e15b2-168">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the moniker.</span></span> <span data-ttu-id="e15b2-169">Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-169">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="e15b2-170">Cela ne fonctionne que si vous disposez des privilèges d’accès appropriés.</span><span class="sxs-lookup"><span data-stu-id="e15b2-170">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="e15b2-171">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md) et [exécution des opérations privilégiées](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-171">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="e15b2-172">Récupérez toutes les instances individuelles que vous souhaitez à l’aide des méthodes regroupements.</span><span class="sxs-lookup"><span data-stu-id="e15b2-172">Retrieve any individual instances you wish using the collections methods.</span></span>

<span data-ttu-id="e15b2-173">L’exemple de code suivant récupère un objet [**SWbemServices**](swbemservices.md) , puis exécute la méthode [**InstancesOf**](swbemservices-instancesof.md) pour afficher la propriété Size pour toutes les instances de lecteurs logiques sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e15b2-173">The following code example retrieves an [**SWbemServices**](swbemservices.md) object and then executes the [**InstancesOf**](swbemservices-instancesof.md) method to display the size property for all instances of logical drives on the local computer.</span></span>


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a><span data-ttu-id="e15b2-174">Énumération de WMI à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="e15b2-174">Enumerating WMI Using C++</span></span>

<span data-ttu-id="e15b2-175">Outre l’exécution de l’énumération de base, vous pouvez définir plusieurs indicateurs et propriétés afin d’augmenter les performances de votre énumération.</span><span class="sxs-lookup"><span data-stu-id="e15b2-175">In addition to performing basic enumeration, you can set several flags and properties to increase the performance of your enumeration.</span></span> <span data-ttu-id="e15b2-176">Pour plus d’informations, consultez amélioration des performances de l' [énumération](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-176">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span>

<span data-ttu-id="e15b2-177">**Pour énumérer un jeu d’objets dans WMI**</span><span class="sxs-lookup"><span data-stu-id="e15b2-177">**To enumerate an object set in WMI**</span></span>

1.  <span data-ttu-id="e15b2-178">Créez une interface [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) décrivant l’ensemble d’objets que vous souhaitez énumérer.</span><span class="sxs-lookup"><span data-stu-id="e15b2-178">Create an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface describing the set of objects you wish to enumerate.</span></span>

    <span data-ttu-id="e15b2-179">Un objet [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) contient une liste décrivant un ensemble d’objets WMI.</span><span class="sxs-lookup"><span data-stu-id="e15b2-179">An [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object contains a list describing a set of WMI objects.</span></span> <span data-ttu-id="e15b2-180">Vous pouvez utiliser les méthodes **IEnumWbemClassObject** pour énumérer les transferts, ignorer les objets, commencer au début et copier l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="e15b2-180">You can use the **IEnumWbemClassObject** methods to enumerate forwards, skip objects, begin at the beginning, and copy the enumerator.</span></span> <span data-ttu-id="e15b2-181">Le tableau suivant répertorie les méthodes utilisées pour créer des énumérateurs pour différents types d’objets WMI.</span><span class="sxs-lookup"><span data-stu-id="e15b2-181">The following table lists the methods use to create enumerators for different types of WMI objects.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="e15b2-182">Object</span><span class="sxs-lookup"><span data-stu-id="e15b2-182">Object</span></span></th>
    <th><span data-ttu-id="e15b2-183">Méthode</span><span class="sxs-lookup"><span data-stu-id="e15b2-183">Method</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e15b2-184">Classe</span><span class="sxs-lookup"><span data-stu-id="e15b2-184">Class</span></span></td>
    <td><dl><span data-ttu-id="e15b2-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices :: CreateClassEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="e15b2-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices::CreateClassEnum</strong></a></span></span><br />
<span data-ttu-id="e15b2-186">[<strong>IWbemServices :: CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span><span class="sxs-lookup"><span data-stu-id="e15b2-186">[<strong>IWbemServices::CreateClassEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e15b2-187">Instance</span><span class="sxs-lookup"><span data-stu-id="e15b2-187">Instance</span></span></td>
    <td><dl><span data-ttu-id="e15b2-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices :: CreateInstanceEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="e15b2-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices::CreateInstanceEnum</strong></a></span></span><br />
<span data-ttu-id="e15b2-189">[<strong>IWbemServices :: CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span><span class="sxs-lookup"><span data-stu-id="e15b2-189">[<strong>IWbemServices::CreateInstanceEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e15b2-190">Résultat de la requête</span><span class="sxs-lookup"><span data-stu-id="e15b2-190">Query result</span></span></td>
    <td><dl><span data-ttu-id="e15b2-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices :: ExecQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="e15b2-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices::ExecQuery</strong></a></span></span><br />
<span data-ttu-id="e15b2-192">[<strong>IWbemServices :: ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span><span class="sxs-lookup"><span data-stu-id="e15b2-192">[<strong>IWbemServices::ExecQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e15b2-193">Notification d'événement</span><span class="sxs-lookup"><span data-stu-id="e15b2-193">Event notification</span></span></td>
    <td><dl><span data-ttu-id="e15b2-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices :: ExecNotificationQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="e15b2-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices::ExecNotificationQuery</strong></a></span></span><br />
<span data-ttu-id="e15b2-195">[<strong>IWbemServices :: ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span><span class="sxs-lookup"><span data-stu-id="e15b2-195">[<strong>IWbemServices::ExecNotificationQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="e15b2-196">Parcourez l’énumération retournée à l’aide de plusieurs appels à [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) ou [**IEnumWbemClassObject :: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span><span class="sxs-lookup"><span data-stu-id="e15b2-196">Traverse through the returned enumeration using multiple calls to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span></span>

<span data-ttu-id="e15b2-197">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="e15b2-197">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 
