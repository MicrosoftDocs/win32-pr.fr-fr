---
description: La première étape de la connexion à WMI consiste à configurer les appels COM vers CoInitializeEx et CoInitializeSecurity.
ms.assetid: c9291aa7-702c-4752-8bd0-97d7a6e6dd54
ms.tgt_platform: multiple
title: Initialisation de COM pour une application WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6c2e590ddb64914f5aab723a56dee2385a49bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953045"
---
# <a name="initializing-com-for-a-wmi-application"></a><span data-ttu-id="06cfb-103">Initialisation de COM pour une application WMI</span><span class="sxs-lookup"><span data-stu-id="06cfb-103">Initializing COM for a WMI Application</span></span>

<span data-ttu-id="06cfb-104">La première étape de la connexion à WMI consiste à configurer les appels COM vers [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) et [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="06cfb-104">The first step in connecting to WMI is setting up the COM calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="06cfb-105">Les exemples de code de cette rubrique requièrent les références suivantes et les \# instructions include pour être compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="06cfb-105">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="06cfb-106">La procédure suivante décrit comment initialiser COM à partir d’une application cliente.</span><span class="sxs-lookup"><span data-stu-id="06cfb-106">The following procedure describes how to initialize COM from a client application.</span></span>

<span data-ttu-id="06cfb-107">**Pour initialiser COM à partir d’une application cliente**</span><span class="sxs-lookup"><span data-stu-id="06cfb-107">**To initialize COM from a client application**</span></span>

1.  <span data-ttu-id="06cfb-108">Initialisez COM avec un appel à [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="06cfb-108">Initialize COM with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="06cfb-109">L’appel de [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) est une procédure standard pour configurer une interface com.</span><span class="sxs-lookup"><span data-stu-id="06cfb-109">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) is a standard procedure for setting up a COM interface.</span></span> <span data-ttu-id="06cfb-110">Par conséquent, WMI ne nécessite pas que vous observiez des procédures supplémentaires lors de l’appel de **CoInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="06cfb-110">Therefore, WMI does not require that you observe any additional procedures when calling **CoInitializeEx**.</span></span> <span data-ttu-id="06cfb-111">Pour plus d’informations, consultez [com](../com/component-object-model--com--portal.md).</span><span class="sxs-lookup"><span data-stu-id="06cfb-111">For more information, see [COM](../com/component-object-model--com--portal.md).</span></span>

    <span data-ttu-id="06cfb-112">L’exemple de code suivant décrit comment appeler [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="06cfb-112">The following code example describes how to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```C++
    HRESULT hr;
    hr = CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hr)) 
    { cout << "Failed to initialize COM library. Error code = 0x"
           << hex << hr << endl; 
      return hr;
    }
    ```

    

2.  <span data-ttu-id="06cfb-113">Définissez les niveaux de sécurité COM généraux à l’aide d’un appel à l’interface [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="06cfb-113">Set the general COM security levels with a call to the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interface.</span></span>

    <span data-ttu-id="06cfb-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) est une fonction standard que vous devez appeler lors de la configuration d’une interface com pour un processus.</span><span class="sxs-lookup"><span data-stu-id="06cfb-114">[**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a standard function you must call when setting up a COM interface for a process.</span></span> <span data-ttu-id="06cfb-115">Appelez **CoInitializeSecurity** si vous souhaitez définir les paramètres de sécurité par défaut pour l’authentification, l’emprunt d’identité ou le service d’authentification pour un processus entier.</span><span class="sxs-lookup"><span data-stu-id="06cfb-115">Call **CoInitializeSecurity** if you want to set the default security settings for authentication, impersonation, or authentication service for an entire process.</span></span> <span data-ttu-id="06cfb-116">Pour plus d’informations, consultez Définition de la [sécurité des processus d’application cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="06cfb-116">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="06cfb-117">Si vous souhaitez définir ou modifier la sécurité pour un proxy spécifique, vous devez appeler [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="06cfb-117">If you want to set or change the security for a specific proxy, you must call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="06cfb-118">Utilisez **CoSetProxyBlanket** chaque fois que vous devez définir ou modifier la sécurité com lors de l’exécution dans un autre processus où vous ne pouvez pas contrôler les paramètres de sécurité par défaut pour l’authentification, l’emprunt d’identité ou le service d’authentification.</span><span class="sxs-lookup"><span data-stu-id="06cfb-118">Use **CoSetProxyBlanket** whenever you must set or change COM security when running inside another process where you cannot control the default security settings for authentication, impersonation, or authentication service.</span></span> <span data-ttu-id="06cfb-119">Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md) et [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="06cfb-119">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md) and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

    <span data-ttu-id="06cfb-120">WMI présente plusieurs problèmes de sécurité que vous devez connaître lors de la programmation d’une application cliente WMI.</span><span class="sxs-lookup"><span data-stu-id="06cfb-120">WMI has several security issues you should be aware of when programming a WMI client application.</span></span> <span data-ttu-id="06cfb-121">Pour plus d’informations, consultez Définition de la [sécurité des processus d’application cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="06cfb-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span>

    <span data-ttu-id="06cfb-122">L’exemple de code suivant décrit comment appeler [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir la sécurité com sur le processus.</span><span class="sxs-lookup"><span data-stu-id="06cfb-122">The following code example describes how to call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set COM security on the process.</span></span>

    ```C++
    hr =  CoInitializeSecurity(
        NULL,                        // Security descriptor    
        -1,                          // COM negotiates authentication service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication level for proxies
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation level for proxies
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities of the client or server
        NULL);                       // Reserved

    if (FAILED(hr))
    {
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       CoUninitialize();
       return hr;                  // Program has failed.
    }
    ```

    

<span data-ttu-id="06cfb-123">Après l’initialisation de COM, l’étape suivante consiste à créer une connexion à un espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="06cfb-123">After you initialize COM, your next step is to create a connection to a WMI namespace.</span></span> <span data-ttu-id="06cfb-124">Pour plus d’informations, consultez [création d’une connexion à un espace de noms WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="06cfb-124">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06cfb-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06cfb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06cfb-126">Création d’une application WMI à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="06cfb-126">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="06cfb-127">Accès aux espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="06cfb-127">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
