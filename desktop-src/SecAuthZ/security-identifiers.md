---
description: Un identificateur de sécurité (SID) est une valeur unique de longueur variable utilisée pour identifier un tiers de confiance.
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: Identificateurs de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368b2484cd8766aa7fa74c24679e82b10854e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517312"
---
# <a name="security-identifiers"></a>Identificateurs de sécurité

Un [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) est une valeur unique de longueur variable utilisée pour identifier un [tiers de confiance](trustees.md). Chaque compte possède un SID unique émis par une autorité, par exemple un contrôleur de domaine Windows, et stocké dans une base de données de sécurité. Chaque fois qu’un utilisateur ouvre une session, le système récupère le SID de cet utilisateur dans la base de données et le place dans le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) de cet utilisateur. Le système utilise le SID dans le jeton d’accès pour identifier l’utilisateur dans toutes les interactions suivantes avec la sécurité Windows. Lorsqu’un SID a été utilisé en tant qu’identificateur unique pour un utilisateur ou un groupe, il ne peut jamais être utilisé pour identifier un autre utilisateur ou groupe.

La sécurité Windows utilise des SID dans les éléments de sécurité suivants :

-   Dans les [descripteurs de sécurité](security-descriptors.md) pour identifier le propriétaire d’un objet et d’un groupe principal
-   Dans les [entrées de contrôle d’accès](access-control-entries.md), pour identifier le tiers de confiance pour lequel l’accès est autorisé, refusé ou audité
-   Dans les [jetons d’accès](access-tokens.md), pour identifier l’utilisateur et les groupes auxquels l’utilisateur appartient

Outre les SID spécifiques à un domaine qui sont créés de manière unique et attribués à des utilisateurs et des groupes spécifiques, des [sid connus](well-known-sids.md) identifient des groupes génériques et des utilisateurs génériques. Par exemple, les SID bien connus, tout le monde et tout le monde, identifient un groupe qui comprend tous les utilisateurs.

La plupart des applications n’ont jamais besoin d’utiliser des SID. Étant donné que les noms de [sid connus](well-known-sids.md) peuvent varier, vous devez utiliser les fonctions pour générer le SID à partir de constantes prédéfinies plutôt que d’utiliser le nom du SID connu. Par exemple, la version anglaise (États-Unis) du système d’exploitation Windows possède un SID connu nommé « \\ administrateurs builtin » qui peut avoir un nom différent sur les versions internationales du système. Pour obtenir un exemple qui crée un SID bien connu, consultez [recherche d’un SID dans un jeton d’accès en C++](searching-for-a-sid-in-an-access-token-in-c--.md).

Si vous devez utiliser des SID, ne les manipulez pas directement. Au lieu de cela, utilisez les fonctions suivantes.



| Fonction                                                       | Description                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | Alloue et initialise un SID avec le nombre spécifié de sous-autorités.                                                                              |
| [**ConvertSidToStringSid a**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | Convertit un SID en un format de chaîne approprié pour l’affichage, le stockage ou le transport.                                                                            |
| [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | Convertit un SID au format chaîne en un SID fonctionnel valide.                                                                                                  |
| [**Copysid a**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | Copie un SID source dans une mémoire tampon.                                                                                                                          |
| [**EqualPrefixSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | Teste l’égalité de deux valeurs de préfixe SID. Un préfixe SID est le SID entier, à l’exception de la dernière valeur de sous-autorité.                                          |
| [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | Teste l’égalité de deux sid. Ils doivent correspondre exactement pour être considérés comme égaux.                                                                              |
| [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | Libère un SID précédemment alloué à l’aide de la fonction [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .                                      |
| [**GetLengthSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | Récupère la longueur d’un SID.                                                                                                                            |
| [**GetSidIdentifierAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | Récupère un pointeur vers l’autorité d’identificateur pour un SID.                                                                                                |
| [**GetSidLengthRequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | Récupère la taille de la mémoire tampon requise pour stocker un SID avec un nombre spécifié de sous-autorités.                                                       |
| [**GetSidSubAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | Récupère un pointeur vers une sous-autorité spécifiée dans un SID.                                                                                                 |
| [**GetSidSubAuthorityCount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | Récupère le nombre de sous-autorités dans un SID.                                                                                                          |
| [**InitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | Initialise une structure [**sid**](/windows/desktop/api/Winnt/ns-winnt-sid) .                                                                                                               |
| [**IsValidSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | Teste la validité d’un SID en vérifiant que le numéro de révision se trouve dans une plage connue et que le nombre de sous-autorités est inférieur au maximum. |
| [**LookupAccountName**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | Récupère le SID qui correspond à un nom de compte spécifié.                                                                                           |
| [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | Récupère le nom du compte qui correspond à un SID spécifié.                                                                                           |



 

 

 
