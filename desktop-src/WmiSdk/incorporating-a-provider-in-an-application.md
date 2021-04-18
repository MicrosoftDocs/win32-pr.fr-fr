---
description: Décrit comment inclure le fournisseur COM WMI en tant que composant dans une application plutôt que dans le processus WMI. Appelé fournisseur découplé, il s’agit du type recommandé de fournisseur COM WMI à créer pour les systèmes d’exploitation Windows 2000 et versions ultérieures.
ms.assetid: a502f0dd-9add-4ebd-bc25-743a55eb78ac
ms.tgt_platform: multiple
title: Incorporation d’un fournisseur dans une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb544cd3b04cc75cef026bb2e4d2e579b8dbf135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553957"
---
# <a name="incorporating-a-provider-in-an-application"></a><span data-ttu-id="b0c47-104">Incorporation d’un fournisseur dans une application</span><span class="sxs-lookup"><span data-stu-id="b0c47-104">Incorporating a Provider in an Application</span></span>

<span data-ttu-id="b0c47-105">Lors de la création d’une application qui doit être instrumentée, la meilleure pratique consiste à inclure le fournisseur en tant que composant dans l’application elle-même.</span><span class="sxs-lookup"><span data-stu-id="b0c47-105">When creating an application that is to be instrumented, the best practice is to include the provider as a component within the application itself.</span></span> <span data-ttu-id="b0c47-106">Cette pratique permet à Windows Management Instrumentation (WMI) d’interagir directement avec le fournisseur de services plutôt que par le biais de l’API du programme.</span><span class="sxs-lookup"><span data-stu-id="b0c47-106">This practice permits Windows Management Instrumentation (WMI) to interact with the service provider directly instead of indirectly through the program API.</span></span> <span data-ttu-id="b0c47-107">Le fait de découpler le fournisseur de WMI permet également à l’application de contrôler la durée de vie du fournisseur, au lieu de WMI.</span><span class="sxs-lookup"><span data-stu-id="b0c47-107">Decoupling the provider from WMI also puts the application in control of the provider lifespan, instead of WMI.</span></span> <span data-ttu-id="b0c47-108">Pour plus d’informations sur l’écriture d’un fournisseur qui s’exécute dans le processus WMI, consultez [fourniture de données à WMI en écrivant un fournisseur](supplying-data-to-wmi-by-writing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b0c47-108">For more information about writing a provider that runs in the WMI process, see [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).</span></span> <span data-ttu-id="b0c47-109">Pour plus d’informations sur le modèle d’hébergement et les paramètres de sécurité pour le fournisseur, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="b0c47-109">For more information about hosting model and security settings for the provider, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="b0c47-110">Le diagramme suivant illustre la relation entre WMI, un fournisseur découplé et une application.</span><span class="sxs-lookup"><span data-stu-id="b0c47-110">The following diagram illustrates the relationship between WMI, a decoupled provider, and an application.</span></span>

![relation entre WMI, le fournisseur découplé et l’application](images/decoupledprov.png)

<span data-ttu-id="b0c47-112">Pour plus d’informations sur les méthodes de fournisseur découplées, consultez [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) et [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span><span class="sxs-lookup"><span data-stu-id="b0c47-112">For more information about decoupled provider methods, see [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) and [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).</span></span>

> [!Note]  
> <span data-ttu-id="b0c47-113">Le fournisseur découplé prend en charge l’instance, la méthode, les fournisseurs d’événements et les consommateurs d’événements.</span><span class="sxs-lookup"><span data-stu-id="b0c47-113">The decoupled provider supports instance, method, event providers, and event consumers.</span></span> <span data-ttu-id="b0c47-114">Elle ne prend pas en charge les fournisseurs de classes et de propriétés.</span><span class="sxs-lookup"><span data-stu-id="b0c47-114">It does not support class and property providers.</span></span> <span data-ttu-id="b0c47-115">Pour plus d’informations, consultez [écriture d’un fournisseur de classes](writing-a-class-provider.md) et [écriture d’un fournisseur de propriétés](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b0c47-115">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Property Provider](writing-a-property-provider.md).</span></span>

 

<span data-ttu-id="b0c47-116">Les exemples de code de cette rubrique requièrent les références suivantes et les \# instructions include pour être compilées correctement.</span><span class="sxs-lookup"><span data-stu-id="b0c47-116">The code examples in this topic require the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="b0c47-117">La procédure suivante utilise des exemples de code C++ pour décrire comment incorporer un fournisseur découplé dans votre application.</span><span class="sxs-lookup"><span data-stu-id="b0c47-117">The following procedure uses C++ code examples to describe how to incorporate a decoupled provider in your application.</span></span> <span data-ttu-id="b0c47-118">La méthode d’initialisation de l’application effectue les étapes suivantes pour que WMI interagisse uniquement avec un fournisseur découplé inscrit.</span><span class="sxs-lookup"><span data-stu-id="b0c47-118">The initialization method of the application performs the following steps so that WMI only interacts with a registered decoupled provider.</span></span>

<span data-ttu-id="b0c47-119">**Pour implémenter un fournisseur découplé dans une application C++**</span><span class="sxs-lookup"><span data-stu-id="b0c47-119">**To implement a decoupled provider in a C++ application**</span></span>

1.  <span data-ttu-id="b0c47-120">Initialise la bibliothèque COM pour une utilisation par le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="b0c47-120">Initialize the COM library for use by the calling thread.</span></span>

    <span data-ttu-id="b0c47-121">L’exemple de code suivant montre comment initialiser la bibliothèque COM.</span><span class="sxs-lookup"><span data-stu-id="b0c47-121">The following code example shows how to initialize the COM library.</span></span>

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  <span data-ttu-id="b0c47-122">Définissez le niveau de sécurité de processus par défaut.</span><span class="sxs-lookup"><span data-stu-id="b0c47-122">Set the default process security level.</span></span>

    <span data-ttu-id="b0c47-123">Ce niveau établit le niveau de sécurité requis par d’autres processus pour accéder aux informations du processus client.</span><span class="sxs-lookup"><span data-stu-id="b0c47-123">This level establishes the security level required of other processes to access the client process' information.</span></span> <span data-ttu-id="b0c47-124">Le niveau d’authentification doit être \_ le \_ \_ niveau par défaut RPC C Authn \_ .</span><span class="sxs-lookup"><span data-stu-id="b0c47-124">The authentication level should be RPC\_C\_AUTHN\_LEVEL\_DEFAULT.</span></span> <span data-ttu-id="b0c47-125">Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="b0c47-125">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="b0c47-126">L’exemple de code suivant montre comment définir le niveau de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="b0c47-126">The following code example shows how to set the default security level.</span></span>

    ```C++
    hr = CoInitializeSecurity (NULL, 
        -1, 
        NULL, 
        NULL,
        RPC_C_AUTHN_LEVEL_DEFAULT,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, 
        EOAC_DYNAMIC_CLOAKING, 
        NULL);

    if (FAILED(hr))
    {
      CoUninitialize();
      cout << "Failed to initialize security. Error code = 0x"
           << hex << hr << endl;
      return;
    }
    ```

    

3.  <span data-ttu-id="b0c47-127">Inscrire le Bureau d’enregistrement du fournisseur découplé.</span><span class="sxs-lookup"><span data-stu-id="b0c47-127">Register the decoupled provider registrar.</span></span>

    <span data-ttu-id="b0c47-128">L’exemple de code suivant montre comment inscrire le Bureau d’enregistrement du fournisseur découplé.</span><span class="sxs-lookup"><span data-stu-id="b0c47-128">The following code example shows how to register the decoupled provider registrar.</span></span>

    ```C++
    CLSID CLSID_WbemDecoupledRegistrar;
    IID IID_IWbemDecoupledRegistrar;
    IWbemDecoupledRegistrar *myRegistrar = NULL;

    hr = CoCreateInstance(CLSID_WbemDecoupledRegistrar,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledRegistrar,
                          (void**)&myRegistrar);
    if (SUCCEEDED(hr))
    {
        IUnknown *pIUnknown = NULL;
        // CMyProv is the class added for WMI instance / event provider
        HRESULT hr = CMyProv::CreateInstance(NULL,&pIUnknown);
        if ( SUCCEEDED(hr))
        {
            hr = myRegistrar->Register(0,
                NULL,
                NULL,
                NULL,
                L"root\\cimv2",
                L"DecoupledInstanceProvider",
                pIUnknown);

                pIUnknown->Release();
        }
    }

    if (FAILED (hr))
    {
        if ( myRegistrar )
        {
            myRegistrar->Release () ;
        }
    }
    ```

    

4.  <span data-ttu-id="b0c47-129">Inscrire le fournisseur d’événements découplé.</span><span class="sxs-lookup"><span data-stu-id="b0c47-129">Register the decoupled event provider.</span></span>

    <span data-ttu-id="b0c47-130">L’exemple de code suivant montre comment inscrire le fournisseur d’événements découplé.</span><span class="sxs-lookup"><span data-stu-id="b0c47-130">The following code example shows how to register the decoupled event provider.</span></span>

    ```C++
    IWbemDecoupledBasicEventProvider *myEvtRegistrar;

    // -- Create an instance of IWbemDecoupledEventProvider
    hr = CoCreateInstance(CLSID_WbemDecoupledBasicEventProvider,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IWbemDecoupledBasicEventProvider,
                          (void**)&myEvtRegistrar);

    if (SUCCEEDED(hr))
    {
       // -- Register the DecoupledEventProvider
       hr = myEvtRegistrar->Register(0,
                                     NULL,
                                     NULL,
                                     L"root\\cimv2",
                                     L"DecoupledEventProvider",
                                     NULL, NULL);
       if (SUCCEEDED(hr))
       {
          IWbemServices *pService = NULL;
          hr = myEvtRegistrar->GetService (0, NULL, &pService);
          if (SUCCEEDED(hr))
          {
             IWbemObjectSink *pSink = NULL;
             hr = myEvtRegistrar->GetSink ( 0, NULL, &pSink );
             if (SUCCEEDED(hr))
             {
                // Provide events
             }
          }
       } 
    }
    ```

    

5.  <span data-ttu-id="b0c47-131">Effectuez les [appels à WMI](making-calls-to-wmi.md) requis par la fonctionnalité du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b0c47-131">Make the [calls to WMI](making-calls-to-wmi.md) required by the provider's functionality.</span></span> <span data-ttu-id="b0c47-132">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="b0c47-132">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="b0c47-133">Pour plus d’informations, si le fournisseur fait une demande de données à partir d’un script ou d’une application, consultez [emprunt d’identité d’un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="b0c47-133">For more information if the provider services a request for data from a script or application, see [Impersonating a Client](impersonating-a-client.md).</span></span>

<span data-ttu-id="b0c47-134">Juste avant de se terminer, l’application doit être nettoyée après elle-même.</span><span class="sxs-lookup"><span data-stu-id="b0c47-134">Just prior to terminating, the application must clean up after itself.</span></span> <span data-ttu-id="b0c47-135">La procédure suivante décrit comment annuler l’inscription du fournisseur découplé afin que WMI ne tente pas de l’interroger pour obtenir des informations.</span><span class="sxs-lookup"><span data-stu-id="b0c47-135">The following procedure describes how to unregister the decoupled provider so that WMI does not attempt to query it for information.</span></span>

<span data-ttu-id="b0c47-136">La procédure suivante décrit comment annuler l’inscription du fournisseur découplé.</span><span class="sxs-lookup"><span data-stu-id="b0c47-136">The following procedure describes how to unregister the decoupled provider.</span></span>

<span data-ttu-id="b0c47-137">**Pour annuler l’inscription du fournisseur découplé**</span><span class="sxs-lookup"><span data-stu-id="b0c47-137">**To unregister the decoupled provider**</span></span>

1.  <span data-ttu-id="b0c47-138">Annulez l’inscription et le lancement du Bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b0c47-138">Unregister and release the registrar.</span></span>

    <span data-ttu-id="b0c47-139">L’exemple de code suivant montre comment annuler l’inscription et libérer le Bureau d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b0c47-139">The following code example shows how to unregister and release the registrar.</span></span>

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  <span data-ttu-id="b0c47-140">Annulez l’inscription et le lancement du fournisseur d’événements.</span><span class="sxs-lookup"><span data-stu-id="b0c47-140">Unregister and release the event provider.</span></span>

    <span data-ttu-id="b0c47-141">L’exemple de code suivant montre comment annuler l’inscription du fournisseur d’événements et le libérer.</span><span class="sxs-lookup"><span data-stu-id="b0c47-141">The following code example shows how to unregister and release the event provider.</span></span>

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  <span data-ttu-id="b0c47-142">Nettoyez le serveur COM.</span><span class="sxs-lookup"><span data-stu-id="b0c47-142">Clean up the COM server.</span></span>

    <span data-ttu-id="b0c47-143">L’exemple de code suivant montre comment désinitialiser la bibliothèque COM.</span><span class="sxs-lookup"><span data-stu-id="b0c47-143">The following code example shows how to uninitialize the COM library.</span></span>

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a><span data-ttu-id="b0c47-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0c47-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0c47-145">Définition des descripteurs de sécurité espace</span><span class="sxs-lookup"><span data-stu-id="b0c47-145">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="b0c47-146">Sécurisation de votre fournisseur</span><span class="sxs-lookup"><span data-stu-id="b0c47-146">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="b0c47-147">Développement d’un fournisseur WMI</span><span class="sxs-lookup"><span data-stu-id="b0c47-147">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> </dl>

 

 



