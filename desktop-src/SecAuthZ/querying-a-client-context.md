---
description: Les applications peuvent appeler la fonction AuthzGetInformationFromContext pour demander des informations sur un contexte client existant.
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: Interrogation d’un contexte client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e944939baae45236c914da7d11b6cedd6623ea132363ec86e1bf6f340644ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912078"
---
# <a name="querying-a-client-context"></a>Interrogation d’un contexte client

Les applications peuvent appeler la fonction [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) pour demander des informations sur un contexte client existant.

Le paramètre *InfoClass* de la fonction [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) accepte une valeur de l’énumération de [**\_ \_ \_ classe d’informations de contexte auth**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) qui spécifie le type d’informations que la fonction interroge.

Les variables d’attribut de sécurité doivent être présentes dans le contexte client si elles sont référencées dans une expression conditionnelle ; dans le cas contraire, le terme des expressions conditionnelles qui les référencera sera évalué comme inconnu. Pour plus d’informations sur les expressions conditionnelles, consultez la rubrique [langage de définition du descripteur de sécurité pour les ACE conditionnel](security-descriptor-definition-language-for-conditional-aces-.md) .

## <a name="example"></a>Exemple

L’exemple suivant interroge le contexte client créé dans l’exemple à partir de l' [initialisation d’un contexte client](initializing-a-client-context.md) pour récupérer la liste des [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) des groupes associés à ce contexte client.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ajout de sid à un contexte client](adding-sids-to-a-client-context.md)
</dt> <dt>

[Mise en cache des contrôles d’accès](caching-access-checks.md)
</dt> <dt>

[Vérification de l’accès avec l’API auth](checking-access-with-authz-api.md)
</dt> <dt>

[Fonctionnement de AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[Initialisation d’un contexte client](initializing-a-client-context.md)
</dt> <dt>

[Langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



