---
description: Windows Management Instrumentation (WMI) peut créer le récepteur pour recevoir des rappels asynchrones pour une application cliente dans un processus séparé.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Diminution de la sécurité d’un récepteur dans un processus distinct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521828"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a>Diminution de la sécurité d’un récepteur dans un processus distinct

Windows Management Instrumentation (WMI) peut créer le récepteur pour recevoir des rappels asynchrones pour une application cliente dans un processus séparé. Le processus distinct est Unsecapp.exe. Utilisez l’interface [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) . **IWbemUnsecuredApartment** vous permet de contrôler si Unsecapp.exe authentifie les rappels sur le récepteur. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

Vous pouvez ensuite réduire la sécurité sur ce processus et WMI peut accéder au récepteur sans restriction. Pour faciliter cette technique, WMI fournit le processus de Unsecapp.exe pour fonctionner en tant que processus distinct. Vous pouvez héberger des Unsecapp.exe à l’aide d’un appel à l’interface [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) .

L’interface [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) permet à une application cliente de créer un processus dédié distinct exécutant Unsecapp.exe pour héberger une implémentation [**IWbemObjectSink**](iwbemobjectsink.md) . Le processus dédié peut appeler [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour accorder l’accès WMI au processus dédié sans compromettre la sécurité du processus principal. Après l’initialisation, le processus dédié agit comme un intermédiaire entre le processus principal et WMI.

La procédure suivante décrit comment effectuer un appel asynchrone avec [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).

**Pour effectuer un appel asynchrone avec IUnsecuredApartment**

1.  Créez un processus dédié avec un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    L’exemple de code suivant appelle [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un processus dédié.

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  Instanciez l’objet récepteur.

    L’exemple de code suivant crée un nouvel objet récepteur.

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  Créez un stub pour le récepteur.

    Un stub est une fonction wrapper produite à partir du récepteur.

    L’exemple de code suivant appelle [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) pour créer un stub pour le récepteur.

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  Appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour le wrapper et demandez un pointeur vers l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    L’exemple de code suivant appelle [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) et demande un pointeur vers l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  Libère le pointeur d’objet récepteur.

    Vous pouvez libérer le pointeur d’objet, car le stub est désormais propriétaire du pointeur.

    L’exemple de code suivant libère le pointeur d’objet récepteur.

    ```C++
    pSink->Release();
    ```

    

6.  Utilisez le stub dans n’importe quel appel asynchrone.

    Lorsque vous avez terminé avec l’appel, libérez le nombre de références locales.

    L’exemple de code suivant utilise le stub dans un appel asynchrone.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    Parfois, vous devrez peut-être annuler un appel asynchrone après avoir effectué l’appel. Si vous devez annuler l’appel, annulez l’appel avec le même pointeur que celui qui a initialement effectué l’appel.

    L’exemple de code suivant montre comment annuler un appel asynchrone.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  Libérez le nombre de références locales lorsque vous avez fini d’utiliser l’appel asynchrone.

    Veillez à libérer le pointeur *pStubSink* uniquement après avoir confirmé que l’appel asynchrone n’a pas besoin d’être annulé. En outre, ne libérez pas *pStubSink* après la libération du pointeur du récepteur *pSink* par WMI. La libération de *pStubSink* après *pSink* crée un nombre de références circulaires dans lequel le récepteur et le stub restent en mémoire indéfiniment. Au lieu de cela, un emplacement possible pour libérer le pointeur se trouve dans l’appel [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , créé par WMI pour signaler que l’appel asynchrone d’origine est terminé.

8.  Lorsque vous avez terminé, désinitialisez COM à l’aide d’un appel à [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

    L’exemple de code suivant montre comment appeler [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur *pUnsecApp* .

    ```C++
    pUnsecApp->Release();
    ```

    

    Les exemples de code de cette rubrique requièrent la référence suivante et l' \# instruction include pour compiler correctement.

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

Pour plus d’informations sur la fonction [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) et les paramètres, consultez la documentation [com](../cossdk/component-services-portal.md) dans le kit de développement logiciel (SDK) de la plateforme.

 

 
