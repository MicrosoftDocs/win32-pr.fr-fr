---
title: Snego
description: Snego, dont l’identificateur de service d’authentification est RPC \_ C \_ Authn \_ GSS \_ Negotiate, ne fournit pas réellement de services d’authentification.
ms.assetid: 2087a84c-d302-4511-9f02-2d20ee9e0d8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676b6428d6b7e79893214c2d234dcfc43992e190
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363591"
---
# <a name="snego"></a>Snego

Snego, dont l’identificateur de service d’authentification est RPC \_ C \_ Authn \_ GSS \_ Negotiate, ne fournit pas réellement de services d’authentification. Au lieu de cela, il prend une liste de services d’authentification et négocie un service qui fonctionnera entre le client et le serveur. Les paramètres d’authentification ne sont pas utilisés par Snego mais sont transmis au service d’authentification choisi, qui effectue l’authentification réelle. Snego a été normalisé par l’IETF (Internet Engineering Task Force) en décembre 1998, dans le document [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt).

Snego est utile lorsque vous ne connaissez pas les services d’authentification que l’ordinateur distant peut fournir.

Pour utiliser Snego, le client et le serveur doivent spécifier Snego comme service d’authentification. Le serveur spécifie \_ RPC \_ \_ \_ Authentication GSS Negotiate en tant que membre **dwAuthnSvc** de l’une des structures de [**\_ \_ service d’authentification unique**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) dans le paramètre de tableau *asAuthSvc* qui est passé à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Le client peut spécifier Snego en appelant [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) et en passant RPC \_ C \_ Authn \_ GSS \_ Negotiate comme paramètre *dwAuthnSvc* . Le client doit également fournir une liste de services d’authentification possibles pour Snego via le membre **PackageList** de la structure de l’identité d’authentification [**\_ winnt winnt \_ \_ \_**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa) qui est transmise au paramètre *pAuthInfo* dans l’appel à **CoSetProxyBlanket**. Si *pAuthInfo* a la **valeur null**, Snego compose une liste de services d’authentification à partir des packages de sécurité installés sur l’ordinateur. Ensuite, Snego envoie la liste des services d’authentification au serveur, compare la liste aux services d’authentification disponibles du serveur et choisit un service d’authentification à utiliser pour la connexion.

> [!Note]  
> Schannel ne peut pas figurer dans la liste des services d’authentification utilisés par Snego.

 

Les clients peuvent également spécifier Snego lorsqu’ils appellent [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Les paramètres *dwAuthnSvc* et *pAuthInfo* de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) deviennent membres d’une structure d' [**\_ \_ informations d’authentification unique**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) qui est transmise à **CoInitializeSecurity** via son paramètre *pAuthList* . Les détails des valeurs de ces membres sont les mêmes que ceux décrits dans le paragraphe précédent.

Si Snego est utilisé, les appels à [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) ou [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) retournent Snego en tant que service d’authentification, plutôt que le service d’authentification réel qui Snego choisi pour établir la connexion.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Packages COM et de sécurité](com-and-security-packages.md)
</dt> </dl>

 

 