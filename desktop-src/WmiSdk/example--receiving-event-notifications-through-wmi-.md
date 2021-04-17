---
description: Vous pouvez utiliser la procédure et l’exemple de code de cette rubrique pour terminer l’application cliente WMI qui exécute l’initialisation COM, se connecte à WMI sur l’ordinateur local, reçoit une notification d’événements, puis nettoie.
ms.assetid: 4d581965-e22a-4205-908c-661eeeec88cf
ms.tgt_platform: multiple
title: 'Exemple : réception de notifications d’événements via WMI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6380d306783f8b547d0d93df0275fd36e17e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485545"
---
# <a name="example-receiving-event-notifications-through-wmi"></a><span data-ttu-id="c8a49-103">Exemple : réception de notifications d’événements via WMI</span><span class="sxs-lookup"><span data-stu-id="c8a49-103">Example: Receiving Event Notifications Through WMI</span></span>

<span data-ttu-id="c8a49-104">Vous pouvez utiliser la procédure et l’exemple de code de cette rubrique pour terminer l’application cliente WMI qui exécute l’initialisation COM, se connecte à WMI sur l’ordinateur local, reçoit une notification d’événements, puis nettoie.</span><span class="sxs-lookup"><span data-stu-id="c8a49-104">You can use the procedure and code example in this topic to complete WMI client application that performs COM initialization, connects to WMI on the local computer, receives an event notification, and then cleans up.</span></span> <span data-ttu-id="c8a49-105">L’exemple avertit l’utilisateur d’un événement lorsqu’un nouveau processus est créé.</span><span class="sxs-lookup"><span data-stu-id="c8a49-105">The example notifies the user of an event when a new process is created.</span></span> <span data-ttu-id="c8a49-106">Les événements sont reçus de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c8a49-106">The events are received asynchronously.</span></span>

<span data-ttu-id="c8a49-107">La procédure suivante est utilisée pour exécuter l’application WMI.</span><span class="sxs-lookup"><span data-stu-id="c8a49-107">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="c8a49-108">Les étapes 1 à 5 contiennent toutes les étapes nécessaires à la configuration et à la connexion à WMI, et l’étape 6 correspond à l’emplacement de réception des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="c8a49-108">Steps 1 through 5 contain all of the steps required to set up and connect to WMI, and step 6 is where the event notifications are received.</span></span>

<span data-ttu-id="c8a49-109">**Pour recevoir une notification d’événement via WMI**</span><span class="sxs-lookup"><span data-stu-id="c8a49-109">**To receive a event notification through WMI**</span></span>

1.  <span data-ttu-id="c8a49-110">Initialisez les paramètres COM avec un appel à [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="c8a49-110">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="c8a49-111">Pour plus d’informations, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="c8a49-111">Fore more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="c8a49-112">Initialisez la sécurité des processus COM en appelant [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="c8a49-112">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="c8a49-113">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="c8a49-113">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="c8a49-114">Obtenez le localisateur initial pour WMI en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c8a49-114">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="c8a49-115">Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="c8a49-115">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="c8a49-116">Obtenez un pointeur vers [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour l' \\ espace de noms CIMV2 racine sur l’ordinateur local en appelant [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="c8a49-116">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="c8a49-117">Pour vous connecter à un ordinateur distant, consultez [exemple : obtention de données WMI à partir d’un ordinateur distant](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c8a49-117">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="c8a49-118">Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="c8a49-118">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="c8a49-119">Définissez la sécurité du proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) afin que le service WMI puisse emprunter l’identité du client en appelant [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="c8a49-119">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="c8a49-120">Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c8a49-120">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="c8a49-121">Utilisez le pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pour effectuer des demandes à WMI.</span><span class="sxs-lookup"><span data-stu-id="c8a49-121">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests to WMI.</span></span> <span data-ttu-id="c8a49-122">Cet exemple utilise la méthode [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) pour recevoir des événements asynchrones.</span><span class="sxs-lookup"><span data-stu-id="c8a49-122">This example uses the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method to receive asynchronous events.</span></span> <span data-ttu-id="c8a49-123">Lorsque vous recevez des événements asynchrones, vous devez fournir une implémentation de [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="c8a49-123">When you receive asynchronous events, you must provide an implementation of [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="c8a49-124">Cet exemple fournit l’implémentation dans la classe EventSink.</span><span class="sxs-lookup"><span data-stu-id="c8a49-124">This example provides the implementation in the EventSink class.</span></span> <span data-ttu-id="c8a49-125">Le code d’implémentation et le code du fichier d’en-tête pour cette classe sont fournis sous l’exemple principal.</span><span class="sxs-lookup"><span data-stu-id="c8a49-125">The implementation code and header file code for this class are provided below the main example.</span></span> <span data-ttu-id="c8a49-126">La méthode **IWbemServices :: ExecNotificationQueryAsync** appelle la méthode **EventSink :: indique** chaque fois qu’un événement est reçu.</span><span class="sxs-lookup"><span data-stu-id="c8a49-126">The **IWbemServices::ExecNotificationQueryAsync** method calls the **EventSink::Indicate** method whenever an event is received.</span></span> <span data-ttu-id="c8a49-127">Pour cet exemple, la méthode **EventSink :: indique** est appelée chaque fois qu’un processus est créé.</span><span class="sxs-lookup"><span data-stu-id="c8a49-127">For this example the **EventSink::Indicate** method is called whenever a process is created.</span></span> <span data-ttu-id="c8a49-128">Pour tester cet exemple, exécutez le code et démarrez un processus tel que Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="c8a49-128">To test this example, run the code and start a process such as Notepad.exe.</span></span> <span data-ttu-id="c8a49-129">Cela déclenche une notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="c8a49-129">This triggers an event notification.</span></span>

    <span data-ttu-id="c8a49-130">Pour plus d’informations sur la création de requêtes WMI, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md) et [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c8a49-130">For more information about making requests of WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c8a49-131">L’exemple de code suivant reçoit des notifications d’événements via WMI.</span><span class="sxs-lookup"><span data-stu-id="c8a49-131">The following example code receives event notifications through WMI.</span></span>


```C++
#include "eventsink.h"

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
    // Set security levels on the proxy -------------------------

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

    // Step 6: -------------------------------------------------
    // Receive event notifications -----------------------------

    // Use an unsecured apartment for security
    IUnsecuredApartment* pUnsecApp = NULL;

    hres = CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
        CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
        (void**)&pUnsecApp);
 
    EventSink* pSink = new EventSink;
    pSink->AddRef();

    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);

    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink,
        (void **) &pStubSink);

    // The ExecNotificationQueryAsync method will call
    // The EventQuery::Indicate method when an event occurs
    hres = pSvc->ExecNotificationQueryAsync(
        _bstr_t("WQL"), 
        _bstr_t("SELECT * " 
            "FROM __InstanceCreationEvent WITHIN 1 "
            "WHERE TargetInstance ISA 'Win32_Process'"), 
        WBEM_FLAG_SEND_STATUS, 
        NULL, 
        pStubSink);

    // Check for errors.
    if (FAILED(hres))
    {
        printf("ExecNotificationQueryAsync failed "
            "with = 0x%X\n", hres);
        pSvc->Release();
        pLoc->Release();
        pUnsecApp->Release();
        pStubUnk->Release();
        pSink->Release();
        pStubSink->Release();
        CoUninitialize();    
        return 1;
    }

    // Wait for the event
    Sleep(10000);
         
    hres = pSvc->CancelAsyncCall(pStubSink);

    // Cleanup
    // ========

    pSvc->Release();
    pLoc->Release();
    pUnsecApp->Release();
    pStubUnk->Release();
    pSink->Release();
    pStubSink->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



<span data-ttu-id="c8a49-132">Le fichier d’en-tête suivant est utilisé pour la classe EventSink.</span><span class="sxs-lookup"><span data-stu-id="c8a49-132">The following header file is used for the class EventSink.</span></span> <span data-ttu-id="c8a49-133">La classe EventSink est utilisée dans l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="c8a49-133">The EventSink class is used in the previous code example.</span></span>


```C++
// EventSink.h
#ifndef EVENTSINK_H
#define EVENTSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class EventSink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;

public:
    EventSink() { m_lRef = 0; }
   ~EventSink() { bDone = true; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT 
        STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppv);

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
};

#endif    // end of EventSink.h
```



<span data-ttu-id="c8a49-134">L’exemple de code suivant est une implémentation de la classe EventSink.</span><span class="sxs-lookup"><span data-stu-id="c8a49-134">The following example code is an implementation of the EventSink class.</span></span>


```C++
// EventSink.cpp
#include "eventsink.h"

ULONG EventSink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG EventSink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT EventSink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT EventSink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        printf("Event occurred\n");
    }

    return WBEM_S_NO_ERROR;
}

HRESULT EventSink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    if(lFlags == WBEM_STATUS_COMPLETE)
    {
        printf("Call complete. hResult = 0x%X\n", hResult);
    }
    else if(lFlags == WBEM_STATUS_PROGRESS)
    {
        printf("Call in progress.\n");
    }

    return WBEM_S_NO_ERROR;
}    // end of EventSink.cpp
```



 

 
