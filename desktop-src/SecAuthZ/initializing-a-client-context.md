---
description: Une application doit créer un contexte client pour pouvoir utiliser l’API auth pour effectuer des vérifications d’accès ou un audit.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Initialisation d’un contexte client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da8a3c3191f323cf6ce35fda90f4bd75299dac67183986998cf21a80c0ee6995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908039"
---
# <a name="initializing-a-client-context"></a>Initialisation d’un contexte client

Une application doit créer un contexte client pour pouvoir utiliser l’API auth pour effectuer des vérifications d’accès ou un audit.

Une application doit appeler la fonction [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) pour initialiser le gestionnaire de ressources. L’application peut ensuite appeler l’une des fonctions suivantes pour créer un contexte client. En outre, si vous effectuez des vérifications d’accès ou un audit à distance, vous devez utiliser la fonction [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .

Pour créer un contexte client basé sur un contexte client existant, appelez la fonction [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .

La fonction [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) crée un nouveau contexte client à l’aide des informations contenues dans un jeton d’ouverture de session. La fonction [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) crée un nouveau contexte client à l’aide du [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid)spécifié.

Si possible, appelez la fonction [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) à la place de [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid). **AuthzInitializeContextFromSid** tente de récupérer les informations disponibles dans un jeton d’ouverture de session si le client est actuellement connecté. Un jeton d’ouverture de session réel fournit plus d’informations, telles que le type de connexion et les propriétés de connexion, et reflète le comportement du package d’authentification utilisé pour l’ouverture de session. Le contexte client créé par **AuthzInitializeContextFromToken** utilise un jeton d’ouverture de session et le contexte client résultant est plus complet et précis qu’un contexte client créé par **AuthzInitializeContextFromSid**.

> [!Note]  
> Les variables d’attribut de sécurité doivent être présentes dans le contexte client si elles sont référencées dans une expression conditionnelle ; dans le cas contraire, le terme des expressions conditionnelles qui les référencera sera évalué comme inconnu. Pour plus d’informations sur les expressions conditionnelles, consultez la rubrique [langage de définition du descripteur de sécurité pour les ACE conditionnel](security-descriptor-definition-language-for-conditional-aces-.md) .

 

## <a name="example"></a>Exemple

L’exemple suivant initialise le gestionnaire de ressources authz et appelle la fonction [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) pour créer un contexte client à partir du jeton d’ouverture de session associé au processus en cours.


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

[Interrogation d’un contexte client](querying-a-client-context.md)
</dt> <dt>

[Langage de définition du descripteur de sécurité pour les ACE conditionnelles](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



