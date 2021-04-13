---
description: Quand une application effectue une vérification d’accès en appelant la fonction AuthzAccessCheck, les résultats de cette vérification d’accès peuvent être mis en cache.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Mise en cache des contrôles d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967e0a5398d93c1715d7d08e5c7c75695e4120ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321210"
---
# <a name="caching-access-checks"></a><span data-ttu-id="0008f-103">Mise en cache des contrôles d’accès</span><span class="sxs-lookup"><span data-stu-id="0008f-103">Caching Access Checks</span></span>

<span data-ttu-id="0008f-104">Quand une application effectue une vérification d’accès en appelant la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , les résultats de cette vérification d’accès peuvent être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="0008f-104">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span> <span data-ttu-id="0008f-105">Lorsque le paramètre *pAuthzHandle* de la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) n’a pas la **valeur null**, la fonction effectue un contrôle d’accès distinct, avec un [**\_ masque d’accès**](access-mask.md) requis de la **valeur maximale \_ autorisée** et met en cache les résultats de cette vérification.</span><span class="sxs-lookup"><span data-stu-id="0008f-105">When the *pAuthzHandle* parameter of the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function is not **NULL**, the function performs a separate access check, with a requested [**ACCESS\_MASK**](access-mask.md) of **MAXIMUM\_ALLOWED**, and caches the results of that check.</span></span> <span data-ttu-id="0008f-106">Un handle vers les résultats de cette vérification peut ensuite être passé comme paramètre *AuthzHandle* à la fonction [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="0008f-106">A handle to the results of that check can then be passed as the *AuthzHandle* parameter to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="0008f-107">Cela permet un contrôle d’accès plus rapide pour un client donné et des [*descripteurs de sécurité*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="0008f-107">This allows faster access checking for a given client and [*security descriptors*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="0008f-108">Seule la partie statique d’une vérification d’accès peut être mise en cache.</span><span class="sxs-lookup"><span data-stu-id="0008f-108">Only the static portion of an access check can be cached.</span></span> <span data-ttu-id="0008f-109">Les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) de rappel ou les ACE qui contiennent l' **\_ auto** -SID principal doivent être évaluées pour chaque vérification d’accès.</span><span class="sxs-lookup"><span data-stu-id="0008f-109">Any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) or ACEs that contain the **PRINCIPAL\_SELF** SID must be evaluated for each access check.</span></span>

<span data-ttu-id="0008f-110">Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.</span><span class="sxs-lookup"><span data-stu-id="0008f-110">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="0008f-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="0008f-111">Example</span></span>

<span data-ttu-id="0008f-112">L’exemple suivant vérifie l’accès par rapport à un résultat mis en cache à partir d’une vérification d’accès précédente.</span><span class="sxs-lookup"><span data-stu-id="0008f-112">The following example checks access against a cached result from a previous access check.</span></span> <span data-ttu-id="0008f-113">La vérification d’accès précédente a été effectuée dans l’exemple de vérification de l' [accès avec l’API auth](checking-access-with-authz-api.md).</span><span class="sxs-lookup"><span data-stu-id="0008f-113">The previous access check was performed in the example in [Checking Access with Authz API](checking-access-with-authz-api.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0008f-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0008f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0008f-115">Ajout de sid à un contexte client</span><span class="sxs-lookup"><span data-stu-id="0008f-115">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="0008f-116">Vérification de l’accès avec l’API auth</span><span class="sxs-lookup"><span data-stu-id="0008f-116">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="0008f-117">Initialisation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="0008f-117">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="0008f-118">Interrogation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="0008f-118">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
