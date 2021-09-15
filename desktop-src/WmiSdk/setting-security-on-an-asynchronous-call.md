---
description: Les appels asynchrones présentent des risques sérieux pour la sécurité, car un rappel au récepteur peut ne pas être le résultat de l’appel asynchrone par l’application ou le script d’origine.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Définition de la sécurité sur un appel asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403584"
---
# <a name="setting-security-on-an-asynchronous-call"></a>Définition de la sécurité sur un appel asynchrone

Les appels asynchrones présentent des risques sérieux pour la sécurité, car un rappel au [*récepteur*](gloss-s.md) peut ne pas être le résultat de l’appel asynchrone par l’application ou le script d’origine. La sécurité des connexions à distance est basée sur le chiffrement de la communication entre le client et le fournisseur sur l’ordinateur distant. En C++, vous pouvez définir le chiffrement via le paramètre de niveau d’authentification dans l’appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Dans les scripts, définissez *AuthenticationLevel* dans la connexion moniker ou sur un objet [**SWbemSecurity**](swbemsecurity.md) . Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

Il existe des risques de sécurité pour les appels asynchrones, car WMI réduit le niveau d’authentification sur un rappel jusqu’à ce que le rappel aboutisse. Sur un appel asynchrone sortant, le client peut définir le niveau d’authentification de la connexion à WMI. WMI récupère les paramètres de sécurité de l’appel client et tente d’effectuer un rappel avec le même niveau d’authentification. Le rappel est toujours initié au niveau de confidentialité de l' **\_ authentification au niveau d' \_ authentification \_ \_ \_ RPC C** . Si le rappel échoue, WMI réduit le niveau d’authentification à un niveau où le rappel peut être réussi, le cas échéant, au niveau d’authentification **RPC \_ C \_ \_ \_** sans. Dans le contexte des appels au sein du système local où le service d’authentification n’est pas Kerberos, le rappel est toujours retourné au **\_ niveau d’authentification RPC C- \_ \_ \_ None**.

Le niveau d’authentification minimal est **RPC \_ C \_ Authn \_ niveau \_** (**wbemAuthenticationLevelPkt** pour les scripts). Toutefois, vous pouvez spécifier un niveau plus élevé, tel que laconfidentialité de l' **\_ \_ authentification \_ au niveau \_ \_** de l’authentification (wbemAuthenticationLevelPktPrivacy) RPC C. Il est recommandé que les applications clientes ou les scripts définissent le niveau d’authentification à la valeur **\_ \_ \_ \_ par défaut du niveau d’authentification RPC C** (**wbemAuthenticationLevelDefault**), ce qui permet de négocier le niveau d’authentification au niveau spécifié par le serveur.

La valeur de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** contrôle si WMI vérifie la présence d’un niveau d’authentification acceptable dans les rappels. Il s’agit du seul mécanisme de protection de la sécurité du récepteur pour les appels asynchrones effectués dans des scripts ou des Visual Basic. Par défaut, cette clé de Registre est définie sur zéro. Si la clé de Registre est égale à zéro, WMI ne vérifie pas les niveaux d’authentification. Pour sécuriser les appels asynchrones dans les scripts, affectez la valeur 1 à la clé de registre. Les clients C++ peuvent appeler [**IWbemUnsecuredApartment :: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) pour contrôler l’accès au récepteur. La valeur est créée n’importe où par défaut.

Les rubriques suivantes fournissent des exemples de définition de la sécurité des appels asynchrones :

-   [Définition de la sécurité sur un appel asynchrone dans VBScript](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   Définition de la sécurité des appels asynchrones en C++

## <a name="setting-asynchronous-call-security-in-c"></a>Définition de la sécurité des appels asynchrones en C++

La méthode [**IWbemUnsecuredApartment :: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) est semblable à la méthode [**IUnsecuredApartment :: CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) et crée un récepteur dans un processus séparé, Unsecapp.exe, pour recevoir des rappels. Toutefois, la méthode **CreateSinkStub** a un paramètre *dwFlag* qui spécifie comment le processus distinct gère le contrôle d’accès.

Le paramètre *dwFlag* spécifie l’une des actions suivantes pour Unsecapp.exe :

-   Utilisez le paramètre de clé de Registre pour déterminer s’il faut ou non vérifier l’accès.
-   Ignorez la clé de Registre et vérifiez toujours l’accès.
-   Ignorer la clé de Registre et ne jamais vérifier l’accès.

L’exemple de code de cette rubrique requiert l' \# instruction include suivante pour compiler correctement.


```C++
#include <wbemidl.h>
```



La procédure suivante décrit comment effectuer un appel asynchrone avec [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).

**Pour effectuer un appel asynchrone avec IWbemUnsecuredApartment**

1.  Créez un processus dédié avec un appel à [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    L’exemple de code suivant appelle [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un processus dédié.

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
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

    L’exemple de code suivant crée un stub pour le récepteur.

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  Libère le pointeur d’objet récepteur.

    Vous pouvez libérer le pointeur d’objet, car le stub est désormais propriétaire du pointeur.

    L’exemple de code suivant libère le pointeur d’objet.

    ```C++
    pSink->Release();
    ```

    

5.  Utilisez le stub dans n’importe quel appel asynchrone.

    Lorsque vous avez terminé avec l’appel, libérez le nombre de références locales.

    L’exemple de code suivant utilise le stub dans un appel asynchrone.

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    Parfois, vous devrez peut-être annuler un appel asynchrone après avoir effectué l’appel. Si vous devez annuler l’appel, annulez l’appel avec le même pointeur que celui qui a initialement effectué l’appel.

    L’exemple de code suivant décrit comment annuler un appel asynchrone.

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  Libérez le nombre de références locales lorsque vous avez fini d’utiliser l’appel asynchrone.

    Veillez à libérer le pointeur *pStubSink* uniquement après avoir vérifié que l’appel asynchrone ne doit pas être annulé. En outre, ne libérez pas *pStubSink* après la libération du pointeur du récepteur *pSink* par WMI. La libération de *pStubSink* après *pSink* crée un nombre de références circulaires dans lequel le récepteur et le stub restent en mémoire indéfiniment. Au lieu de cela, un emplacement possible pour libérer le pointeur se trouve dans l’appel [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , créé par WMI pour signaler que l’appel asynchrone d’origine est terminé.

7.  Lorsque vous avez terminé, désinitialisez COM à l’aide d’un appel à [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

    L’exemple de code suivant montre comment appeler [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur *pUnsecApp* .

    ```C++
    pUnsecApp->Release();
    ```

    

Pour plus d’informations sur la fonction [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) et les paramètres, consultez la documentation [com](../cossdk/component-services-portal.md) .

 

 
