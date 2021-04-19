---
description: Le premier type d’objet que vous pouvez récupérer est une classe WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Récupération d’une classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106543552"
---
# <a name="retrieving-a-wmi-class"></a><span data-ttu-id="43ab1-103">Récupération d’une classe WMI</span><span class="sxs-lookup"><span data-stu-id="43ab1-103">Retrieving a WMI Class</span></span>

<span data-ttu-id="43ab1-104">Le premier type d’objet que vous pouvez récupérer est une classe WMI.</span><span class="sxs-lookup"><span data-stu-id="43ab1-104">The first type of object you can retrieve is a WMI class.</span></span> <span data-ttu-id="43ab1-105">Lorsque vous récupérez une classe WMI, vous récupérez en fait une définition de classe, qui est une liste des propriétés, des qualificateurs et des méthodes qui décrivent entièrement la classe.</span><span class="sxs-lookup"><span data-stu-id="43ab1-105">When retrieving a WMI class, you actually retrieve a class definition, which is a listing of the properties, qualifiers, and methods that fully describe the class.</span></span> <span data-ttu-id="43ab1-106">Toutefois, une définition de classe est fondamentalement la classe elle-même.</span><span class="sxs-lookup"><span data-stu-id="43ab1-106">However, a class definition is basically the class itself.</span></span>

<span data-ttu-id="43ab1-107">PowerShell utilise une requête standard pour récupérer les définitions de classe, à l’aide de la classe **meta \_ Class** .</span><span class="sxs-lookup"><span data-stu-id="43ab1-107">PowerShell uses a standard query to retrieve class definitions, using the **meta\_class** class.</span></span>

<span data-ttu-id="43ab1-108">**Pour récupérer une définition de classe dans PowerShell**</span><span class="sxs-lookup"><span data-stu-id="43ab1-108">**To retrieve a class definition in PowerShell**</span></span>

-   <span data-ttu-id="43ab1-109">Utilisez la clause with [-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) avec une requête to **meta \_ Class**, avec la clause WHERE contenant le nom de la classe que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="43ab1-109">Use the [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    <span data-ttu-id="43ab1-110">L’applet de commande is [-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) est l’applet de commande standard utilisée par PowerShell pour récupérer des informations de classes et d’instances à partir de WMI.</span><span class="sxs-lookup"><span data-stu-id="43ab1-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) is the standard cmdlet PowerShell uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="43ab1-111">La classe de la **\_ classe Meta** définit la requête en tant que requête de schéma.</span><span class="sxs-lookup"><span data-stu-id="43ab1-111">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="43ab1-112">Sans la classe de la classe **meta \_** , cette requête retourne toutes les instances de \_ disque logique Win32.</span><span class="sxs-lookup"><span data-stu-id="43ab1-112">Without the **meta\_class** class, this query would return all instances of Win32\_LogicalDisk.</span></span> <span data-ttu-id="43ab1-113">Pour plus d’informations sur l’interrogation de WMI, consultez [instruction SELECT pour les requêtes de schéma](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="43ab1-113">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="43ab1-114">Le processus actuel de récupération d’une définition WMI en C# consiste à utiliser la classe **CIMInstance** .</span><span class="sxs-lookup"><span data-stu-id="43ab1-114">The current process for retrieving a WMI definition in C# is to use **CIMInstance** class.</span></span>

<span data-ttu-id="43ab1-115">**Pour récupérer une définition de classe en C# (Microsoft. Management. infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="43ab1-115">**To retrieve a class definition in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="43ab1-116">À l’aide de l’espace de noms **Microsoft. Management. infrastructure** , créez une classe **CIMInstance** avec l’espace de noms et le nom de classe spécifiés.</span><span class="sxs-lookup"><span data-stu-id="43ab1-116">Using the **Microsoft.Management.Infrastructure** namespace, create a **CIMInstance** class with the specified namespace and class name.</span></span>

    <span data-ttu-id="43ab1-117">La classe créée contient toutes les informations de classe, mais pas de données d’instance.</span><span class="sxs-lookup"><span data-stu-id="43ab1-117">The created class will contain all of the class information, but no instance data.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="43ab1-118">Comme avec PowerShell, vous pouvez également exécuter une requête à l’aide de la balise **meta \_ Class** dans le cadre de la requête.</span><span class="sxs-lookup"><span data-stu-id="43ab1-118">Alternately, as with PowerShell, you could also perform a query, using the **meta\_class** tag as part of the query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

<span data-ttu-id="43ab1-119">Comme avec PowerShell, C# utilise une requête de **méta- \_ classe** pour récupérer les définitions de classe.</span><span class="sxs-lookup"><span data-stu-id="43ab1-119">As with PowerShell, C# uses a **meta\_class** query to retrieve class definitions.</span></span> <span data-ttu-id="43ab1-120">Vous pouvez également créer un objet **ManagementClass** pour accéder directement à la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="43ab1-120">Alternately, you can create a **ManagementClass** object to access the class definition directly.</span></span>

> [!Note]  
> <span data-ttu-id="43ab1-121">**System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.</span><span class="sxs-lookup"><span data-stu-id="43ab1-121">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="43ab1-122">**Pour récupérer une définition de classe en C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="43ab1-122">**To retrieve a class definition in C# (System.Management)**</span></span>

1.  <span data-ttu-id="43ab1-123">Vous pouvez utiliser [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) avec une requête à la **\_ classe Meta**, avec la clause WHERE contenant le nom de la classe que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="43ab1-123">You can use the [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    <span data-ttu-id="43ab1-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) est la classe standard utilisée par .net pour récupérer des informations de classes et d’instances à partir de WMI.</span><span class="sxs-lookup"><span data-stu-id="43ab1-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) is the standard class .NET uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="43ab1-125">[ManagementObjectSerarcher. obtenir](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) retourne un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) qui contient la classe de définition de schéma.</span><span class="sxs-lookup"><span data-stu-id="43ab1-125">[ManagementObjectSerarcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains the schema definition class.</span></span> <span data-ttu-id="43ab1-126">La classe de la **\_ classe Meta** définit la requête en tant que requête de schéma.</span><span class="sxs-lookup"><span data-stu-id="43ab1-126">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="43ab1-127">Sans la classe de la classe **\_ meta** , cette requête retourne toutes les instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="43ab1-127">Without the **meta\_class** class, this query would return all instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="43ab1-128">Pour plus d’informations sur l’interrogation de WMI, consultez [instruction SELECT pour les requêtes de schéma](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="43ab1-128">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

2.  <span data-ttu-id="43ab1-129">Vous pouvez également créer un nouvel objet [ManagementClass](/dotnet/api/system.management.managementclass) , avec le nom comme chemin d’accès, pour récupérer la classe.</span><span class="sxs-lookup"><span data-stu-id="43ab1-129">Alternately, create a new [ManagementClass](/dotnet/api/system.management.managementclass) object, with the name as the path, to retrieve the class.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

<span data-ttu-id="43ab1-130">Vous pouvez récupérer une définition de classe dans VBScript de la même façon pour récupérer une instance spécifique.</span><span class="sxs-lookup"><span data-stu-id="43ab1-130">You can retrieve a class definition in VBScript in a similar way to retrieving a specific instance.</span></span>

<span data-ttu-id="43ab1-131">**Pour récupérer une définition de classe dans VBScript**</span><span class="sxs-lookup"><span data-stu-id="43ab1-131">**To retrieve a class definition in VBScript**</span></span>

1.  <span data-ttu-id="43ab1-132">Appelez [**SWbemServices. obtenir**](swbemservices-get.md) mais n’identifiez pas une instance spécifique dans le chemin d’accès de l’objet pour la classe.</span><span class="sxs-lookup"><span data-stu-id="43ab1-132">Call [**SWbemServices.Get**](swbemservices-get.md) but do not identify a specific instance in the object path for the class.</span></span>
2.  <span data-ttu-id="43ab1-133">L’exemple de code suivant récupère la définition de classe pour la classe qui décrit les lecteurs logiques sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="43ab1-133">The following code example retrieves the class definition for the class that describes logical drives on your computer.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    <span data-ttu-id="43ab1-134">Windows Script Host (WSH) prend également en charge les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="43ab1-134">Windows Script Host (WSH) also supports the following.</span></span>

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    <span data-ttu-id="43ab1-135">Sur Active Server pages (ASP), utilisez [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) ou [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) dans le script côté serveur.</span><span class="sxs-lookup"><span data-stu-id="43ab1-135">On Active Server Pages (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) or [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) in the server-side script.</span></span> <span data-ttu-id="43ab1-136">Pour plus d’informations, consultez [création de pages de Active Server pour WMI](creating-active-server-pages-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="43ab1-136">For more information, see [Creating Active Server Pages for WMI](creating-active-server-pages-for-wmi.md).</span></span>

3.  <span data-ttu-id="43ab1-137">Une classe ou une instance peut également être spécifiée, auquel cas l’objet retourné est un objet WMI, par exemple, une instance de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), plutôt qu’un objet services.</span><span class="sxs-lookup"><span data-stu-id="43ab1-137">A class or instance can also be specified, in which case the returned object is a WMI object, for example, an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), rather than a services object.</span></span> <span data-ttu-id="43ab1-138">Notez que vous ne pouvez pas utiliser les fonctions VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) pour créer une instance de l’objet générique [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="43ab1-138">Note that you cannot use the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) functions to create an instance of the generic object [**SWbemObject**](swbemobject.md).</span></span>
4.  <span data-ttu-id="43ab1-139">Dans les pages HTML s’exécutant dans Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) et [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) peuvent échouer parce que les objets de script WMI, comme les contrôles ActiveX, ne sont pas marqués comme sécurisés pour l’écriture de scripts.</span><span class="sxs-lookup"><span data-stu-id="43ab1-139">In HTML pages running in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) and [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) can fail because WMI scripting objects, like ActiveX controls, are not marked as safe for scripting.</span></span> <span data-ttu-id="43ab1-140">La seule exception est l’objet [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="43ab1-140">The one exception is the [**SWbemDateTime**](swbemdatetime.md) object.</span></span> <span data-ttu-id="43ab1-141">La seule façon dont ces appels peuvent être exécutés est lorsque vous réduisez les paramètres de sécurité d’Internet Explorer, ce qui n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="43ab1-141">The only way that these calls can succeed is when you lower the IE security settings, which is not recommended.</span></span>

<span data-ttu-id="43ab1-142">Lorsque vous récupérez une classe en C++, appelez la version de la fonction [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="43ab1-142">When retrieving a class in C++, call the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) version of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="43ab1-143">**Pour récupérer une définition de classe en C++**</span><span class="sxs-lookup"><span data-stu-id="43ab1-143">**To retrieve a class definition in C++**</span></span>

1.  <span data-ttu-id="43ab1-144">Appelez les méthodes [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) pour récupérer la définition d’une classe.</span><span class="sxs-lookup"><span data-stu-id="43ab1-144">Call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to retrieve the definition of a class.</span></span>
2.  <span data-ttu-id="43ab1-145">Une classe peut avoir plusieurs définitions de classe, ce qui se produit généralement lorsque plusieurs fournisseurs de classes sont chargés dans un même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="43ab1-145">One class can have multiple class definitions, which happens typically when you have more than one class provider loaded into one namespace.</span></span> <span data-ttu-id="43ab1-146">Quand une classe a plusieurs définitions de classe, WMI retourne le code d’état de la première définition découverte et du code d’état des **\_ \_ \_ objets en double WBEM** .</span><span class="sxs-lookup"><span data-stu-id="43ab1-146">When a class has multiple class definitions, WMI returns the first definition discovered and the **WBEM\_S\_DUPLICATE\_OBJECTS** status code.</span></span>

<span data-ttu-id="43ab1-147">Comme [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retourne une définition de classe, elle est couramment utilisée comme première étape de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="43ab1-147">Because [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) returns a class definition, it is commonly used as the first step in creating an instance.</span></span> <span data-ttu-id="43ab1-148">Pour plus d’informations sur l’utilisation de **GetObject**, consultez [création et déclaration d’une instance à l’aide de C++](creating-and-declaring-an-instance-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="43ab1-148">For more information on how to use **GetObject**, see [Creating and Declaring an Instance Using C++](creating-and-declaring-an-instance-using-c-.md).</span></span>

 

 
