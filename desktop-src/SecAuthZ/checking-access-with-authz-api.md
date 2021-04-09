---
description: Les applications déterminent s’il faut accorder l’accès aux objets sécurisables en appelant la fonction AuthzAccessCheck.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Vérification de l’accès avec l’API auth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e129b690a7c1f701b5f669a8f0705c5a5e9a2eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862850"
---
# <a name="checking-access-with-authz-api"></a><span data-ttu-id="a23cc-103">Vérification de l’accès avec l’API auth</span><span class="sxs-lookup"><span data-stu-id="a23cc-103">Checking Access with Authz API</span></span>

<span data-ttu-id="a23cc-104">Les applications déterminent s’il faut accorder l’accès aux objets sécurisables en appelant la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="a23cc-104">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

<span data-ttu-id="a23cc-105">La fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) accepte à la fois les [**\_ \_ requêtes d’accès**](/windows/desktop/api/Authz/ns-authz-authz_access_request) et les structures de [**\_ descripteurs de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) en tant que paramètres.</span><span class="sxs-lookup"><span data-stu-id="a23cc-105">The [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function takes both [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) and [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structures as parameters.</span></span> <span data-ttu-id="a23cc-106">La structure de **\_ \_ demande d’accès auth** spécifie un niveau d’accès demandé.</span><span class="sxs-lookup"><span data-stu-id="a23cc-106">The **AUTHZ\_ACCESS\_REQUEST** structure specifies a level of access requested.</span></span> <span data-ttu-id="a23cc-107">La fonction **AuthzAccessCheck** évalue l’accès demandé par rapport au **\_ descripteur de sécurité** spécifié pour un contexte client spécifié.</span><span class="sxs-lookup"><span data-stu-id="a23cc-107">The **AuthzAccessCheck** function evaluates the requested access against the specified **SECURITY\_DESCRIPTOR** for a specified client context.</span></span> <span data-ttu-id="a23cc-108">Pour plus d’informations sur la façon dont un descripteur de sécurité contrôle l’accès à un objet, consultez la rubrique relative au [contrôle de l’accès aux DACL à un objet](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="a23cc-108">For information about how a security descriptor controls access to an object, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="a23cc-109">Les variables d’attribut doivent être sous la forme d’une expression lorsqu’elles sont utilisées avec des opérateurs logiques ; dans le cas contraire, elles sont évaluées comme étant inconnues.</span><span class="sxs-lookup"><span data-stu-id="a23cc-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="callback-function"></a><span data-ttu-id="a23cc-110">Fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="a23cc-110">Callback Function</span></span>

<span data-ttu-id="a23cc-111">Si la [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) du [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) de l’objet à vérifier contient des [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) de rappel, [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) appelle la fonction [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) pour chaque ACE de rappel contenue dans la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="a23cc-111">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) of the object to be checked contains any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) calls the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function for each callback ACE contained in the DACL.</span></span> <span data-ttu-id="a23cc-112">Une entrée de contrôle d’accès de rappel est toute structure d’entrée du contrôle d’accès dont le type d’entrée contient le mot « callback ».</span><span class="sxs-lookup"><span data-stu-id="a23cc-112">A callback ACE is any ACE structure whose ACE type contains the word "callback."</span></span> <span data-ttu-id="a23cc-113">La fonction **AuthzAccessCheckCallback** est une fonction définie par l’application qui doit être inscrite lorsque le gestionnaire de ressources est initialisé en appelant la fonction [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="a23cc-113">The **AuthzAccessCheckCallback** function is an application-defined function that must be registered when the resource manager is initialized by calling the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function.</span></span>

<span data-ttu-id="a23cc-114">Une fonction de rappel permet à une application de définir la logique métier à évaluer au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a23cc-114">A callback function allows an application to define business logic to be evaluated at runtime.</span></span> <span data-ttu-id="a23cc-115">Lorsque la fonction [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) est appelée, l’entrée du contrôle d’accès qui a provoqué l’appel est passée à la fonction de rappel à des fins d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="a23cc-115">When the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function is called, the callback ACE that caused the call is passed to the callback function for evaluation.</span></span> <span data-ttu-id="a23cc-116">Si la logique définie par l’application a la **valeur true**, l’entrée du contrôle d’accès est incluse dans la vérification d’accès.</span><span class="sxs-lookup"><span data-stu-id="a23cc-116">If the application-defined logic evaluates as **TRUE**, then the callback ACE is included in the access check.</span></span> <span data-ttu-id="a23cc-117">Sinon, il est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a23cc-117">Otherwise, it is ignored.</span></span>

## <a name="caching-access-results"></a><span data-ttu-id="a23cc-118">Mise en cache des résultats d’accès</span><span class="sxs-lookup"><span data-stu-id="a23cc-118">Caching Access Results</span></span>

<span data-ttu-id="a23cc-119">Les résultats d’une vérification d’accès peuvent être mis en cache et utilisés lors des appels ultérieurs à la fonction [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="a23cc-119">The results of an access check can be cached and used in future calls to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="a23cc-120">Pour plus d’informations sur la mise en cache des contrôles d’accès, y compris un exemple, consultez [Caching Access Checks](caching-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="a23cc-120">For more information about caching access checks, including an example, see [Caching Access Checks](caching-access-checks.md).</span></span>

## <a name="example"></a><span data-ttu-id="a23cc-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="a23cc-121">Example</span></span>

<span data-ttu-id="a23cc-122">L’exemple suivant crée un [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) qui autorise l’accès au **\_ contrôle de lecture** aux administrateurs intégrés.</span><span class="sxs-lookup"><span data-stu-id="a23cc-122">The following example creates a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) that allows **READ\_CONTROL** access to built-in administrators.</span></span> <span data-ttu-id="a23cc-123">Elle utilise ce descripteur de sécurité pour vérifier l’accès du client spécifié par le contexte client créé dans l’exemple dans l' [initialisation d’un contexte client](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="a23cc-123">It uses that security descriptor to check access for the client specified by the client context created in the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a23cc-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a23cc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a23cc-125">Ajout de sid à un contexte client</span><span class="sxs-lookup"><span data-stu-id="a23cc-125">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="a23cc-126">Mise en cache des contrôles d’accès</span><span class="sxs-lookup"><span data-stu-id="a23cc-126">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="a23cc-127">Initialisation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="a23cc-127">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="a23cc-128">Interrogation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="a23cc-128">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
