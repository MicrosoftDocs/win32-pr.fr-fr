---
description: Une application peut ajouter des identificateurs de sécurité (SID) à un contexte client existant en appelant la fonction AuthzAddSidsToContext.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Ajout de sid à un contexte client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a601f485110ddacea0fdb54cb7dcef587a25cb9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529728"
---
# <a name="adding-sids-to-a-client-context"></a><span data-ttu-id="d45bc-103">Ajout de sid à un contexte client</span><span class="sxs-lookup"><span data-stu-id="d45bc-103">Adding SIDs to a Client Context</span></span>

<span data-ttu-id="d45bc-104">Une application peut ajouter des [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) à un contexte client existant en appelant la fonction [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="d45bc-104">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span> <span data-ttu-id="d45bc-105">La fonction [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) permet à une application de spécifier à la fois une liste de sid et une liste de sid restreints au contexte client spécifié.</span><span class="sxs-lookup"><span data-stu-id="d45bc-105">The [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function allows an application to specify both a list of SIDs and a list of restricting SIDs to the specified client context.</span></span>

<span data-ttu-id="d45bc-106">Le système utilise la liste des SID restreints lorsqu’il vérifie l’accès du jeton à un objet sécurisable.</span><span class="sxs-lookup"><span data-stu-id="d45bc-106">The system uses the list of restricting SIDs when it checks the token's access to a securable object.</span></span> <span data-ttu-id="d45bc-107">Quand un processus ou un thread restreint tente d’accéder à un objet sécurisable, le système effectue deux vérifications d’accès : une utilisant les SID activés du jeton et une autre à l’aide de la liste des SID de restriction.</span><span class="sxs-lookup"><span data-stu-id="d45bc-107">When a restricted process or thread tries to access a securable object, the system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs.</span></span> <span data-ttu-id="d45bc-108">L’accès est accordé uniquement si les deux contrôles d’accès autorisent les droits d’accès demandés.</span><span class="sxs-lookup"><span data-stu-id="d45bc-108">Access is granted only if both access checks allow the requested access rights.</span></span>

<span data-ttu-id="d45bc-109">Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.</span><span class="sxs-lookup"><span data-stu-id="d45bc-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="d45bc-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="d45bc-110">Example</span></span>

<span data-ttu-id="d45bc-111">L’exemple suivant ajoute un SID et un SID restreint au contexte client créé par l’exemple dans [initialisation d’un contexte client](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="d45bc-111">The following example adds a SID and a restricting SID to the client context created by the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d45bc-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d45bc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d45bc-113">Mise en cache des contrôles d’accès</span><span class="sxs-lookup"><span data-stu-id="d45bc-113">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="d45bc-114">Vérification de l’accès avec l’API auth</span><span class="sxs-lookup"><span data-stu-id="d45bc-114">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="d45bc-115">Initialisation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="d45bc-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="d45bc-116">Interrogation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="d45bc-116">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
