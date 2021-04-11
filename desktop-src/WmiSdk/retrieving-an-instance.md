---
description: La récupération d’une instance est l’une des procédures de récupération les plus courantes que vous êtes susceptible d’effectuer dans WMI.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Récupération d’une instance WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042762"
---
# <a name="retrieving-a-wmi-instance"></a><span data-ttu-id="977df-103">Récupération d’une instance WMI</span><span class="sxs-lookup"><span data-stu-id="977df-103">Retrieving a WMI Instance</span></span>

<span data-ttu-id="977df-104">La récupération d’une instance est l’une des procédures de récupération les plus courantes que vous êtes susceptible d’effectuer dans WMI.</span><span class="sxs-lookup"><span data-stu-id="977df-104">Retrieving an instance is one of the most common retrieval procedures you are likely to perform in WMI.</span></span> <span data-ttu-id="977df-105">Vous pouvez récupérer une instance existante ou créer une nouvelle instance sans nom.</span><span class="sxs-lookup"><span data-stu-id="977df-105">You can retrieve an existing instance or create a new unnamed instance.</span></span> <span data-ttu-id="977df-106">Le chemin d’accès WMI de l’instance existante est un paramètre obligatoire.</span><span class="sxs-lookup"><span data-stu-id="977df-106">The WMI path to the existing instance is a required parameter.</span></span> <span data-ttu-id="977df-107">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="977df-107">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

> [!Note]  
> <span data-ttu-id="977df-108">Lorsque vous fournissez une instance, un fournisseur peut ne pas être en mesure de fournir une valeur pour certaines propriétés.</span><span class="sxs-lookup"><span data-stu-id="977df-108">When providing an instance, a provider may be unable to provide a value for certain properties.</span></span> <span data-ttu-id="977df-109">Sauf indication contraire dans la description de la propriété, vous ne pouvez pas déduire une signification à partir d’une valeur vide.</span><span class="sxs-lookup"><span data-stu-id="977df-109">Unless otherwise stated in the property description, you cannot infer any meaning from an empty value.</span></span> <span data-ttu-id="977df-110">Cela ne doit pas être confondu avec une chaîne qui a une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="977df-110">This is not to be confused with a string which has a **NULL** value.</span></span> <span data-ttu-id="977df-111">Dans ce cas, la valeur est remplie.</span><span class="sxs-lookup"><span data-stu-id="977df-111">In this case, the value is populated.</span></span> <span data-ttu-id="977df-112">Il est vide, mais a une valeur : **null**.</span><span class="sxs-lookup"><span data-stu-id="977df-112">It is empty but has a value: **NULL**.</span></span>

 

<span data-ttu-id="977df-113">Récupérez une copie locale de l’instance avec un appel à l’applet de commande PowerShell [-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) .</span><span class="sxs-lookup"><span data-stu-id="977df-113">Retrieve a local copy of the instance with a call to the PowerShell [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

<span data-ttu-id="977df-114">**Pour récupérer une instance d’une classe WMI à l’aide de PowerShell**</span><span class="sxs-lookup"><span data-stu-id="977df-114">**To retrieve an instance of a WMI class using PowerShell**</span></span>

-   <span data-ttu-id="977df-115">Vous pouvez récupérer des instances spécifiques à l’aide des paramètres *-Class* et *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="977df-115">You can retrieve specific instances using the *-class* and *-filter* parameters.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="977df-116">Vous pouvez récupérer une instance WMI en utilisant C# en créant un objet de recherche à l’aide de [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), puis en le remplissant avec les valeurs de clé pertinentes, puis en recherchant cet objet avec un appel de [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="977df-116">You can retrieve a WMI instance using C# by creating a search object using [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), and then filling it with the relevant key values, and then searching for that object with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

<span data-ttu-id="977df-117">**Pour récupérer une instance d’une classe WMI à l’aide de C# (Microsoft. Management. infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="977df-117">**To retrieve an instance of a WMI class using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="977df-118">À l’aide de l’espace de noms [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , créez un nouvel objet [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) avec le nom de classe et l’espace de noms appropriés.</span><span class="sxs-lookup"><span data-stu-id="977df-118">Using the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, create a new [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) object with the relevant class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="977df-119">Créez un [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) qui contient le nom et la valeur de la propriété de clé de l’instance que vous souhaitez rechercher, puis ajoutez cette propriété à votre objet de classe.</span><span class="sxs-lookup"><span data-stu-id="977df-119">Create a [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) that contains the name and value of the key property of the instance you wish to search for, and add that property to your class object.</span></span>

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  <span data-ttu-id="977df-120">Récupérez l’objet de WMI avec un appel [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="977df-120">Retrieve the object from WMI with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

<span data-ttu-id="977df-121">Vous pouvez récupérer une instance de classe WMI spécifique ou une collection d’instances de classe WMI à l’aide des classes de l’espace de noms [System. Management](/dotnet/api/system.management) .</span><span class="sxs-lookup"><span data-stu-id="977df-121">You can retrieve either a specific WMI class instance, or a collection of WMI class instances, using classes in the [System.Management](/dotnet/api/system.management) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="977df-122">**System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.</span><span class="sxs-lookup"><span data-stu-id="977df-122">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="977df-123">**Pour récupérer une instance d’une classe WMI à l’aide de C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="977df-123">**To retrieve an instance of a WMI class using C# (System.Management)**</span></span>

1.  <span data-ttu-id="977df-124">Récupérez une copie locale d’une instance spécifique en créant un nouveau [ManagementObject](/dotnet/api/system.management.managementobject), avec le nom et la valeur d’instance spécifique transmis par le biais du paramètre *ManagementPath* .</span><span class="sxs-lookup"><span data-stu-id="977df-124">Retrieve a local copy of a specific instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject), with the name and specific instance value passed in though the *ManagementPath* parameter.</span></span> <span data-ttu-id="977df-125">Vous pouvez ensuite récupérer les données d’instance en appelant explicitement [ManagementObject. obtenir](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="977df-125">You can then retrieve the instance data by explicitly calling [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  <span data-ttu-id="977df-126">Vous pouvez également récupérer toutes les instances d’une classe WMI en les recherchant avec un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher), puis en énumérant les [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)retournés.</span><span class="sxs-lookup"><span data-stu-id="977df-126">Alternately, you can retrieve all instances of a WMI class by searching for them with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher), and then enumerating through the returned [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    <span data-ttu-id="977df-127">Vous pouvez appeler la méthode d' **extraction** de manière implicite en accédant à l’instance.</span><span class="sxs-lookup"><span data-stu-id="977df-127">You can implicitly call the **Get** method by accessing the instance.</span></span> <span data-ttu-id="977df-128">Pour plus d’informations, consultez [récupération d’une partie d’une instance WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="977df-128">For more information, see [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

<span data-ttu-id="977df-129">Récupérez une copie locale de l’instance avec un appel à la méthode VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) .</span><span class="sxs-lookup"><span data-stu-id="977df-129">Retrieve a local copy of the instance with a call to the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) method.</span></span>

<span data-ttu-id="977df-130">**Pour récupérer une instance d’une classe WMI à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="977df-130">**To retrieve an instance of a WMI class using VBScript**</span></span>

-   <span data-ttu-id="977df-131">Appelez [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) avec le chemin d’accès de l’objet de l’instance, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="977df-131">Call [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) with the object path of the instance as shown in the following example.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    <span data-ttu-id="977df-132">Pour récupérer une instance spécifique, vous devez donner un nom dans le chemin d’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="977df-132">Retrieving a specific instance requires giving a name as part of the object path.</span></span>

<span data-ttu-id="977df-133">En C++, appelez [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="977df-133">In C++, call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="977df-134">**Pour récupérer une instance d’une classe WMI à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="977df-134">**To retrieve an instance of a WMI class using C++**</span></span>

-   <span data-ttu-id="977df-135">Récupérez une copie locale de l’instance avec un appel à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="977df-135">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="977df-136">Le chemin d’accès WMI de l’objet doit être inclus.</span><span class="sxs-lookup"><span data-stu-id="977df-136">The WMI path to the object must be included.</span></span>

    <span data-ttu-id="977df-137">Comme son nom l’indique, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) récupère l’instance de façon asynchrone, tandis que [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) récupère l’instance de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="977df-137">As the name implies, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) retrieves the instance asynchronously, while [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retrieves the instance synchronously.</span></span> <span data-ttu-id="977df-138">Si vous souhaitez utiliser la récupération asynchrone, vous devez implémenter l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="977df-138">If you want to use asynchronous retrieval, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="977df-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="977df-139">Examples</span></span>

<span data-ttu-id="977df-140">Pour obtenir un exemple VBScript à utiliser comme modèle pour récupérer des informations de classe et d’instance, consultez l’exemple de [script de modèle WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) sur la Galerie technet.</span><span class="sxs-lookup"><span data-stu-id="977df-140">For a VBScript example to use as a template to retrieve class and instance information, see the [WMI Template Script](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) example on TechNet Gallery.</span></span> <span data-ttu-id="977df-141">Cet exemple particulier utilise GetObject pour récupérer le service WMI.</span><span class="sxs-lookup"><span data-stu-id="977df-141">This particular example uses GetObject to retrieve the WMI Service.</span></span>

 

 
