---
description: Un qualificateur est une balise qui fournit plus d’informations sur un objet, une méthode ou une propriété WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Accès à un qualificateur WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521375"
---
# <a name="accessing-a-wmi-qualifier"></a><span data-ttu-id="a3017-103">Accès à un qualificateur WMI</span><span class="sxs-lookup"><span data-stu-id="a3017-103">Accessing a WMI Qualifier</span></span>

<span data-ttu-id="a3017-104">Un qualificateur est une balise qui fournit plus d’informations sur un objet, une méthode ou une propriété WMI.</span><span class="sxs-lookup"><span data-stu-id="a3017-104">A qualifier is a tag that provides more information about a WMI object, method, or property.</span></span> <span data-ttu-id="a3017-105">Dans certains cas, vous devrez peut-être accéder aux données stockées dans un qualificateur.</span><span class="sxs-lookup"><span data-stu-id="a3017-105">At times, you may need to access the data stored in a qualifier.</span></span> <span data-ttu-id="a3017-106">Par exemple, une tâche courante consiste à déterminer si un fournisseur implémente une méthode en tentant de récupérer le qualificateur **implémenté** pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a3017-106">For example, a common task is to determine if a provider implements a method by attempting to retrieve the **Implemented** qualifier for that method.</span></span> <span data-ttu-id="a3017-107">Pour plus d’informations, consultez [qualificateurs WMI](wmi-qualifiers.md) et [Ajout d’un qualificateur](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="a3017-107">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

<span data-ttu-id="a3017-108">Vous pouvez récupérer les qualificateurs d’un objet WMI dans PowerShell en extrayant d’abord l’objet, puis en examinant les qualificateurs comme vous le feriez pour toute autre propriété.</span><span class="sxs-lookup"><span data-stu-id="a3017-108">You can retrieve the qualifiers on a WMI object in PowerShell by first retrieving the object, and then examining the qualifiers as you would any other property.</span></span>

<span data-ttu-id="a3017-109">**Pour récupérer un qualificateur à l’aide de PowerShell**</span><span class="sxs-lookup"><span data-stu-id="a3017-109">**To retrieve a qualifier using PowerShell**</span></span>

-   <span data-ttu-id="a3017-110">Récupérez l’objet dont vous souhaitez afficher les qualificateurs à l’aide de la propriété [obtenir-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), puis accédez aux qualificateurs via la propriété **qualificateurs** :</span><span class="sxs-lookup"><span data-stu-id="a3017-110">Retrieve the object whose qualifiers you want to view using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), and then access the qualifiers through the **Qualifiers** property:</span></span>

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    <span data-ttu-id="a3017-111">Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="a3017-111">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="a3017-112">Vous pouvez récupérer les qualificateurs sur une instance WMI en C# en extrayant d’abord l’objet, puis en examinant les qualificateurs en tant que collection.</span><span class="sxs-lookup"><span data-stu-id="a3017-112">You can retrieve the qualifiers on a WMI instance in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

<span data-ttu-id="a3017-113">**Pour récupérer un qualificateur à l’aide de C# (Microsoft.SysTEM. Gestion**</span><span class="sxs-lookup"><span data-stu-id="a3017-113">**To retrieve a qualifier using C# (Microsoft.System.Management)**</span></span>

1.  <span data-ttu-id="a3017-114">Récupérez la classe dont vous souhaitez afficher les qualificateurs en créant un objet CimInstance à l’aide du nom de classe et de l’espace de noms spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a3017-114">Retrieve the class whose qualifiers you want to view by creating a CimInstance object, using the specified class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    <span data-ttu-id="a3017-115">Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="a3017-115">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="a3017-116">Vous pouvez récupérer les qualificateurs de classe à partir de [CimInstance. CimClass. CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), les qualificateurs de propriété de [CimInstance. CimClass. CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))et les qualificateurs de méthode de [CimInstance. CimClass. CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3017-116">You can retrieve the class qualifiers from the [CimInstance.CimClass.CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), the property qualifiers from [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85)), and the method qualifiers from [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span></span>

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    <span data-ttu-id="a3017-117">Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="a3017-117">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="a3017-118">Vous pouvez récupérer les qualificateurs sur un objet WMI en C# en extrayant d’abord l’objet, puis en examinant les qualificateurs en tant que collection.</span><span class="sxs-lookup"><span data-stu-id="a3017-118">You can retrieve the qualifiers on a WMI object in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

> [!Note]  
> <span data-ttu-id="a3017-119">**System. Management** était l’espace de noms .net d’origine utilisé pour accéder à WMI. Toutefois, les API de cet espace de noms sont généralement plus lentes et ne sont pas mises à l’échelle par rapport à leurs homologues **Microsoft. Management. infrastructure** plus modernes.</span><span class="sxs-lookup"><span data-stu-id="a3017-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="a3017-120">**Pour récupérer un qualificateur à l’aide de C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="a3017-120">**To retrieve a qualifier using C# (System.Management)**</span></span>

1.  <span data-ttu-id="a3017-121">Récupérez l’objet dont vous souhaitez afficher les qualificateurs à l’aide de [ManagementObject](/dotnet/api/system.management.managementobject).</span><span class="sxs-lookup"><span data-stu-id="a3017-121">Retrieve the object whose qualifiers you want to view using [ManagementObject](/dotnet/api/system.management.managementobject).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    <span data-ttu-id="a3017-122">Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="a3017-122">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="a3017-123">Placez les qualificateurs dans un [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)et Énumérez les valeurs [QualifierData](/dotnet/api/system.management.qualifierdata) .</span><span class="sxs-lookup"><span data-stu-id="a3017-123">Place the qualifiers into a [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection), and enumerate through the [QualifierData](/dotnet/api/system.management.qualifierdata) values.</span></span>

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    <span data-ttu-id="a3017-124">Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="a3017-124">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="a3017-125">La procédure suivante décrit comment récupérer un qualificateur à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="a3017-125">The following procedure describes how to retrieve a qualifier using VBScript.</span></span>

<span data-ttu-id="a3017-126">**Pour récupérer un qualificateur à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="a3017-126">**To retrieve a qualifier using VBScript**</span></span>

1.  <span data-ttu-id="a3017-127">Récupérez l’objet dont vous souhaitez afficher les qualificateurs, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="a3017-127">Retrieve the object whose qualifiers you want to view, as shown in the following example:</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    <span data-ttu-id="a3017-128">La méthode la plus courante pour récupérer un objet consiste à utiliser la méthode [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="a3017-128">The most common way to retrieve an object is by using the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method.</span></span> <span data-ttu-id="a3017-129">Pour plus d’informations, consultez [récupération d’une instance WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="a3017-129">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="a3017-130">Accédez aux qualificateurs de l’objet via la propriété [**SWbemObject. Qualifiers \_**](swbemobject-qualifiers-.md) , comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="a3017-130">Access the qualifiers of the object through the [**SWbemObject.Qualifiers\_**](swbemobject-qualifiers-.md) property, as shown in the following example:</span></span>

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

<span data-ttu-id="a3017-131">L’exemple de code suivant décrit comment accéder à tous les qualificateurs d’un objet [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="a3017-131">The following code example describes how to access all the qualifiers on a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object.</span></span>


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="a3017-132">La procédure suivante décrit comment récupérer un qualificateur à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="a3017-132">The following procedure describes how to retrieve a qualifier using C++.</span></span>

<span data-ttu-id="a3017-133">**Pour récupérer un qualificateur à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="a3017-133">**To retrieve a qualifier using C++**</span></span>

1.  <span data-ttu-id="a3017-134">Récupérez l’objet dont vous souhaitez afficher les qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="a3017-134">Retrieve the object whose qualifiers you want to view.</span></span>

    <span data-ttu-id="a3017-135">La méthode la plus courante pour récupérer un objet consiste à utiliser un appel à [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou à [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="a3017-135">The most common way to retrieve an object is by using a call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="a3017-136">Pour plus d’informations, consultez [récupération de données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="a3017-136">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="a3017-137">Récupérez le jeu de qualificateurs pour une propriété donnée avec un appel à [**IWbemClassObject :: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) ou [**IWbemClassObject :: GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) méthodes.</span><span class="sxs-lookup"><span data-stu-id="a3017-137">Retrieve the qualifier set for a given property with a call to [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) or [**IWbemClassObject::GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) methods.</span></span>

3.  <span data-ttu-id="a3017-138">Accédez aux qualificateurs de l’objet par le biais de l’interface [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) retournée.</span><span class="sxs-lookup"><span data-stu-id="a3017-138">Access the qualifiers of the object through the returned [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="a3017-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="a3017-139">Examples</span></span>

<span data-ttu-id="a3017-140">Pour plus d’informations sur la récupération des qualificateurs, consultez l’exemple de code PowerShell [WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) dans la Galerie technet.</span><span class="sxs-lookup"><span data-stu-id="a3017-140">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

 

 
