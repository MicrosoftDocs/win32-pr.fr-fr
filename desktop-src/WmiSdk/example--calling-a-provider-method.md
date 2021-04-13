---
description: Vous pouvez utiliser la procédure et les exemples de code de cette rubrique pour créer une application cliente WMI complète qui exécute l’initialisation COM, se connecte à WMI sur l’ordinateur local, appelle une méthode de fournisseur, puis nettoie.
ms.assetid: ee8faa14-74ec-49a2-88d6-187627c40071
ms.tgt_platform: multiple
title: 'Exemple : appel d’une méthode de fournisseur'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa20d6e3a90b7d2f7826d7f62b4092bc18d2d917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319670"
---
# <a name="example-calling-a-provider-method"></a><span data-ttu-id="122d3-103">Exemple : appel d’une méthode de fournisseur</span><span class="sxs-lookup"><span data-stu-id="122d3-103">Example: Calling a Provider Method</span></span>

<span data-ttu-id="122d3-104">Vous pouvez utiliser la procédure et les exemples de code de cette rubrique pour créer une application cliente WMI complète qui exécute l’initialisation COM, se connecte à WMI sur l’ordinateur local, appelle une méthode de fournisseur, puis nettoie.</span><span class="sxs-lookup"><span data-stu-id="122d3-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, calls a provider method, and then cleans up.</span></span> <span data-ttu-id="122d3-105">La méthode [**Win32 \_ Process :: Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) est utilisée pour démarrer Notepad.exe dans un nouveau processus.</span><span class="sxs-lookup"><span data-stu-id="122d3-105">The [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method is used to start Notepad.exe in a new process.</span></span>

<span data-ttu-id="122d3-106">La procédure suivante est utilisée pour exécuter l’application WMI.</span><span class="sxs-lookup"><span data-stu-id="122d3-106">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="122d3-107">Les étapes 1 à 5 contiennent toutes les étapes nécessaires à la configuration et à la connexion à WMI, et 6 à l’emplacement où la méthode du fournisseur est appelée.</span><span class="sxs-lookup"><span data-stu-id="122d3-107">Steps 1 through 5 contain all of the steps needed to set up and connect to WMI, and 6 is where the provider method is called.</span></span>

<span data-ttu-id="122d3-108">**Pour appeler une méthode de fournisseur**</span><span class="sxs-lookup"><span data-stu-id="122d3-108">**To call a provider method**</span></span>

1.  <span data-ttu-id="122d3-109">Initialisez les paramètres COM avec un appel à [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="122d3-109">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="122d3-110">Pour plus d’informations, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="122d3-110">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="122d3-111">Initialisez la sécurité des processus COM en appelant [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="122d3-111">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="122d3-112">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="122d3-112">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="122d3-113">Obtenez le localisateur initial pour WMI en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="122d3-113">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="122d3-114">Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="122d3-114">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="122d3-115">Obtenez un pointeur vers [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour l' \\ espace de noms CIMV2 racine sur l’ordinateur local en appelant [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="122d3-115">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="122d3-116">Pour vous connecter à un ordinateur distant, consultez [exemple : obtention de données WMI à partir d’un ordinateur distant](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="122d3-116">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="122d3-117">Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="122d3-117">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="122d3-118">Définissez la sécurité du proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) afin que le service WMI puisse emprunter l’identité du client en appelant [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="122d3-118">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="122d3-119">Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="122d3-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="122d3-120">Utilisez le pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour effectuer des demandes à WMI.</span><span class="sxs-lookup"><span data-stu-id="122d3-120">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests to WMI.</span></span> <span data-ttu-id="122d3-121">Cet exemple utilise [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) pour appeler la méthode de fournisseur [**Win32 \_ Process :: Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="122d3-121">This example uses [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to call the provider method [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span>

    <span data-ttu-id="122d3-122">Pour plus d’informations sur l’exécution de requêtes à WMI, consultez manipulation d’informations sur les [classes et les instances](manipulating-class-and-instance-information.md) et [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="122d3-122">For more information about making requests to WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="122d3-123">Si la méthode du fournisseur contient des paramètres ou des paramètres out, les valeurs des paramètres doivent être données aux pointeurs [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="122d3-123">If the provider method has any in-parameters or out-parameters, then values of the parameters must be given to [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointers.</span></span> <span data-ttu-id="122d3-124">Pour in-Parameters, vous devez générer une instance des définitions dans le paramètre, puis définir les valeurs de ces nouvelles instances.</span><span class="sxs-lookup"><span data-stu-id="122d3-124">For in-parameters, you must spawn an instance of the in-parameter definitions, and then set the values of these new instances.</span></span> <span data-ttu-id="122d3-125">La méthode [**Win32 \_ Process :: Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) requiert une valeur pour que la *ligne* de commande in-Parameter s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="122d3-125">The [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method requires a value for the *CommandLine* in-parameter to execute properly.</span></span>

    <span data-ttu-id="122d3-126">L’exemple de code suivant crée un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , génère une nouvelle instance des définitions [**Win32 \_ Process :: Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) in-Parameter, puis définit la valeur de la *ligne* de commande in-Parameter sur Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="122d3-126">The following code example creates an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer, spawns a new instance of the [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) in-parameter definitions, and then sets the value of the *CommandLine* in-parameter to Notepad.exe.</span></span>

    ```C++
    // Set up to call the Win32_Process::Create method
    BSTR MethodName = SysAllocString(L"Create");
    BSTR ClassName = SysAllocString(L"Win32_Process");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, NULL);

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in-parameters
    VARIANT varCommand;
    varCommand.vt = VT_BSTR;
    varCommand.bstrVal = _bstr_t(L"notepad.exe");

    // Store the value for the in-parameters
    hres = pClassInstance->Put(L"CommandLine", 0,
        &varCommand, 0);
    wprintf(L"The command is: %s\n", V_BSTR(&varCommand));
    ```

    

    <span data-ttu-id="122d3-127">L’exemple de code suivant montre comment les paramètres out de la méthode [**\_ Process :: Create Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) sont donnés à un pointeur [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="122d3-127">The following code example shows how the [**Win32\_Process::Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method out-parameters are given to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer.</span></span> <span data-ttu-id="122d3-128">La valeur de paramètre de sortie est obtenue avec la méthode [**IWbemClassObject :: obtenir**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) et stockée dans une variable de [**type Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) afin qu’elle puisse être affichée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="122d3-128">The out-parameter value is obtained with the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method and stored in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable so that it can be displayed to the user.</span></span>

    ```C++
    // Execute Method
    IWbemClassObject* pOutParams = NULL;
    hres = pSvc->ExecMethod(ClassName, MethodName, 0,
        NULL, pClassInstance, &pOutParams, NULL);

    VARIANT varReturnValue;
    hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
        &varReturnValue, NULL, 0);
    ```

    

<span data-ttu-id="122d3-129">L’exemple de code suivant montre comment appeler une méthode de fournisseur à l’aide de WMI.</span><span class="sxs-lookup"><span data-stu-id="122d3-129">The following code example shows how to call a provider method using WMI.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
             << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );


    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
    }

    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );

    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels for the proxy ------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // set up to call the Win32_Process::Create method
    BSTR MethodName = SysAllocString(L"Create");
    BSTR ClassName = SysAllocString(L"Win32_Process");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, NULL);

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT varCommand;
    varCommand.vt = VT_BSTR;
    varCommand.bstrVal = _bstr_t(L"notepad.exe");

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"CommandLine", 0,
        &varCommand, 0);
    wprintf(L"The command is: %s\n", V_BSTR(&varCommand));

    // Execute Method
    IWbemClassObject* pOutParams = NULL;
    hres = pSvc->ExecMethod(ClassName, MethodName, 0,
    NULL, pClassInstance, &pOutParams, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&varCommand);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pClassInstance->Release();
        pInParamsDefinition->Release();
        pOutParams->Release();
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // To see what the method returned,
    // use the following code.  The return value will
    // be in &varReturnValue
    VARIANT varReturnValue;
    hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
        &varReturnValue, NULL, 0);


    // Clean up
    //--------------------------
    VariantClear(&varCommand);
    VariantClear(&varReturnValue);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pClassInstance->Release();
    pInParamsDefinition->Release();
    pOutParams->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



 

 
