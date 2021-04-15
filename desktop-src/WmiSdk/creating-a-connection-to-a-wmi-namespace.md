---
description: 'Une fois que vous avez défini les appels standard à COM, vous devez ensuite vous connecter à WMI via un appel à la méthode IWbemLocator :: ConnectServer.'
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Création d’une connexion à un espace de noms WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce0e1caeef15709742704570c008012feeaf8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485744"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a><span data-ttu-id="7a2ca-103">Création d’une connexion à un espace de noms WMI</span><span class="sxs-lookup"><span data-stu-id="7a2ca-103">Creating a Connection to a WMI Namespace</span></span>

<span data-ttu-id="7a2ca-104">Une fois que vous avez défini les appels standard à COM, vous devez ensuite vous connecter à WMI via un appel à la méthode [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="7a2ca-104">After you have set the standard calls to COM, you must then connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span> <span data-ttu-id="7a2ca-105">La méthode **ConnectServer** retourne un proxy d’une interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="7a2ca-105">The **ConnectServer** method returns a proxy of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span> <span data-ttu-id="7a2ca-106">Via **IWbemServices**, vous pouvez accéder aux différentes fonctionnalités de WMI.</span><span class="sxs-lookup"><span data-stu-id="7a2ca-106">Through **IWbemServices**, you can access the different capabilities of WMI.</span></span>

<span data-ttu-id="7a2ca-107">Les exemples de code de cette rubrique requièrent les références suivantes et les \# instructions include pour être compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="7a2ca-107">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="7a2ca-108">La procédure suivante décrit comment créer une connexion à un espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="7a2ca-108">The following procedure describes how to create a connection to a WMI namespace.</span></span>

<span data-ttu-id="7a2ca-109">**Pour créer une connexion à un espace de noms WMI**</span><span class="sxs-lookup"><span data-stu-id="7a2ca-109">**To create a connection to a WMI namespace**</span></span>

-   <span data-ttu-id="7a2ca-110">Initialisez l’interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) par le biais d’un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="7a2ca-110">Initialize the [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) interface through a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="7a2ca-111">WMI ne nécessite pas l’exécution de procédures supplémentaires lors de l’appel de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) sur [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="7a2ca-111">WMI does not require that you perform any additional procedures when calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    <span data-ttu-id="7a2ca-112">L’exemple de code suivant décrit comment initialiser [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="7a2ca-112">The following code example describes how to initialize [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   <span data-ttu-id="7a2ca-113">Connectez-vous à WMI via un appel à la méthode [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="7a2ca-113">Connect to WMI through a call to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method.</span></span>

        <span data-ttu-id="7a2ca-114">La méthode [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) retourne un proxy à une interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) qui utilise pour accéder à l’espace de noms WMI local ou distant spécifié dans votre appel à **ConnectServer**.</span><span class="sxs-lookup"><span data-stu-id="7a2ca-114">The [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method returns a proxy to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface that use to access the local or remote WMI namespace specified in your call to **ConnectServer**.</span></span>

        <span data-ttu-id="7a2ca-115">L’exemple de code suivant décrit comment appeler [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="7a2ca-115">The following code example describes how to call [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

<span data-ttu-id="7a2ca-116">Une fois que vous avez reçu un pointeur vers le proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , vous devez définir la sécurité sur le proxy pour accéder à WMI.</span><span class="sxs-lookup"><span data-stu-id="7a2ca-116">After you have received a pointer to the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI.</span></span> <span data-ttu-id="7a2ca-117">Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7a2ca-117">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a2ca-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a2ca-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a2ca-119">Création d’une application WMI à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="7a2ca-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[<span data-ttu-id="7a2ca-120">Prise en charge D’ipv6 et IPv6 dans WMI</span><span class="sxs-lookup"><span data-stu-id="7a2ca-120">IPv6 and IPv4 Support in WMI</span></span>](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
