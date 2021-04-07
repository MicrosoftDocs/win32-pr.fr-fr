---
description: Une fois que vous avez défini les niveaux de sécurité pour votre pointeur IWbemServices, vous pouvez accéder aux diverses fonctionnalités de WMI. Une fois que vous avez fini d’utiliser WMI, vous devez arrêter votre application.
ms.assetid: 32bc7dd8-cb05-4354-bf46-f4359ac1f0d8
ms.tgt_platform: multiple
title: Nettoyage et arrêt d’une application WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7758cbdba81e018ff3362cec86aa5096838dc9e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952471"
---
# <a name="cleaning-up-and-shutting-down-a-wmi-application"></a><span data-ttu-id="f53e9-104">Nettoyage et arrêt d’une application WMI</span><span class="sxs-lookup"><span data-stu-id="f53e9-104">Cleaning up and Shutting Down a WMI Application</span></span>

<span data-ttu-id="f53e9-105">Une fois que vous avez défini les niveaux de sécurité pour votre pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , vous pouvez accéder aux diverses fonctionnalités de WMI.</span><span class="sxs-lookup"><span data-stu-id="f53e9-105">After you set the security levels for your [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer, you can access the various capabilities of WMI.</span></span> <span data-ttu-id="f53e9-106">Une fois que vous avez fini d’utiliser WMI, vous devez arrêter votre application.</span><span class="sxs-lookup"><span data-stu-id="f53e9-106">After you finish using WMI, you must shut down your application.</span></span>

<span data-ttu-id="f53e9-107">La procédure suivante décrit comment nettoyer et arrêter une application WMI.</span><span class="sxs-lookup"><span data-stu-id="f53e9-107">The following procedure describes how to clean up and shut down a WMI application.</span></span>

<span data-ttu-id="f53e9-108">**Pour nettoyer et arrêter une application WMI**</span><span class="sxs-lookup"><span data-stu-id="f53e9-108">**To clean up and shut down a WMI application**</span></span>

1.  <span data-ttu-id="f53e9-109">Libère toutes les interfaces COM ouvertes.</span><span class="sxs-lookup"><span data-stu-id="f53e9-109">Release any open COM interfaces.</span></span>

    <span data-ttu-id="f53e9-110">Les deux interfaces principales dont vous devez vous souvenir sont [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) et [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span><span class="sxs-lookup"><span data-stu-id="f53e9-110">The two primary interfaces you must remember to release are [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).</span></span>

2.  <span data-ttu-id="f53e9-111">Appeler [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="f53e9-111">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

    <span data-ttu-id="f53e9-112">Comme avec toutes les applications COM, vous devez appeler [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) à la fin de votre application.</span><span class="sxs-lookup"><span data-stu-id="f53e9-112">As with all COM applications, you must call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) at the end of your application.</span></span>

3.  <span data-ttu-id="f53e9-113">Quittez votre application.</span><span class="sxs-lookup"><span data-stu-id="f53e9-113">Exit your application.</span></span>

    <span data-ttu-id="f53e9-114">L’exemple de code suivant montre comment quitter une application cliente WMI.</span><span class="sxs-lookup"><span data-stu-id="f53e9-114">The following code example shows how to exit a WMI client application.</span></span>

    ```C++
        // The following #include and #define statements need
        // to be used with this code:
        // #define _WIN32_DCOM
        // #include <wbemidl.h>  
        // #pragma comment(lib, "wbemuuid.lib")
        
        // pSvc was declared as IWbemServices *pSvc;
        // pLoc was declared as IWbemLocator *pLoc;

        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 0;   // Program successfully completed.
    ```

    

    > [!Note]  
    > <span data-ttu-id="f53e9-115">La `pSvc` variable est de type [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \* , et la variable PLoc est de type [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) \* .</span><span class="sxs-lookup"><span data-stu-id="f53e9-115">The `pSvc` variable is of type [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)\*, and the pLoc variable is of type [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)\*.</span></span>

     

<span data-ttu-id="f53e9-116">Vous avez correctement initialisé COM, accédé à WMI et quitté votre application.</span><span class="sxs-lookup"><span data-stu-id="f53e9-116">You have now successfully initialized COM, accessed WMI, and exited your application.</span></span> <span data-ttu-id="f53e9-117">Pour plus d’informations, consultez [exemple : création d’une application WMI](example-creating-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="f53e9-117">For more information, see [Example: Creating a WMI Application](example-creating-a-wmi-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f53e9-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f53e9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f53e9-119">Création d’une application WMI à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="f53e9-119">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
</dt> </dl>

 

 
