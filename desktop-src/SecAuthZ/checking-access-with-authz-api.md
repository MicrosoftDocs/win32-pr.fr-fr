---
description: Les applications déterminent s’il faut accorder l’accès aux objets sécurisables en appelant la fonction AuthzAccessCheck.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Vérification de l’accès avec l’API auth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876c3b5305e33969f63932fdc9e1e4f6767c95a64b11272283420a377b39f795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783095"
---
# <a name="checking-access-with-authz-api"></a>Vérification de l’accès avec l’API auth

Les applications déterminent s’il faut accorder l’accès aux objets sécurisables en appelant la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

La fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) accepte à la fois les [**\_ \_ requêtes d’accès**](/windows/desktop/api/Authz/ns-authz-authz_access_request) et les structures de [**\_ descripteurs de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) en tant que paramètres. La structure de **\_ \_ demande d’accès auth** spécifie un niveau d’accès demandé. La fonction **AuthzAccessCheck** évalue l’accès demandé par rapport au **\_ descripteur de sécurité** spécifié pour un contexte client spécifié. Pour plus d’informations sur la façon dont un descripteur de sécurité contrôle l’accès à un objet, consultez la rubrique relative au [contrôle de l’accès aux DACL à un objet](how-dacls-control-access-to-an-object.md).

Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.

## <a name="callback-function"></a>Fonction de rappel

Si la [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) du [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) de l’objet à vérifier contient des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) de rappel, [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) appelle la fonction [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) pour chaque ACE de rappel contenue dans la liste DACL. Une entrée de contrôle d’accès de rappel est toute structure d’entrée du contrôle d’accès dont le type d’entrée contient le mot « callback ». La fonction **AuthzAccessCheckCallback** est une fonction définie par l’application qui doit être inscrite lorsque le gestionnaire de ressources est initialisé en appelant la fonction [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .

Une fonction de rappel permet à une application de définir la logique métier à évaluer au moment de l’exécution. Lorsque la fonction [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) est appelée, l’entrée du contrôle d’accès qui a provoqué l’appel est passée à la fonction de rappel à des fins d’évaluation. Si la logique définie par l’application a la **valeur true**, l’entrée du contrôle d’accès est incluse dans la vérification d’accès. Sinon, il est ignoré.

## <a name="caching-access-results"></a>Mise en cache des résultats d’accès

Les résultats d’une vérification d’accès peuvent être mis en cache et utilisés lors des appels ultérieurs à la fonction [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) . Pour plus d’informations sur la mise en cache des contrôles d’accès, y compris un exemple, consultez [Caching Access Checks](caching-access-checks.md).

## <a name="example"></a>Exemple

L’exemple suivant crée un [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) qui autorise l’accès au **\_ contrôle de lecture** aux administrateurs intégrés. Elle utilise ce descripteur de sécurité pour vérifier l’accès du client spécifié par le contexte client créé dans l’exemple dans l' [initialisation d’un contexte client](initializing-a-client-context.md).


```C++
BOOL CheckAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR    pSecurityDescriptor = NULL;
    ULONG                    cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST    Request;
    CHAR                    ReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY        pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    DWORD                    AuthzError =0;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

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

    //Call AuthzAccessCheck.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        NULL))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
    
        return FALSE;
    }


    //Print results.
    if(*pReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }

  LocalFree(pSecurityDescriptor);
    return TRUE;

}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ajout de sid à un contexte client](adding-sids-to-a-client-context.md)
</dt> <dt>

[Mise en cache des contrôles d’accès](caching-access-checks.md)
</dt> <dt>

[Initialisation d’un contexte client](initializing-a-client-context.md)
</dt> <dt>

[Interrogation d’un contexte client](querying-a-client-context.md)
</dt> </dl>

 

 
