---
description: Une méthode de fournisseur est une méthode implémentée par un fournisseur Windows Management Instrumentation (WMI).
ms.assetid: 9c692bc7-246b-4619-a371-cc9e0e2d5a6e
ms.tgt_platform: multiple
title: Appel d’une méthode de fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ed8d05a1105c15f06b3df5f47006c5dafcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519430"
---
# <a name="calling-a-provider-method"></a><span data-ttu-id="2a64c-103">Appel d’une méthode de fournisseur</span><span class="sxs-lookup"><span data-stu-id="2a64c-103">Calling a Provider Method</span></span>

<span data-ttu-id="2a64c-104">Une méthode de fournisseur est une méthode implémentée par un fournisseur Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2a64c-104">A provider method is a method that is implemented by a Windows Management Instrumentation (WMI) provider.</span></span> <span data-ttu-id="2a64c-105">La méthode se trouve dans une classe définie par un fournisseur pour représenter des données à partir d’un logiciel ou d’un matériel.</span><span class="sxs-lookup"><span data-stu-id="2a64c-105">The method is found in a class defined by a provider to represent data from software or hardware.</span></span> <span data-ttu-id="2a64c-106">Par exemple, la classe de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) a des méthodes pour démarrer, arrêter, reprendre, suspendre et changer des services.</span><span class="sxs-lookup"><span data-stu-id="2a64c-106">For example, the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class has methods to start, stop, resume, pause, and change services.</span></span>

<span data-ttu-id="2a64c-107">Les méthodes de fournisseur ne doivent pas être confondues avec les types de méthodes suivants :</span><span class="sxs-lookup"><span data-stu-id="2a64c-107">Provider methods should not be confused with the following types of methods:</span></span>

-   <span data-ttu-id="2a64c-108">Méthodes sur les [classes système WMI](wmi-system-classes.md), telles que [**la méthode de type de**](--systemsecurity-getsd.md) [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-108">Methods on [WMI system classes](wmi-system-classes.md), such as the [**GetSD**](--systemsecurity-getsd.md) method on [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>
-   <span data-ttu-id="2a64c-109">Méthodes sur les objets de l' [API de script pour WMI](scripting-api-for-wmi.md), comme [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-109">Methods on objects in the [Scripting API for WMI](scripting-api-for-wmi.md), such as [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>
-   <span data-ttu-id="2a64c-110">Méthodes dans l' [API com pour WMI](com-api-for-wmi.md), telles que [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="2a64c-110">Methods in the [COM API for WMI](com-api-for-wmi.md), such as [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

## <a name="calling-a-provider-method-using-scripting"></a><span data-ttu-id="2a64c-111">Appel d’une méthode de fournisseur à l’aide de scripts</span><span class="sxs-lookup"><span data-stu-id="2a64c-111">Calling a Provider Method Using Scripting</span></span>

<span data-ttu-id="2a64c-112">Tout langage Automation, tel que VBScript, PowerShell ou perl, peut appeler une méthode WMI.</span><span class="sxs-lookup"><span data-stu-id="2a64c-112">Any automation language, such as VBScript, PowerShell, or Perl, can call a WMI method.</span></span> <span data-ttu-id="2a64c-113">Certains langages peuvent utiliser l' [accès direct](/windows), mais d’autres doivent utiliser [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) pour exécuter indirectement la méthode du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2a64c-113">Some languages can use [direct access](/windows), but others must use [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to execute the provider method indirectly.</span></span>

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

<span data-ttu-id="2a64c-114">La procédure suivante décrit comment appeler une méthode de fournisseur à l’aide de l’API de script et en utilisant l’accès direct.</span><span class="sxs-lookup"><span data-stu-id="2a64c-114">The following procedure describes how to call a provider method using the Scripting API and using direct access.</span></span>

<span data-ttu-id="2a64c-115">**Pour appeler une méthode de fournisseur à l’aide de l’API de script et de l’accès direct**</span><span class="sxs-lookup"><span data-stu-id="2a64c-115">**To call a provider method using the Scripting API and direct access**</span></span>

1.  <span data-ttu-id="2a64c-116">Utilisez cette approche pour VBScript ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2a64c-116">Use this approach for VBScript or PowerShell.</span></span>
2.  <span data-ttu-id="2a64c-117">Déterminez si la méthode que vous souhaitez exécuter est implémentée.</span><span class="sxs-lookup"><span data-stu-id="2a64c-117">Determine if the method you want to execute is implemented.</span></span>

    <span data-ttu-id="2a64c-118">Certaines classes ont des méthodes définies qui ne sont pas prises en charge par un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2a64c-118">Some classes have methods defined that are not supported by a provider.</span></span> <span data-ttu-id="2a64c-119">Si une méthode n’est pas implémentée, vous ne pouvez pas l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="2a64c-119">If a method is not implemented, you cannot execute it.</span></span> <span data-ttu-id="2a64c-120">Vous pouvez déterminer si une méthode est implémentée en vérifiant si la méthode a le qualificateur [**implémenté**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="2a64c-120">You can determine if a method is implemented by checking if the method has the [**Implemented**](standard-wmi-qualifiers.md) qualifier.</span></span> <span data-ttu-id="2a64c-121">Pour plus d’informations, consultez [qualificateurs WMI](wmi-qualifiers.md) et [accès à un qualificateur WMI](accessing-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-121">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Accessing a WMI Qualifier](accessing-a-qualifier.md).</span></span> <span data-ttu-id="2a64c-122">Vous pouvez également déterminer si une méthode de classe fournisseur a le qualificateur **implémenté** défini en exécutant l’utilitaire Wbemtest.exe non pris en charge, disponible sur tout système d’exploitation sur lequel WMI est installé.</span><span class="sxs-lookup"><span data-stu-id="2a64c-122">You can also determine if a provider class method has the **Implemented** qualifier set by running the unsupported Wbemtest.exe utility, available on any operating system with WMI installed.</span></span>

3.  <span data-ttu-id="2a64c-123">Déterminez si la méthode que vous souhaitez exécuter est une méthode [*statique*](gloss-s.md) ou une méthode non statique.</span><span class="sxs-lookup"><span data-stu-id="2a64c-123">Determine if the method you want to execute is a [*static method*](gloss-s.md) or a nonstatic method.</span></span>

    <span data-ttu-id="2a64c-124">Les méthodes statiques s’appliquent uniquement aux classes WMI et non aux instances spécifiques d’une classe.</span><span class="sxs-lookup"><span data-stu-id="2a64c-124">Static methods apply only to WMI classes and not to specific instances of a class.</span></span> <span data-ttu-id="2a64c-125">Par exemple, la méthode [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la classe [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) est une méthode statique car elle l’utilise pour créer un nouveau processus sans instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="2a64c-125">For example, the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is a static method because use it to create a new process without an instance of this class.</span></span> <span data-ttu-id="2a64c-126">Les méthodes non statiques s’appliquent uniquement aux instances d’une classe.</span><span class="sxs-lookup"><span data-stu-id="2a64c-126">Nonstatic methods apply only to instances of a class.</span></span> <span data-ttu-id="2a64c-127">Par exemple, la méthode [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) de la classe de **\_ processus Win32** est une méthode non statique parce qu’il est logique de terminer un processus uniquement si une instance de ce processus existe.</span><span class="sxs-lookup"><span data-stu-id="2a64c-127">For example, the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method of the **Win32\_Process** class is a nonstatic method because it only makes sense to terminate a process if an instance of that process exists.</span></span> <span data-ttu-id="2a64c-128">Vous pouvez déterminer si une méthode est statique en vérifiant si le qualificateur [**statique**](standard-wmi-qualifiers.md) est associé à la méthode.</span><span class="sxs-lookup"><span data-stu-id="2a64c-128">You can determine if a method is static by checking if the [**Static**](standard-wmi-qualifiers.md) qualifier is associated with the method.</span></span>

4.  <span data-ttu-id="2a64c-129">Récupérez la classe ou l’instance qui contient la méthode que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="2a64c-129">Retrieve the class or instance that contains the method you want to execute.</span></span>

    <span data-ttu-id="2a64c-130">Pour plus d’informations, consultez [récupération de données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-130">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

5.  <span data-ttu-id="2a64c-131">Configurez tous les paramètres de sécurité que la méthode peut nécessiter.</span><span class="sxs-lookup"><span data-stu-id="2a64c-131">Set up any security settings that the method may require.</span></span>

    <span data-ttu-id="2a64c-132">Vous pouvez souvent déterminer les privilèges requis par une méthode en examinant les valeurs dans le qualificateur [**Privileges**](swbemsecurity-privileges.md) de la méthode.</span><span class="sxs-lookup"><span data-stu-id="2a64c-132">You can often determine the privileges that a method requires by examining the values in the [**Privileges**](swbemsecurity-privileges.md) qualifier of the method.</span></span> <span data-ttu-id="2a64c-133">Par exemple, la méthode [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) Class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) vous oblige à définir le privilège « SeShutdownPrivilege ».</span><span class="sxs-lookup"><span data-stu-id="2a64c-133">For example, the [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) method requires you to set the "SeShutdownPrivilege" privilege.</span></span> <span data-ttu-id="2a64c-134">Pour plus d’informations, consultez [exécution d’opérations privilégiées](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-134">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

6.  <span data-ttu-id="2a64c-135">Appelez la méthode et examinez la valeur de retour pour déterminer si la méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="2a64c-135">Call the method and examine the return value to determine if the method was successful.</span></span>

<span data-ttu-id="2a64c-136">L’exemple de code suivant crée un processus Notepad et obtient l’ID de processus à l’aide de l’accès direct.</span><span class="sxs-lookup"><span data-stu-id="2a64c-136">The following code example creates a Notepad process and gets the process ID using direct access.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_Process")

Error = objWMIService.Create("notepad.exe", null, _
    null, intProcessID)
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & intProcessID & "."
Else
    Wscript.Echo "Notepad could not be started due to error " _
       & Error & "."
End If  
```


```PowerShell

try
{ 
    $myProcess = ([wmiclass]&quot;win32_process&quot;).create(&quot;notepad.exe&quot;, $null, $null) 
}
catch 
{
    &quot;Notepad could not be started due to the following error:&quot; 
    $error[0]
    return 
}
#else
&quot;Notepad was started with a process ID of &quot; + $myProcess.ProcessID
```





<span id="indirect_access"></span><span id="INDIRECT_ACCESS"></span>

<span data-ttu-id="2a64c-137">La procédure suivante décrit comment appeler une méthode de fournisseur à l’aide de l’API de script et du [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-137">The following procedure describes how to call a provider method using the Scripting API and the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>

<span data-ttu-id="2a64c-138">**Pour appeler une méthode de fournisseur à l’aide de l’API de script et SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="2a64c-138">**To call a provider method using the Scripting API and SWbemServices.ExecMethod**</span></span>

1.  <span data-ttu-id="2a64c-139">Récupérez la définition de classe WMI pour exécuter une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="2a64c-139">Retrieve the WMI class definition to execute a static method.</span></span> <span data-ttu-id="2a64c-140">Récupérez l’instance de classe WMI pour exécuter une méthode non statique.</span><span class="sxs-lookup"><span data-stu-id="2a64c-140">Retrieve the WMI class instance to execute a nonstatic method.</span></span>
2.  <span data-ttu-id="2a64c-141">Récupérez la méthode à exécuter à partir de la collection [**SWbemObject. Methods \_**](swbemobject-methods-.md) de votre classe ou instance à l’aide de la méthode [**SWbemObjectSet. Item**](swbemobjectset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="2a64c-141">Retrieve the method to execute from the [**SWbemObject.Methods\_**](swbemobject-methods-.md) collection of your class or instance by using the [**SWbemObjectSet.Item**](swbemobjectset-item.md) method.</span></span>
3.  <span data-ttu-id="2a64c-142">Obtenez un objet [**Parameters**](swbemmethod-inparameters.md) pour la méthode et configurez les paramètres comme décrit dans [construction d’objets inparamètres](constructing-inparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-142">Obtain an [**InParameters**](swbemmethod-inparameters.md) object for the method and set up the parameters as described in [Constructing InParameters Objects](constructing-inparameters-objects.md).</span></span>
4.  <span data-ttu-id="2a64c-143">Appelez la méthode **SWbemServices.ExecMethod** pour exécuter et assigner la valeur de retour à un objet [**SWbemObject**](swbemobject.md) pour stocker les paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="2a64c-143">Call the **SWbemServices.ExecMethod** method to execute and assign the return value to an [**SWbemObject**](swbemobject.md) object to store the output parameters.</span></span>
5.  <span data-ttu-id="2a64c-144">Vérifiez les valeurs dans l’objet paramètres de sortie pour vérifier que la méthode s’est exécutée correctement.</span><span class="sxs-lookup"><span data-stu-id="2a64c-144">Check the values in the output parameters object to verify that the method executed correctly.</span></span>

<span data-ttu-id="2a64c-145">L’exemple de code VBScript suivant exécute la même opération que le script précédent par l’approche indirecte par le biais de l’appel de [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-145">The following VBScript code example performs the same operation as the previous script by the indirect approach through calling [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")

Set objProcess = objWMIService.Get("Win32_Process")

' Obtain an InParameters object specific to 
'   the Win32_Process.Create method.
Set objInParam = _
    objProcess.Methods_("Create").inParameters.SpawnInstance_()

' Add the input parameters. 
objInParam.Properties_.item("CommandLine") = "Notepad"
objInParam.Properties_.item("CurrentDirectory") = NULL
objInParam.Properties_.item("ProcessStartupInformation") = NULL


Set objOutParams = objProcess.ExecMethod_("Create", objInParam) 
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & objOutParams.ProcessId 
Else
    Wscript.Echo "Notepad could not be started due to error " & _
       objOutParams.ReturnValue
End If
```




<span data-ttu-id="2a64c-146">La procédure suivante décrit comment appeler une méthode de fournisseur à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="2a64c-146">The following procedure describes how to call a provider method using C++.</span></span>

<span data-ttu-id="2a64c-147">**Pour appeler une méthode de fournisseur à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="2a64c-147">**To call a provider method using C++**</span></span>

1.  <span data-ttu-id="2a64c-148">Connectez-vous à WMI.</span><span class="sxs-lookup"><span data-stu-id="2a64c-148">Connect to WMI.</span></span>

    <span data-ttu-id="2a64c-149">Pour appeler une méthode dans WMI, vous devez d’abord disposer d’une connexion active à un espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="2a64c-149">To call a method in WMI, first you must have a working connection to a WMI namespace.</span></span> <span data-ttu-id="2a64c-150">Pour plus d’informations, consultez [création d’une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md) et [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-150">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md) and [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="2a64c-151">L’exemple suivant montre comment se connecter à WMI.</span><span class="sxs-lookup"><span data-stu-id="2a64c-151">The following example shows how to connect to WMI.</span></span> <span data-ttu-id="2a64c-152">Pour plus d’informations sur les problèmes de sécurité dans les appels du fournisseur WMI, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-152">For more information about security issues in WMI provider calls, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

```C++
    HRESULT hr = CoInitialize(0);
        hr  =  CoInitializeSecurity(
                NULL, 
                -1, 
                NULL, 
                NULL,
                RPC_C_AUTHN_LEVEL_DEFAULT, 
                RPC_C_IMP_LEVEL_IMPERSONATE, 
                NULL, 
                EOAC_NONE, 
                NULL); 
        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
                CLSCTX_INPROC_SERVER,
                IID_IWbemLocator, (LPVOID *) &pLocator);
        hr = pLocator->ConnectServer(path, NULL, NULL, 
                NULL, 0, NULL, NULL, &pNamespace);
```

    

2.  <span data-ttu-id="2a64c-153">Appelez [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) pour récupérer la définition de la classe de la méthode que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="2a64c-153">Call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve the definition of the class of the method you want to call.</span></span>

    <span data-ttu-id="2a64c-154">La méthode [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retourne un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) qui pointe vers la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="2a64c-154">The [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the class definition.</span></span>

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  <span data-ttu-id="2a64c-155">Pour les méthodes qui requièrent des paramètres d’entrée, appelez la méthode [**IWbemClassObject :: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) pour obtenir l’objet de classe de paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2a64c-155">For methods that require input parameters, call the [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method to get the input parameter class object.</span></span>

    <span data-ttu-id="2a64c-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) retourne un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) qui pointe vers la classe de paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2a64c-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the input parameter class.</span></span>

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  <span data-ttu-id="2a64c-157">Générez une instance de la classe de paramètres d’entrée avec un appel à la méthode [**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="2a64c-157">Generate an instance of the input parameter class with a call to the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  <span data-ttu-id="2a64c-158">Définissez les propriétés de la classe de paramètre d’entrée à l’aide d’un appel à la méthode [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="2a64c-158">Set the properties of the input parameter class with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  <span data-ttu-id="2a64c-159">Appelez la méthode avec un appel à [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="2a64c-159">Invoke the method with a call to [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span>

    <span data-ttu-id="2a64c-160">Pour [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI retourne tous les paramètres de sortie dans l’appel.</span><span class="sxs-lookup"><span data-stu-id="2a64c-160">For [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI returns any output parameters in the call.</span></span> <span data-ttu-id="2a64c-161">Pour [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI retourne tous les paramètres de sortie via un appel à [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-161">For [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI returns any output parameters through a call to [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="2a64c-162">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2a64c-162">For more information, see [Calling a Method](calling-a-method.md).</span></span>

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

<span data-ttu-id="2a64c-163">Le code suivant est un exemple complet d’appel d’une méthode de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2a64c-163">The following code is a complete example for calling a provider method.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    IWbemLocator *pLocator = NULL;
    IWbemServices *pNamespace = 0;
    IWbemClassObject * pClass = NULL;
    IWbemClassObject * pOutInst = NULL;
    IWbemClassObject * pInClass = NULL;
    IWbemClassObject * pInInst = NULL;
  
    BSTR path = SysAllocString(L"root\\default");
    BSTR ClassPath = SysAllocString(L"TestMeth");
    BSTR MethodName = SysAllocString(L"Echo");
    BSTR ArgName = SysAllocString(L"sInArg");
    BSTR Text;

    // Initialize COM and connect to WMI.

    HRESULT hr = CoInitialize(0);
    hr  =  CoInitializeSecurity(NULL, -1, NULL, NULL,RPC_C_AUTHN_LEVEL_DEFAULT, 
                                RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE, NULL); 
    hr = CoCreateInstance(CLSID_WbemLocator, 0, CLSCTX_INPROC_SERVER,
                          IID_IWbemLocator, (LPVOID *) &pLocator);
    hr = pLocator->ConnectServer(path, NULL, NULL, NULL, 0, NULL, NULL, &pNamespace);

    // Get the class object for the method definition.

    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);

    // Get the input-argument class object and 
    // create an instance.

    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL); 
    hr = pInClass->SpawnInstance(0, &pInInst);

    // Set the property.

    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);

    // Call the method.

    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
    
    // Display the results. Note that the return 
    // value is in the property "ReturnValue"
    // and the returned string is in the 
    // property "sOutArg".

    hr = pOutInst->GetObjectText(0, &Text);
    printf("\nThe object text is:\n%S", Text);

    // Free up resources.

    SysFreeString(path);
    SysFreeString(ClassPath);
    SysFreeString(MethodName);
    SysFreeString(ArgName);
    SysFreeString(Text);
    pClass->Release();
    pInInst->Release();
    pInClass->Release();
    pOutInst->Release();
    pLocator->Release();
    pNamespace->Release();
    CoUninitialize();
    printf("Terminating normally\n");
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="2a64c-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a64c-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a64c-165">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="2a64c-165">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
