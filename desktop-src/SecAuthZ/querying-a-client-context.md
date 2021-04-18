---
description: Les applications peuvent appeler la fonction AuthzGetInformationFromContext pour demander des informations sur un contexte client existant.
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: Interrogation d’un contexte client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101c35466e675d9ecba942089bbe7b5e82cffd90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520380"
---
# <a name="querying-a-client-context"></a><span data-ttu-id="cc161-103">Interrogation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="cc161-103">Querying a Client Context</span></span>

<span data-ttu-id="cc161-104">Les applications peuvent appeler la fonction [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) pour demander des informations sur un contexte client existant.</span><span class="sxs-lookup"><span data-stu-id="cc161-104">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span>

<span data-ttu-id="cc161-105">Le paramètre *InfoClass* de la fonction [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) accepte une valeur de l’énumération de [**\_ \_ \_ classe d’informations de contexte auth**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) qui spécifie le type d’informations que la fonction interroge.</span><span class="sxs-lookup"><span data-stu-id="cc161-105">The *InfoClass* parameter of the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function takes a value from the [**AUTHZ\_CONTEXT\_INFORMATION\_CLASS**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) enumeration that specifies what type of information the function queries.</span></span>

<span data-ttu-id="cc161-106">Les variables d’attribut de sécurité doivent être présentes dans le contexte client si elles sont référencées dans une expression conditionnelle ; dans le cas contraire, le terme des expressions conditionnelles qui les référencera sera évalué comme inconnu.</span><span class="sxs-lookup"><span data-stu-id="cc161-106">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="cc161-107">Pour plus d’informations sur les expressions conditionnelles, consultez la rubrique [langage de définition du descripteur de sécurité pour les ACE conditionnel](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="cc161-107">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

## <a name="example"></a><span data-ttu-id="cc161-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="cc161-108">Example</span></span>

<span data-ttu-id="cc161-109">L’exemple suivant interroge le contexte client créé dans l’exemple à partir de l' [initialisation d’un contexte client](initializing-a-client-context.md) pour récupérer la liste des [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) des groupes associés à ce contexte client.</span><span class="sxs-lookup"><span data-stu-id="cc161-109">The following example queries the client context created in the example from [Initializing a Client Context](initializing-a-client-context.md) to retrieve the list of [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) of groups associated with that client context.</span></span>


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="cc161-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc161-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc161-111">Ajout de sid à un contexte client</span><span class="sxs-lookup"><span data-stu-id="cc161-111">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="cc161-112">Mise en cache des contrôles d’accès</span><span class="sxs-lookup"><span data-stu-id="cc161-112">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="cc161-113">Vérification de l’accès avec l’API auth</span><span class="sxs-lookup"><span data-stu-id="cc161-113">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="cc161-114">Fonctionnement de AccessCheck</span><span class="sxs-lookup"><span data-stu-id="cc161-114">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="cc161-115">Initialisation d’un contexte client</span><span class="sxs-lookup"><span data-stu-id="cc161-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="cc161-116">Langage de définition du descripteur de sécurité pour les ACE conditionnelles</span><span class="sxs-lookup"><span data-stu-id="cc161-116">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



