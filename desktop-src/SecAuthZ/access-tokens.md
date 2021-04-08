---
description: Un jeton d’accès est un objet qui décrit le contexte de sécurité d’un processus ou d’un thread.
ms.assetid: 350159c9-2399-427a-ba44-c897a9664299
title: Jetons d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993c1f5aebab797ab28e61b36f59507e4d2f1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866002"
---
# <a name="access-tokens"></a>Jetons d’accès

Un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) est un objet qui décrit le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) d’un [*processus*](/windows/desktop/SecGloss/p-gly) ou d’un thread. Les informations contenues dans un jeton incluent l’identité et les privilèges du compte d’utilisateur associé au processus ou au thread. Lorsqu’un utilisateur ouvre une session, le système vérifie le mot de passe de l’utilisateur en le comparant avec les informations stockées dans une base de données de sécurité. Si le mot de passe est [*authentifié*](/windows/desktop/SecGloss/a-gly), le système génère un jeton d’accès. Chaque processus exécuté pour le compte de cet utilisateur dispose d’une copie de ce jeton d’accès.

Le système utilise un jeton d’accès pour identifier l’utilisateur lorsqu’un thread interagit avec un [objet sécurisable](securable-objects.md) ou tente d’exécuter une tâche système qui requiert des privilèges. Les jetons d’accès contiennent les informations suivantes :

-   [Identificateur de sécurité](security-identifiers.md) (SID) pour le compte de l’utilisateur
-   Sid pour les groupes dont l’utilisateur est membre
-   Un [*SID d’ouverture*](/windows/desktop/SecGloss/l-gly) de session qui identifie la [*session d’ouverture de session*](/windows/desktop/SecGloss/l-gly) active
-   Liste des [privilèges](privileges.md) détenus par l’utilisateur ou par les groupes de l’utilisateur
-   Un SID propriétaire
-   SID du groupe principal
-   [DACL](access-control-lists.md) par défaut que le système utilise quand l’utilisateur crée un objet sécurisable sans spécifier de [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)
-   Source du jeton d’accès
-   Si le jeton est un jeton [*principal*](/windows/desktop/SecGloss/p-gly) ou un jeton d' [emprunt d’identité](client-impersonation.md)
-   Liste facultative des [SID de restriction](restricted-tokens.md)
-   Niveaux d’emprunt d’identité actuels
-   Autres statistiques

Chaque processus a un [*jeton principal*](/windows/desktop/SecGloss/p-gly) qui décrit le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) du compte d’utilisateur associé au processus. Par défaut, le système utilise le jeton principal lorsqu’un thread du processus interagit avec un objet sécurisable. En outre, un thread peut emprunter l’identité d’un compte client. L’emprunt d’identité permet au thread d’interagir avec les objets sécurisables à l’aide du contexte de sécurité du client. Un thread qui emprunte l’identité d’un client possède un jeton principal et un [*jeton d’emprunt d’identité*](/windows/desktop/SecGloss/i-gly).

Utilisez la fonction [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) pour récupérer un handle vers le jeton principal d’un processus. Utilisez la fonction [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) pour récupérer un handle pour le jeton d’emprunt d’identité d’un thread. Pour plus d’informations, consultez [emprunt d’identité](client-impersonation.md).

Vous pouvez utiliser les fonctions suivantes pour manipuler des jetons d’accès.



| Fonction                                               | Description                                                                                                                                                            |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustTokenGroups**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups)         | Modifie les informations de groupe dans un jeton d’accès.                                                                                                                      |
| [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) | Active ou désactive les privilèges dans un jeton d’accès. Elle n’accorde pas de nouveaux privilèges ou révoque des privilèges existants.                                                       |
| [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership)   | Détermine si un SID spécifié est activé dans un jeton d’accès spécifié.                                                                                             |
| [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) | Crée un nouveau jeton qui est une version limitée d’un jeton existant. Le jeton restreint peut avoir des SID désactivés, des privilèges supprimés et une liste de sid restreints. |
| [**DuplicateToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken)               | Crée un nouveau jeton d’emprunt d’identité qui duplique un jeton existant.                                                                                                   |
| [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)           | Crée un jeton principal ou un jeton d’emprunt d’identité qui duplique un jeton existant.                                                                                  |
| [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)     | Récupère des informations sur un jeton.                                                                                                                                   |
| [**IsTokenRestricted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-istokenrestricted)         | Détermine si un jeton a une liste de SID de restriction.                                                                                                             |
| [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)           | Récupère un handle vers le jeton d’accès principal pour un processus.                                                                                                          |
| [**OpenThreadToken,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)             | Récupère un handle pour le jeton d’accès d’emprunt d’identité pour un thread.                                                                                                     |
| [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken)               | Assigne ou supprime un jeton d’emprunt d’identité pour un thread.                                                                                                                |
| [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation)     | Modifie le propriétaire, le groupe principal ou la liste DACL par défaut d’un jeton.                                                                                                               |



 

Les fonctions de jeton d’accès utilisent les structures suivantes pour décrire les parties d’un jeton d’accès.



| Structure                                            | Description                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**\_contrôle Token**](/windows/desktop/api/Winnt/ns-winnt-token_control)              | Informations qui identifient un jeton d’accès.                                                          |
| [**\_DACL par défaut du jeton \_**](/windows/desktop/api/Winnt/ns-winnt-token_default_dacl)   | DACL par défaut que le système utilise dans les descripteurs de sécurité des nouveaux objets créés par un thread. |
| [**groupes de jetons \_**](/windows/desktop/api/Winnt/ns-winnt-token_groups)                | Spécifie les SID et les attributs des SID de groupe dans un jeton d’accès.                               |
| [**propriétaire du jeton \_**](/windows/desktop/api/Winnt/ns-winnt-token_owner)                  | SID de propriétaire par défaut pour les descripteurs de sécurité de nouveaux objets.                                    |
| [**\_groupe principal de jetons \_**](/windows/desktop/api/Winnt/ns-winnt-token_primary_group) | SID de groupe principal par défaut pour les descripteurs de sécurité de nouveaux objets.                            |
| [**privilèges de jeton \_**](/windows/desktop/api/Winnt/ns-winnt-token_privileges)        | Privilèges associés à un jeton d’accès. Détermine également si les privilèges sont activés.   |
| [**SOURCE du jeton \_**](/windows/desktop/api/Winnt/ns-winnt-token_source)                | Source d’un jeton d’accès.                                                                        |
| [**statistiques des jetons \_**](/windows/desktop/api/Winnt/ns-winnt-token_statistics)        | Statistiques associées à un jeton d’accès.                                                           |
| [**utilisateur du jeton \_**](/windows/desktop/api/Winnt/ns-winnt-token_user)                    | SID de l’utilisateur associé à un jeton d’accès.                                                  |



 

Les fonctions de jeton d’accès utilisent les types d’énumération suivants.



| Type d'énumération                                             | Spécifie                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_classe d’informations de jeton \_**](/windows/desktop/api/Winnt/ne-winnt-token_information_class) | Identifie le type d’informations qui est défini ou récupéré à partir d’un jeton d’accès. |
| [**TYPE de jeton \_**](/windows/desktop/api/Winnt/ne-winnt-token_type)                            | Identifie un jeton d’accès en tant que jeton principal ou d’emprunt d’identité.                 |



 

 

 
