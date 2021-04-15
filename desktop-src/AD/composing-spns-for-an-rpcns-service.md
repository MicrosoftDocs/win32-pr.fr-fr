---
title: Composition de SPN pour un service de RpcNs
description: L’exemple de code suivant compose les noms de principal du service (SPN) pour un service RPC qui a une entrée dans le conteneur RpcServices dans le répertoire. Un service RPC utilise la fonction RpcNsBindingExport pour créer son entrée RpcServices.
ms.assetid: 4fd585b3-3f9b-4f7f-bc1b-22879587a590
ms.tgt_platform: multiple
keywords:
- Composition de SPN pour une publicité de service de RpcNs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb65b377b5bdd041c5a34b05262f7e62f43801c5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462911"
---
# <a name="composing-spns-for-an-rpcns-service"></a>Composition de SPN pour un service de RpcNs

L’exemple de code suivant compose les noms de principal du service (SPN) pour un service RPC qui a une entrée dans le conteneur RpcServices dans le répertoire. Un service RPC utilise la fonction [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) pour créer son entrée RpcServices.

Un service RPC utilise cet exemple de code pour générer le SPN ou SPN qui identifient une instance du service. Le service utilise cette routine pour effectuer les tâches suivantes :

-   Pour inscrire ou annuler l’inscription des noms de principal du service dans le répertoire, lorsque le service est installé ou supprimé. Pour plus d’informations et pour obtenir un exemple de code, consultez [enregistrement des noms de principal du service pour un service](registering-the-spns-for-a-service.md).
-   S’inscrire auprès du service d’authentification RPC au démarrage du service. Pour plus d’informations, consultez [authentification mutuelle dans les applications RPC](mutual-authentication-in-rpc-applications.md).

Cet exemple de code utilise le nom unique de l’entrée RpcServices du service pour composer le SPN. Avant d’appeler ce code, appelez la fonction [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) pour créer l’entrée RpcServices du service.

Cet exemple de code appelle la fonction [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) pour générer un SPN. Le SPN est composé du nom de la classe de service et du nom unique de l’entrée de RpcServices de service.


```C++
/**********

    SpnCompose()

    Composes a service principal name from a service name and class.

    Parameters:

    pszServiceName - Contains a null-terminated string that contains 
    the name of the service.

    pszServiceClass - Contains a null-terminated string that contains 
    the name of the service class.

    pspn - Pointer to an LPTSTR array that receives the array of 
    SPNs. This array must freed with the DsFreeSpnArray function when 
    it is no longer required.

    pulSpn - Pointer to a unsigned long that receives the number of 
    elements in the pspn array.

***********/

HRESULT SpnCompose(LPTSTR pszServiceName, 
                   LPTSTR pszServiceClass, 
                   LPTSTR **pspn, 
                   unsigned long *pulSpn) 
{
    HRESULT hr;
    CComPtr<IADs> spRoot;

    // Get the defaultNamingContext for the local domain.
    hr = ADsGetObject(L"LDAP://RootDSE",
                      IID_IADs,
                      (void**)&spRoot);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the distinguished name of the current domain.
    CComVariant svarDSRoot;
    hr = spRoot->Get(CComBSTR("defaultNamingContext"), &svarDSRoot);
     
    /*
    Compose the DN of the service's entry in the RpcServices 
    container, created by a call to RpcNsBindingExport. The entry 
    for an RPC service is in the System/RpcServices container in the 
    defaultNamingContext of the local domain.
    */
    
    CComBSTR sbstrDsEntryName = "CN=";
    sbstrDsEntryName += pszServiceName;
    sbstrDsEntryName += ",CN=RpcServices,CN=System,";
    sbstrDsEntryName += svarDSRoot.bstrVal;

    USES_CONVERSION;  // Required for the W2T() macro.
    DWORD status;

    /*
    Build the SPN for this service using the DN and the service 
    class.
    */
    status = DsGetSpn(
        DS_SPN_SERVICE, // Type of SPN to create.
        pszServiceClass, // Service class - a name in this case.
        W2T(sbstrDsEntryName), // DN of the RpcServices for 
                               // this RPC service.
        0, // Use the default instance port.
        0, // Number of additional instance names.
        NULL, // No additional instance names.
        NULL, // No additional instance ports.
        pulSpn, // Size of SPN array.
        pspn // Returned SPN(s).
        );
     
    return HRESULT_FROM_WIN32(status);
}
```



 

 