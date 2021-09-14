---
title: Écriture d’un serveur SSPI authentifié
description: Avant que la communication authentifiée puisse avoir lieu entre les programmes client et serveur, le serveur doit enregistrer ses informations d’authentification.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- Appel de procédure distante RPC, tâches, écriture d’un serveur SSPI authentifié
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011366"
---
# <a name="writing-an-authenticated-sspi-server"></a>Écriture d’un serveur SSPI authentifié

Avant que la communication authentifiée puisse avoir lieu entre les programmes client et serveur, le serveur doit enregistrer ses informations d’authentification. En particulier, le serveur doit inscrire son nom principal et spécifier le service d’authentification qu’il utilise. Pour plus d’informations sur les noms principaux, consultez [noms principaux](principal-names.md). Pour plus d’informations sur les services d’authentification, consultez [services d’authentification](authentication-services.md).

Pour enregistrer ses informations d’authentification, les serveurs appellent la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) . Transmettez un pointeur vers le nom principal en tant que valeur du premier paramètre. Définissez le deuxième paramètre sur une constante indiquant le service d’authentification que l’application utilisera. Pour obtenir une description des services d’authentification, consultez la rubrique relative [aux constantes de service d’authentification](authentication-service-constants.md).

Le serveur peut également passer l’adresse d’une fonction d’acquisition de clé comme valeur du troisième paramètre. Consultez [fonctions d’acquisition de clés](key-acquisition-functions.md). Pour utiliser la fonction d’acquisition de clé par défaut pour le service d’authentification sélectionné, définissez le troisième paramètre sur la **valeur null**. Le dernier paramètre de la fonction [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) est une donnée de pointeur à passer à la fonction d’acquisition de clé, si vous fournissez une fonction d’acquisition de clé. Un appel à **RpcServerRegisterAuthInfo** est indiqué dans le fragment de code suivant.


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



En outre, le serveur peut fournir la bibliothèque Runtime RPC avec une fonction d’autorisation. Pour définir une fonction d’autorisation, appelez la fonction [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) .

La partie serveur d’une application distribuée peut appeler la fonction [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) ou [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) pour interroger un handle de liaison afin d’obtenir des informations d’authentification.

Si votre serveur s’inscrit auprès d’un fournisseur de support de sécurité, les appels clients avec des informations d’identification non valides ne seront pas distribués. Toutefois, les appels sans informations d’identification seront distribués. Il existe trois façons d’éviter ce problème :

-   Inscrire l’interface à l’aide de [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), avec une fonction de rappel de sécurité ; en conséquence, la bibliothèque Runtime RPC rejette automatiquement les appels non authentifiés à cette interface. L’inscription d’une fonction de rappel est compatible avec d’autres méthodes de vérification des informations d’identification d’accès ; la fonction de rappel peut elle-même appeler les fonctions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)ou [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) , ou d’autres. Toutefois, ces fonctions ne peuvent pas utiliser les arguments passés à la fonction, car ils ne sont pas démarshalés à ce stade.

> [!IMPORTANT]
> L’inscription de l’interface à l’aide de [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) avec une fonction de rappel de sécurité est la méthode la plus fortement recommandée pour vérifier les informations d’identification du client.

 

-   Appelez [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) pour déterminer le niveau de sécurité utilisé par le client. Votre stub peut ensuite retourner une erreur si le client n’est pas authentifié.

 

 




