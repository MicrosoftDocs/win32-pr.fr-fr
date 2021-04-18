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
# <a name="incorporating-a-provider-in-an-application"></a>Incorporation d’un fournisseur dans une application

Lors de la création d’une application qui doit être instrumentée, la meilleure pratique consiste à inclure le fournisseur en tant que composant dans l’application elle-même. Cette pratique permet à Windows Management Instrumentation (WMI) d’interagir directement avec le fournisseur de services plutôt que par le biais de l’API du programme. Le fait de découpler le fournisseur de WMI permet également à l’application de contrôler la durée de vie du fournisseur, au lieu de WMI. Pour plus d’informations sur l’écriture d’un fournisseur qui s’exécute dans le processus WMI, consultez [fourniture de données à WMI en écrivant un fournisseur](supplying-data-to-wmi-by-writing-a-provider.md). Pour plus d’informations sur le modèle d’hébergement et les paramètres de sécurité pour le fournisseur, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

Le diagramme suivant illustre la relation entre WMI, un fournisseur découplé et une application.

![relation entre WMI, le fournisseur découplé et l’application](images/decoupledprov.png)

Pour plus d’informations sur les méthodes de fournisseur découplées, consultez [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar) et [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider).

> [!Note]  
> Le fournisseur découplé prend en charge l’instance, la méthode, les fournisseurs d’événements et les consommateurs d’événements. Elle ne prend pas en charge les fournisseurs de classes et de propriétés. Pour plus d’informations, consultez [écriture d’un fournisseur de classes](writing-a-class-provider.md) et [écriture d’un fournisseur de propriétés](writing-a-property-provider.md).

 

Les exemples de code de cette rubrique requièrent les références suivantes et les \# instructions include pour être compilées correctement.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



La procédure suivante utilise des exemples de code C++ pour décrire comment incorporer un fournisseur découplé dans votre application. La méthode d’initialisation de l’application effectue les étapes suivantes pour que WMI interagisse uniquement avec un fournisseur découplé inscrit.

**Pour implémenter un fournisseur découplé dans une application C++**

1.  Initialise la bibliothèque COM pour une utilisation par le thread appelant.

    L’exemple de code suivant montre comment initialiser la bibliothèque COM.

    ```C++
    HRESULT hr = S_OK ;
    hr = CoInitializeEx (0, COINIT_MULTITHREADED );
    ```

    

2.  Définissez le niveau de sécurité de processus par défaut.

    Ce niveau établit le niveau de sécurité requis par d’autres processus pour accéder aux informations du processus client. Le niveau d’authentification doit être \_ le \_ \_ niveau par défaut RPC C Authn \_ . Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).

    L’exemple de code suivant montre comment définir le niveau de sécurité par défaut.

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

    

3.  Inscrire le Bureau d’enregistrement du fournisseur découplé.

    L’exemple de code suivant montre comment inscrire le Bureau d’enregistrement du fournisseur découplé.

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

    

4.  Inscrire le fournisseur d’événements découplé.

    L’exemple de code suivant montre comment inscrire le fournisseur d’événements découplé.

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

    

5.  Effectuez les [appels à WMI](making-calls-to-wmi.md) requis par la fonctionnalité du fournisseur. Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md). Pour plus d’informations, si le fournisseur fait une demande de données à partir d’un script ou d’une application, consultez [emprunt d’identité d’un client](impersonating-a-client.md).

Juste avant de se terminer, l’application doit être nettoyée après elle-même. La procédure suivante décrit comment annuler l’inscription du fournisseur découplé afin que WMI ne tente pas de l’interroger pour obtenir des informations.

La procédure suivante décrit comment annuler l’inscription du fournisseur découplé.

**Pour annuler l’inscription du fournisseur découplé**

1.  Annulez l’inscription et le lancement du Bureau d’enregistrement.

    L’exemple de code suivant montre comment annuler l’inscription et libérer le Bureau d’enregistrement.

    ```C++
    myRegistrar->UnRegister();
    myRegistrar->Release();
    ```

    

2.  Annulez l’inscription et le lancement du fournisseur d’événements.

    L’exemple de code suivant montre comment annuler l’inscription du fournisseur d’événements et le libérer.

    ```C++
    myEvtRegistrar->UnRegister();
    myEvtRegistrar->Release();
    ```

    

3.  Nettoyez le serveur COM.

    L’exemple de code suivant montre comment désinitialiser la bibliothèque COM.

    ```C++
    CoUninitialize();
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sécurisation de votre fournisseur](securing-your-provider.md)
</dt> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 



