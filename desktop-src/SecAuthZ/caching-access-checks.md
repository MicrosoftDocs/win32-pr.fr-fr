---
description: Quand une application effectue une vérification d’accès en appelant la fonction AuthzAccessCheck, les résultats de cette vérification d’accès peuvent être mis en cache.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Mise en cache des contrôles d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83659c35fb9334e55bd7dfcd2368275dc16eb0d4836b8d6fa69a6ed8d713d953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783554"
---
# <a name="caching-access-checks"></a>Mise en cache des contrôles d’accès

Quand une application effectue une vérification d’accès en appelant la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , les résultats de cette vérification d’accès peuvent être mis en cache. Lorsque le paramètre *pAuthzHandle* de la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) n’a pas la **valeur null**, la fonction effectue un contrôle d’accès distinct, avec un [**\_ masque d’accès**](access-mask.md) requis de la **valeur maximale \_ autorisée** et met en cache les résultats de cette vérification. Un handle vers les résultats de cette vérification peut ensuite être passé comme paramètre *AuthzHandle* à la fonction [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) . Cela permet un contrôle d’accès plus rapide pour un client donné et des [*descripteurs de sécurité*](/windows/desktop/SecGloss/s-gly).

Seule la partie statique d’une vérification d’accès peut être mise en cache. Les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) de rappel ou les ACE qui contiennent l' **\_ auto** -SID principal doivent être évaluées pour chaque vérification d’accès.

Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.

## <a name="example"></a>Exemple

L’exemple suivant vérifie l’accès par rapport à un résultat mis en cache à partir d’une vérification d’accès précédente. La vérification d’accès précédente a été effectuée dans l’exemple de vérification de l' [accès avec l’API auth](checking-access-with-authz-api.md).


```C++
BOOL CheckCachedAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR                pSecurityDescriptor = NULL;
    ULONG                                cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST                Request;
    CHAR                                ReplyBuffer[MY_MAX];
    CHAR                                CachedReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY                    pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    PAUTHZ_ACCESS_REPLY                    pCachedReply = (PAUTHZ_ACCESS_REPLY)CachedReplyBuffer;
    DWORD                                AuthzError =0;
    AUTHZ_ACCESS_CHECK_RESULTS_HANDLE    hCached;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the initial access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Allocate memory for the cached access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the cached access reply structure.
    pCachedReply->ResultListLength = 1;
    pCachedReply->Error = (PDWORD) ((PCHAR) pCachedReply + sizeof(AUTHZ_ACCESS_REPLY));
    pCachedReply->GrantedAccessMask = (PACCESS_MASK) (pCachedReply->Error + pCachedReply->ResultListLength);
    pCachedReply->SaclEvaluationResults = NULL;

    //Create security descriptor.
    if(!ConvertStringSecurityDescriptorToSecurityDescriptor(
        L"O:LAG:BAD:(A;;RC;;;BA)",
        SDDL_REVISION_1,
        &pSecurityDescriptor,
        NULL))
    {
        printf_s("ConvertStringSecurityDescriptorToSecurityDescriptor failed with %d\n", GetLastError()); 
        return FALSE;
    }

    //Call AuthzAccessCheck and cache results.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        &hCached))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
        
        return FALSE;
    }

    //Call AuthzCachedAccessCheck with the cached result from the previous call.
    if(!AuthzCachedAccessCheck(
        0,
        hCached,
        &Request,
        NULL,
        pCachedReply))
    {
        printf_s("AuthzCachedAccessCheck failed with %d\n", GetLastError());
        
        LocalFree(pSecurityDescriptor);
    AuthzFreeHandle(hCached);
    
        return FALSE;
    }

    //Print results.
    if(*pCachedReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }


  LocalFree(pSecurityDescriptor);
  AuthzFreeHandle(hCached);
    return TRUE;

}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ajout de sid à un contexte client](adding-sids-to-a-client-context.md)
</dt> <dt>

[Vérification de l’accès avec l’API auth](checking-access-with-authz-api.md)
</dt> <dt>

[Initialisation d’un contexte client](initializing-a-client-context.md)
</dt> <dt>

[Interrogation d’un contexte client](querying-a-client-context.md)
</dt> </dl>

 

 
