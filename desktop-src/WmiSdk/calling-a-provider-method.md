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
# <a name="calling-a-provider-method"></a>Appel d’une méthode de fournisseur

Une méthode de fournisseur est une méthode implémentée par un fournisseur Windows Management Instrumentation (WMI). La méthode se trouve dans une classe définie par un fournisseur pour représenter des données à partir d’un logiciel ou d’un matériel. Par exemple, la classe de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) a des méthodes pour démarrer, arrêter, reprendre, suspendre et changer des services.

Les méthodes de fournisseur ne doivent pas être confondues avec les types de méthodes suivants :

-   Méthodes sur les [classes système WMI](wmi-system-classes.md), telles que [**la méthode de type de**](--systemsecurity-getsd.md) [**\_ \_ SystemSecurity**](--systemsecurity.md).
-   Méthodes sur les objets de l' [API de script pour WMI](scripting-api-for-wmi.md), comme [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).
-   Méthodes dans l' [API com pour WMI](com-api-for-wmi.md), telles que [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

## <a name="calling-a-provider-method-using-scripting"></a>Appel d’une méthode de fournisseur à l’aide de scripts

Tout langage Automation, tel que VBScript, PowerShell ou perl, peut appeler une méthode WMI. Certains langages peuvent utiliser l' [accès direct](/windows), mais d’autres doivent utiliser [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) pour exécuter indirectement la méthode du fournisseur.

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

La procédure suivante décrit comment appeler une méthode de fournisseur à l’aide de l’API de script et en utilisant l’accès direct.

**Pour appeler une méthode de fournisseur à l’aide de l’API de script et de l’accès direct**

1.  Utilisez cette approche pour VBScript ou PowerShell.
2.  Déterminez si la méthode que vous souhaitez exécuter est implémentée.

    Certaines classes ont des méthodes définies qui ne sont pas prises en charge par un fournisseur. Si une méthode n’est pas implémentée, vous ne pouvez pas l’exécuter. Vous pouvez déterminer si une méthode est implémentée en vérifiant si la méthode a le qualificateur [**implémenté**](standard-wmi-qualifiers.md) . Pour plus d’informations, consultez [qualificateurs WMI](wmi-qualifiers.md) et [accès à un qualificateur WMI](accessing-a-qualifier.md). Vous pouvez également déterminer si une méthode de classe fournisseur a le qualificateur **implémenté** défini en exécutant l’utilitaire Wbemtest.exe non pris en charge, disponible sur tout système d’exploitation sur lequel WMI est installé.

3.  Déterminez si la méthode que vous souhaitez exécuter est une méthode [*statique*](gloss-s.md) ou une méthode non statique.

    Les méthodes statiques s’appliquent uniquement aux classes WMI et non aux instances spécifiques d’une classe. Par exemple, la méthode [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la classe [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) est une méthode statique car elle l’utilise pour créer un nouveau processus sans instance de cette classe. Les méthodes non statiques s’appliquent uniquement aux instances d’une classe. Par exemple, la méthode [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) de la classe de **\_ processus Win32** est une méthode non statique parce qu’il est logique de terminer un processus uniquement si une instance de ce processus existe. Vous pouvez déterminer si une méthode est statique en vérifiant si le qualificateur [**statique**](standard-wmi-qualifiers.md) est associé à la méthode.

4.  Récupérez la classe ou l’instance qui contient la méthode que vous souhaitez exécuter.

    Pour plus d’informations, consultez [récupération de données de classe ou d’instance WMI](retrieving-class-or-instance-data.md).

5.  Configurez tous les paramètres de sécurité que la méthode peut nécessiter.

    Vous pouvez souvent déterminer les privilèges requis par une méthode en examinant les valeurs dans le qualificateur [**Privileges**](swbemsecurity-privileges.md) de la méthode. Par exemple, la méthode [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) Class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) vous oblige à définir le privilège « SeShutdownPrivilege ». Pour plus d’informations, consultez [exécution d’opérations privilégiées](executing-privileged-operations.md).

6.  Appelez la méthode et examinez la valeur de retour pour déterminer si la méthode a réussi.

L’exemple de code suivant crée un processus Notepad et obtient l’ID de processus à l’aide de l’accès direct.


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

La procédure suivante décrit comment appeler une méthode de fournisseur à l’aide de l’API de script et du [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).

**Pour appeler une méthode de fournisseur à l’aide de l’API de script et SWbemServices.ExecMethod**

1.  Récupérez la définition de classe WMI pour exécuter une méthode statique. Récupérez l’instance de classe WMI pour exécuter une méthode non statique.
2.  Récupérez la méthode à exécuter à partir de la collection [**SWbemObject. Methods \_**](swbemobject-methods-.md) de votre classe ou instance à l’aide de la méthode [**SWbemObjectSet. Item**](swbemobjectset-item.md) .
3.  Obtenez un objet [**Parameters**](swbemmethod-inparameters.md) pour la méthode et configurez les paramètres comme décrit dans [construction d’objets inparamètres](constructing-inparameters-objects.md).
4.  Appelez la méthode **SWbemServices.ExecMethod** pour exécuter et assigner la valeur de retour à un objet [**SWbemObject**](swbemobject.md) pour stocker les paramètres de sortie.
5.  Vérifiez les valeurs dans l’objet paramètres de sortie pour vérifier que la méthode s’est exécutée correctement.

L’exemple de code VBScript suivant exécute la même opération que le script précédent par l’approche indirecte par le biais de l’appel de [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).


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




La procédure suivante décrit comment appeler une méthode de fournisseur à l’aide de C++.

**Pour appeler une méthode de fournisseur à l’aide de C++**

1.  Connectez-vous à WMI.

    Pour appeler une méthode dans WMI, vous devez d’abord disposer d’une connexion active à un espace de noms WMI. Pour plus d’informations, consultez [création d’une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md) et [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).

    L’exemple suivant montre comment se connecter à WMI. Pour plus d’informations sur les problèmes de sécurité dans les appels du fournisseur WMI, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).

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

    

2.  Appelez [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) pour récupérer la définition de la classe de la méthode que vous souhaitez appeler.

    La méthode [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retourne un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) qui pointe vers la définition de classe.

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  Pour les méthodes qui requièrent des paramètres d’entrée, appelez la méthode [**IWbemClassObject :: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) pour obtenir l’objet de classe de paramètre d’entrée.

    [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) retourne un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) qui pointe vers la classe de paramètre d’entrée.

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  Générez une instance de la classe de paramètres d’entrée avec un appel à la méthode [**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  Définissez les propriétés de la classe de paramètre d’entrée à l’aide d’un appel à la méthode [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  Appelez la méthode avec un appel à [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) ou [**IWbemServices :: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).

    Pour [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI retourne tous les paramètres de sortie dans l’appel. Pour [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI retourne tous les paramètres de sortie via un appel à [**IWbemObjectSink**](iwbemobjectsink.md). Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

Le code suivant est un exemple complet d’appel d’une méthode de fournisseur.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

 
