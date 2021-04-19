---
description: Après avoir récupéré un pointeur vers un proxy IWbemServices, vous devez définir la sécurité sur le proxy pour accéder à WMI par le biais du proxy.
ms.assetid: dd453e0e-aa1f-4ef1-ab21-613630b2758c
ms.tgt_platform: multiple
title: Définition des niveaux de sécurité sur une connexion WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc58b4bbbe1a01d927d8f5977c21003cdae2e315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530253"
---
# <a name="setting-the-security-levels-on-a-wmi-connection"></a><span data-ttu-id="ef2f9-103">Définition des niveaux de sécurité sur une connexion WMI</span><span class="sxs-lookup"><span data-stu-id="ef2f9-103">Setting the Security Levels on a WMI Connection</span></span>

<span data-ttu-id="ef2f9-104">Après avoir récupéré un pointeur vers un proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , vous devez définir la sécurité sur le proxy pour accéder à WMI par le biais du proxy.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-104">After you retrieve a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy, you must set the security on the proxy to access WMI through the proxy.</span></span> <span data-ttu-id="ef2f9-105">Vous devez définir la sécurité, car le proxy **IWbemServices** accorde l’accès à un objet hors processus.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-105">You must set the security because the **IWbemServices** proxy grants access to an out-of-process object.</span></span> <span data-ttu-id="ef2f9-106">En général, la sécurité COM ne permet pas à un processus d’accéder à un autre processus si vous ne définissez pas les propriétés de sécurité appropriées.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-106">In general, COM security does not allow one process to access another process if you do not set the proper security properties.</span></span> <span data-ttu-id="ef2f9-107">Pour plus d’informations, consultez [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="ef2f9-107">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span> <span data-ttu-id="ef2f9-108">Les connexions à différents systèmes d’exploitation nécessitent différents niveaux d’authentification et d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-108">Connections to different operating systems require varying levels of authentication and impersonation.</span></span> <span data-ttu-id="ef2f9-109">Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="ef2f9-109">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="ef2f9-110">Les exemples de code de cette rubrique requièrent les références suivantes et les \# instructions include pour être compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-110">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="ef2f9-111">La procédure suivante décrit comment définir les niveaux de sécurité sur une connexion WMI.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-111">The following procedure describes how to set the security levels on a WMI connection.</span></span>

<span data-ttu-id="ef2f9-112">**Pour définir les niveaux de sécurité sur une connexion WMI**</span><span class="sxs-lookup"><span data-stu-id="ef2f9-112">**To set the security levels on a WMI connection**</span></span>

-   <span data-ttu-id="ef2f9-113">Définissez les niveaux de sécurité sur le proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) à l’aide d’un appel à [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="ef2f9-113">Set the security levels on the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="ef2f9-114">L’exemple de code suivant décrit une méthode courante pour appeler [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="ef2f9-114">The following code example describes a common way of calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    ```C++
        HRESULT hres;
        IWbemServices *pSvc = 0;
        IWbemLocator *pLoc = 0;

        // Set the proxy so that impersonation of the client occurs.
        hres = CoSetProxyBlanket(pSvc,
           RPC_C_AUTHN_WINNT,
           RPC_C_AUTHZ_NONE,
           NULL,
           RPC_C_AUTHN_LEVEL_CALL,
           RPC_C_IMP_LEVEL_IMPERSONATE,
           NULL,
           EOAC_NONE
        );

        if (FAILED(hres))
        {
            cout << "Could not set proxy blanket. Error code = 0x" 
                 << hex << hres << endl;
           pSvc->Release();
          pLoc->Release();     
            CoUninitialize();
            return hres;      // Program has failed.
        }
    ```

    

<span data-ttu-id="ef2f9-115">Une fois que vous avez défini les niveaux de sécurité pour votre pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , vous pouvez accéder aux diverses fonctionnalités de WMI.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-115">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="ef2f9-116">Une fois que vous avez fini d’utiliser WMI, vous devez arrêter votre application.</span><span class="sxs-lookup"><span data-stu-id="ef2f9-116">After you finish using WMI, you must shut down your application.</span></span> <span data-ttu-id="ef2f9-117">Pour plus d’informations, consultez [nettoyage et arrêt d’une application WMI](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="ef2f9-117">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

 

 
