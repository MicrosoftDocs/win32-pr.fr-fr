---
description: Vous pouvez utiliser la procédure et les exemples de code de cette rubrique pour créer une application cliente WMI complète qui exécute l’initialisation COM, se connecte à WMI sur l’ordinateur local, récupère les données de manière asynchrone, puis nettoie.
ms.assetid: 1e11ca27-e67d-486c-8fc5-a10382edfff3
ms.tgt_platform: multiple
title: 'Exemple : obtention de données WMI à partir de l’ordinateur local de façon asynchrone'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5acf8df91b5ff279d70a9f76f0a353df90e8ff3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115862"
---
# <a name="example-getting-wmi-data-from-the-local-computer-asynchronously"></a><span data-ttu-id="42ad2-103">Exemple : obtention de données WMI à partir de l’ordinateur local de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="42ad2-103">Example: Getting WMI Data from the Local Computer Asynchronously</span></span>

<span data-ttu-id="42ad2-104">Vous pouvez utiliser la procédure et les exemples de code de cette rubrique pour créer une application cliente WMI complète qui exécute l’initialisation COM, se connecte à WMI sur l’ordinateur local, récupère les données de manière asynchrone, puis nettoie.</span><span class="sxs-lookup"><span data-stu-id="42ad2-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, gets data asynchronously, and then cleans up.</span></span> <span data-ttu-id="42ad2-105">Cet exemple obtient le nom du système d’exploitation sur l’ordinateur local et l’affiche.</span><span class="sxs-lookup"><span data-stu-id="42ad2-105">This example gets the name of the operating system on the local computer and displays it.</span></span>

<span data-ttu-id="42ad2-106">La procédure suivante est utilisée pour exécuter l’application WMI.</span><span class="sxs-lookup"><span data-stu-id="42ad2-106">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="42ad2-107">Les étapes 1 à 5 contiennent toutes les étapes nécessaires à la configuration et à la connexion à WMI, et les étapes 6 et 7 sont l’emplacement où le nom du système d’exploitation est récupéré de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="42ad2-107">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and steps 6 and seven are where the operating system name is retrieved asynchronously.</span></span>

<span data-ttu-id="42ad2-108">**Pour récupérer les données WMI de l’ordinateur local de façon asynchrone**</span><span class="sxs-lookup"><span data-stu-id="42ad2-108">**To get WMI data from the local computer asynchronously**</span></span>

1.  <span data-ttu-id="42ad2-109">Initialisez les paramètres COM avec un appel à [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="42ad2-109">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="42ad2-110">Pour plus d’informations, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="42ad2-110">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="42ad2-111">Initialisez la sécurité des processus COM en appelant [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="42ad2-111">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="42ad2-112">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="42ad2-112">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="42ad2-113">Obtenez le localisateur initial pour WMI en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="42ad2-113">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="42ad2-114">Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="42ad2-114">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="42ad2-115">Obtenez un pointeur vers [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour l' \\ espace de noms CIMV2 racine sur l’ordinateur local en appelant [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="42ad2-115">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="42ad2-116">Pour plus d’informations sur la façon de se connecter à un ordinateur distant, consultez [exemple : obtention de données WMI à partir d’un ordinateur distant](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="42ad2-116">For more information about how to connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="42ad2-117">Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="42ad2-117">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="42ad2-118">Définissez la sécurité du proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) afin que le service WMI puisse emprunter l’identité du client en appelant [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="42ad2-118">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="42ad2-119">Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="42ad2-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="42ad2-120">Utilisez le pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour effectuer des demandes à WMI.</span><span class="sxs-lookup"><span data-stu-id="42ad2-120">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests to WMI.</span></span> <span data-ttu-id="42ad2-121">Cet exemple utilise la méthode [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) pour recevoir les données de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="42ad2-121">This example uses the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method to receive the data asynchronously.</span></span> <span data-ttu-id="42ad2-122">Chaque fois que vous recevez des données de façon asynchrone, vous devez fournir une implémentation de [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="42ad2-122">Whenever you receive data asynchronously, you must provide an implementation of [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="42ad2-123">Cet exemple fournit l’implémentation dans la classe QuerySink.</span><span class="sxs-lookup"><span data-stu-id="42ad2-123">This example provides the implementation in the QuerySink class.</span></span> <span data-ttu-id="42ad2-124">Le code d’implémentation et le code du fichier d’en-tête pour cette classe sont fournis à la suite de l’exemple principal.</span><span class="sxs-lookup"><span data-stu-id="42ad2-124">The implementation code and header file code for this class are provided following the main example.</span></span> <span data-ttu-id="42ad2-125">La méthode **IWbemServices :: ExecQueryAsync** appelle la méthode QuerySink :: indique chaque fois que les données sont reçues.</span><span class="sxs-lookup"><span data-stu-id="42ad2-125">The **IWbemServices::ExecQueryAsync** method calls the QuerySink::Indicate method whenever the data is received.</span></span>

    <span data-ttu-id="42ad2-126">Pour plus d’informations sur la création d’une demande WMI, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md) et [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="42ad2-126">For more information about how to create a WMI request, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Calling a Method](calling-a-method.md).</span></span>

7.  <span data-ttu-id="42ad2-127">Attendez que les données soient récupérées de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="42ad2-127">Wait for the data to be retrieved asynchronously.</span></span> <span data-ttu-id="42ad2-128">Utilisez la méthode [**IWbemServices :: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) pour arrêter manuellement l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="42ad2-128">Use the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method to manually stop the asynchronous call.</span></span>

<span data-ttu-id="42ad2-129">L’exemple de code suivant obtient les données WMI de l’ordinateur local de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="42ad2-129">The following code example gets WMI data from the local computer asynchronously.</span></span>


```C++
#include "querysink.h"


int main(int argc, char **argv)
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

    hres =  CoInitializeSecurity(NULL, 
                                 -1,                          // COM authentication
                                 NULL,                        // Authentication services
                                 NULL,                        // Reserved
                                 RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
                                 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
                                 NULL,                        // Authentication info
                                 EOAC_NONE,                   // Additional capabilities 
                                 NULL);                       // Reserved

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
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
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(_bstr_t(L"ROOT\\CIMV2"), 
                               NULL,
                               NULL,
                               0,
                               NULL,
                               0,
                               0, 
                               &pSvc);
    
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
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(pSvc,                        // Indicates the proxy to set
                             RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
                             RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
                             NULL,                        // Server principal name 
                             RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
                             RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
                             NULL,                        // client identity
                             EOAC_NONE);                  // proxy capabilities 

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

    // For example, get the name of the operating system.
    // The IWbemService::ExecQueryAsync method will call
    // the QuerySink::Indicate method when it receives a result
    // and the QuerySink::Indicate method will display the OS name
    QuerySink* pResponseSink = new QuerySink();
    pResponseSink->AddRef();
    hres = pSvc->ExecQueryAsync(bstr_t("WQL"), 
                                bstr_t("SELECT * FROM Win32_OperatingSystem"),
                                WBEM_FLAG_BIDIRECTIONAL, 
                                NULL,
                                pResponseSink);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        pResponseSink->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Wait to get the data from the query in step 6 -----------
    Sleep(500);
    pSvc->CancelAsyncCall(pResponseSink);

    // Cleanup
    // ========
    pSvc->Release();
    pLoc->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



<span data-ttu-id="42ad2-130">Le fichier d’en-tête suivant est utilisé pour la classe QuerySink.</span><span class="sxs-lookup"><span data-stu-id="42ad2-130">The following header file is used for the QuerySink class.</span></span> <span data-ttu-id="42ad2-131">La classe QuerySink est utilisée dans l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="42ad2-131">The QuerySink class is used in the previous code example.</span></span>


```C++
// QuerySink.h
#ifndef QUERYSINK_H
#define QUERYSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;
 CRITICAL_SECTION threadLock; // for thread safety

public:
    QuerySink() { m_lRef = 0; bDone = false; 
     InitializeCriticalSection(&threadLock); }
    ~QuerySink() { bDone = true;
        DeleteCriticalSection(&threadLock); }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid,
        void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            LONG lObjectCount,
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );

 bool IsDone();
};

#endif    // end of QuerySink.h
```



<span data-ttu-id="42ad2-132">L’exemple de code suivant est une implémentation de la classe QuerySink.</span><span class="sxs-lookup"><span data-stu-id="42ad2-132">The following code example is an implementation of the QuerySink class.</span></span>


```C++
// QuerySink.cpp
#include "querysink.h"

ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        VARIANT varName;
        hres = apObjArray[i]->Get(_bstr_t(L"Name"),
            0, &varName, 0, 0);

        if (FAILED(hres))
        {
            cout << "Failed to get the data from the query"
                << " Error code = 0x"
                << hex << hres << endl;
            return WBEM_E_FAILED;       // Program has failed.
        }

        printf("Name: %ls\n", V_BSTR(&varName));
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
 if(lFlags == WBEM_STATUS_COMPLETE)
 {
  printf("Call complete.\n");

  EnterCriticalSection(&threadLock);
  bDone = true;
  LeaveCriticalSection(&threadLock);
 }
 else if(lFlags == WBEM_STATUS_PROGRESS)
 {
  printf("Call in progress.\n");
 }
    
    return WBEM_S_NO_ERROR;
}


bool QuerySink::IsDone()
{
    bool done = true;

 EnterCriticalSection(&threadLock);
 done = bDone;
 LeaveCriticalSection(&threadLock);

    return done;
}    // end of QuerySink.cpp
```



 

 
