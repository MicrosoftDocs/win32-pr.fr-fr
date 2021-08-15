---
description: L' \_ énumération de niveau d’emprunt d’identité de sécurité \_ définit quatre niveaux d’emprunt d’identité qui déterminent les opérations qu’un serveur peut effectuer dans le contexte des clients.
ms.assetid: ae152dbf-44f0-417f-a85e-09bf60dcfcb0
title: Niveaux d’emprunt d’identité (autorisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf80f4f6b84499a94659c137c629d66a041752e5171cb3fa7220506586f36e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414589"
---
# <a name="impersonation-levels-authorization"></a>Niveaux d’emprunt d’identité (autorisation)

L’énumération de [**\_ \_ niveau d’emprunt d’identité de sécurité**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level) définit quatre niveaux d’emprunt d’identité qui déterminent les opérations qu’un serveur peut effectuer dans le contexte du client.



| Niveau d'emprunt d'identité    | Description                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| SecurityAnonymous      | Le serveur ne peut pas emprunter l’identité ou identifier le client.                                            |
| SecurityIdentification | Le serveur peut accéder à l’identité et aux privilèges du client, mais ne peut pas emprunter l’identité du client. |
| SecurityImpersonation  | Le serveur peut emprunter l’identité du contexte de sécurité du client sur le système local.                    |
| SecurityDelegation     | Le serveur peut emprunter l’identité du contexte de sécurité du client sur les systèmes distants.                      |



 

Le client d’un canal nommé, d’un RPC ou d’une connexion DDE peut contrôler le niveau d’emprunt d’identité. Par exemple, un client de canal nommé peut appeler la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un handle vers un canal nommé et spécifier le niveau d’emprunt d’identité du serveur.

Lorsque le canal nommé, le RPC ou la connexion DDE est distant, les indicateurs passés à [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour définir le niveau d’emprunt d’identité sont ignorés. Dans ce cas, le niveau d’emprunt d’identité du client est déterminé par les niveaux d’emprunt d’identité activés par le serveur, qui est défini par un indicateur sur le compte du serveur dans le service d’annuaire. Par exemple, si le serveur est activé pour la délégation, le niveau d’emprunt d’identité du client est également défini sur délégation même si les indicateurs passés à **CreateFile** spécifient le niveau d’emprunt d’identité d’identification.

Les clients DDE utilisent la fonction [**DdeSetQualityOfService**](/windows/win32/api/dde/nf-dde-ddesetqualityofservice) avec [**la \_ qualité de la sécurité de la structure \_ de \_ service**](/windows/desktop/api/Winnt/ns-winnt-security_quality_of_service) pour spécifier le niveau d’emprunt d’identité. Le niveau SecurityImpersonation est la valeur par défaut pour les serveurs de canal nommé, RPC et DDE. Les fonctions [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself), [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)et [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) permettent à l’appelant de spécifier un niveau d’emprunt d’identité. Utilisez la fonction [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) pour récupérer le niveau d’emprunt d’identité d’un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly).

Au niveau SecurityImpersonation, la plupart des actions du thread se produisent dans le contexte de sécurité du jeton d' [*emprunt d’identité*](/windows/desktop/SecGloss/i-gly) du thread plutôt que dans le [*jeton principal*](/windows/desktop/SecGloss/p-gly) du [*processus*](/windows/desktop/SecGloss/p-gly) qui possède le thread. Par exemple, si un thread d’emprunt d’identité ouvre un [objet sécurisable](securable-objects.md), le système utilise le jeton d’emprunt d’identité pour vérifier l’accès du thread. De même, si un thread d’emprunt d’identité crée un nouvel objet, par exemple en appelant la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , le propriétaire du nouvel objet est le propriétaire par défaut du [*jeton d’accès*](/windows/desktop/SecGloss/a-gly)du client.

Toutefois, le système utilise le jeton principal du processus plutôt que le jeton d’emprunt d’identité du thread appelant dans les cas suivants :

-   Si un thread d’emprunt d’identité appelle la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) , le nouveau processus hérite toujours du jeton principal du processus.
-   pour les fonctions qui nécessitent le \_ privilège SE TCB \_ NAME, comme la fonction [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) , le système recherche toujours le privilège dans le jeton principal du processus.
-   pour les fonctions qui nécessitent le \_ privilège SE nom d’AUDIT \_ , tel que la fonction [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) , le système recherche toujours le privilège dans le jeton principal du processus.
-   Dans un appel à la fonction [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) , un thread peut spécifier si la fonction utilise le jeton d’emprunt d’identité ou le jeton principal pour déterminer s’il faut accorder l’accès demandé.

 

 
