---
description: Une application peut ajouter des identificateurs de sécurité (SID) à un contexte client existant en appelant la fonction AuthzAddSidsToContext.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Ajout de sid à un contexte client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07805031d299efc400c491c7fff1c43653e90b53f6c753c81a8676d4b0941b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784921"
---
# <a name="adding-sids-to-a-client-context"></a>Ajout de sid à un contexte client

Une application peut ajouter des [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) à un contexte client existant en appelant la fonction [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) . La fonction [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) permet à une application de spécifier à la fois une liste de sid et une liste de sid restreints au contexte client spécifié.

Le système utilise la liste des SID restreints lorsqu’il vérifie l’accès du jeton à un objet sécurisable. Quand un processus ou un thread restreint tente d’accéder à un objet sécurisable, le système effectue deux vérifications d’accès : une utilisant les SID activés du jeton et une autre à l’aide de la liste des SID de restriction. L’accès est accordé uniquement si les deux contrôles d’accès autorisent les droits d’accès demandés.

Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.

## <a name="example"></a> Exemple

L’exemple suivant ajoute un SID et un SID restreint au contexte client créé par l’exemple dans [initialisation d’un contexte client](initializing-a-client-context.md).


```C++
BOOL AddSidsToContext(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{
    AUTHZ_CLIENT_CONTEXT_HANDLE        NewContext = NULL;
    PSID                            pEveryoneSid = NULL;
    PSID                            pLocalSid = NULL;
    SID_AND_ATTRIBUTES                Sids;
    SID_AND_ATTRIBUTES                RestrictedSids;
    DWORD                            SidCount = 0;
    DWORD                            RestrictedSidCount = 0;

    //Create a PSID from the "Everyone" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-1-0", &pEveryoneSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError());
        return FALSE;
    }

    //Create a PSID from the "Local" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-2-0", &pLocalSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError);
        return FALSE;
    }

    //Set the members of the SID_AND_ATTRIBUTES structure to be added.
    Sids.Sid = pEveryoneSid;
    Sids.Attributes = SE_GROUP_ENABLED;

    //Set the members of the SID_AND_ATTRIBUTES structure for the restricting SID.
    RestrictedSids.Sid = pLocalSid;
    RestrictedSids.Attributes = SE_GROUP_ENABLED;

    

    //Create a new context with the new "Everyone" SID and "Local" restricting SID.
    if(!AuthzAddSidsToContext(
        *phClientContext,
        &Sids,
        1,
        &RestrictedSids,
        1,
        &NewContext))
    {
        printf_s("AuthzAddSidsToContext failed with %d\n", GetLastError());
        if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        return FALSE;
    }

    if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        
        AuthzFreeContext(*phClientContext);
        *phClientContext = NewContext;

    return TRUE;

}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise en cache des contrôles d’accès](caching-access-checks.md)
</dt> <dt>

[Vérification de l’accès avec l’API auth](checking-access-with-authz-api.md)
</dt> <dt>

[Initialisation d’un contexte client](initializing-a-client-context.md)
</dt> <dt>

[Interrogation d’un contexte client](querying-a-client-context.md)
</dt> </dl>

 

 
