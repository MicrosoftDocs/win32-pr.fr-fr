---
description: Une application doit créer un contexte client pour pouvoir utiliser l’API auth pour effectuer des vérifications d’accès ou un audit.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Initialisation d’un contexte client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be229a60a12e33ab0c2bbd3e52fc533cf29ed1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530713"
---
# <a name="initializing-a-client-context"></a><span data-ttu-id="bd056-103">Initialisation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="bd056-103">Initializing a Client Context</span></span>

<span data-ttu-id="bd056-104">Une application doit créer un contexte client pour pouvoir utiliser l’API auth pour effectuer des vérifications d’accès ou un audit.</span><span class="sxs-lookup"><span data-stu-id="bd056-104">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span>

<span data-ttu-id="bd056-105">Une application doit appeler la fonction [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) pour initialiser le gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="bd056-105">An application must call the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function to initialize the resource manager.</span></span> <span data-ttu-id="bd056-106">L’application peut ensuite appeler l’une des fonctions suivantes pour créer un contexte client.</span><span class="sxs-lookup"><span data-stu-id="bd056-106">The application can then call one of several functions to create a client context.</span></span> <span data-ttu-id="bd056-107">En outre, si vous effectuez des vérifications d’accès ou un audit à distance, vous devez utiliser la fonction [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="bd056-107">Additionally, if you are performing access checks or auditing remotely, you must use the [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) function.</span></span>

<span data-ttu-id="bd056-108">Pour créer un contexte client basé sur un contexte client existant, appelez la fonction [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .</span><span class="sxs-lookup"><span data-stu-id="bd056-108">To create a client context based on an existing client context, call the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) function.</span></span>

<span data-ttu-id="bd056-109">La fonction [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) crée un nouveau contexte client à l’aide des informations contenues dans un jeton d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="bd056-109">The [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function creates a new client context by using information in a logon token.</span></span> <span data-ttu-id="bd056-110">La fonction [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) crée un nouveau contexte client à l’aide du [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid)spécifié.</span><span class="sxs-lookup"><span data-stu-id="bd056-110">The [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) function creates a new client context by using the specified [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid).</span></span>

<span data-ttu-id="bd056-111">Si possible, appelez la fonction [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) à la place de [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span><span class="sxs-lookup"><span data-stu-id="bd056-111">If possible, call the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function instead of [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span></span> <span data-ttu-id="bd056-112">**AuthzInitializeContextFromSid** tente de récupérer les informations disponibles dans un jeton d’ouverture de session si le client est actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="bd056-112">**AuthzInitializeContextFromSid** attempts to retrieve the information available in a logon token had the client actually logged on.</span></span> <span data-ttu-id="bd056-113">Un jeton d’ouverture de session réel fournit plus d’informations, telles que le type de connexion et les propriétés de connexion, et reflète le comportement du package d’authentification utilisé pour l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="bd056-113">An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon.</span></span> <span data-ttu-id="bd056-114">Le contexte client créé par **AuthzInitializeContextFromToken** utilise un jeton d’ouverture de session et le contexte client résultant est plus complet et précis qu’un contexte client créé par **AuthzInitializeContextFromSid**.</span><span class="sxs-lookup"><span data-stu-id="bd056-114">The client context created by **AuthzInitializeContextFromToken** uses a logon token, and the resulting client context is more complete and accurate than a client context created by **AuthzInitializeContextFromSid**.</span></span>

> [!Note]  
> <span data-ttu-id="bd056-115">Les variables d’attribut de sécurité doivent être présentes dans le contexte client si elles sont référencées dans une expression conditionnelle ; dans le cas contraire, le terme des expressions conditionnelles qui les référencera sera évalué comme inconnu.</span><span class="sxs-lookup"><span data-stu-id="bd056-115">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="bd056-116">Pour plus d’informations sur les expressions conditionnelles, consultez la rubrique [langage de définition du descripteur de sécurité pour les ACE conditionnel](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="bd056-116">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

 

## <a name="example"></a><span data-ttu-id="bd056-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="bd056-117">Example</span></span>

<span data-ttu-id="bd056-118">L’exemple suivant initialise le gestionnaire de ressources authz et appelle la fonction [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) pour créer un contexte client à partir du jeton d’ouverture de session associé au processus en cours.</span><span class="sxs-lookup"><span data-stu-id="bd056-118">The following example initializes the Authz resource manager and calls the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function to create a client context from the logon token associated with the current process.</span></span>


```C++
BOOL AuthzInitFromToken(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{

    HANDLE                            hToken = NULL;
    LUID                            Luid = {0, 0};

    
    ULONG                            uFlags = 0;


    //Initialize Resource Manager
    if(!AuthzInitializeResourceManager(
        AUTHZ_RM_FLAG_NO_AUDIT,
        NULL,
        NULL,
        NULL,
        L"My Resource Manager",
        &g_hResourceManager
        ))
    {
        printf_s("AuthzInitializeResourceManager failed with %d\n", GetLastError);
        return FALSE;
    }
    

    //Get the current token.

    if(!OpenProcessToken(GetCurrentProcess(), TOKEN_ALL_ACCESS, &hToken))
    {
        printf_s("OpenProcessToken failed with %d\n", GetLastError);
        return FALSE;
    }


    //Initialize the client context

    if(!AuthzInitializeContextFromToken(
        0,
        hToken,
        g_hResourceManager,
        NULL,
        Luid,
        NULL,
        phClientContext
        ))
    {    
        printf_s("AuthzInitializeContextFromToken failed with %d\n", GetLastError);
        return FALSE;
    }

    
    printf_s("Initialized client context. \n");
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="bd056-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd056-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd056-120">Ajout de sid à un contexte client</span><span class="sxs-lookup"><span data-stu-id="bd056-120">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="bd056-121">Mise en cache des contrôles d’accès</span><span class="sxs-lookup"><span data-stu-id="bd056-121">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="bd056-122">Vérification de l’accès avec l’API auth</span><span class="sxs-lookup"><span data-stu-id="bd056-122">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="bd056-123">Fonctionnement de AccessCheck</span><span class="sxs-lookup"><span data-stu-id="bd056-123">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="bd056-124">Interrogation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="bd056-124">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="bd056-125">Langage de définition du descripteur de sécurité pour les ACE conditionnelles</span><span class="sxs-lookup"><span data-stu-id="bd056-125">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="bd056-126">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="bd056-126">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="bd056-127">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="bd056-127">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



