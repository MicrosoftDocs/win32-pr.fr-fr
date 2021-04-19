---
description: Une application serveur peut appeler la fonction CreateProcessAsUser pour créer un nouveau processus qui s’exécute dans un contexte de sécurité clients.
ms.assetid: bd416109-fe76-4d55-bc63-3ebbcf32b92a
title: Processus dans le contexte de sécurité du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c9bafb576bd0d195ae762c69be885ac32f1071
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529686"
---
# <a name="processes-in-the-client-security-context"></a>Processus dans le contexte de sécurité du client

Une application serveur peut appeler la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) pour créer un nouveau processus qui s’exécute dans le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly)d’un client. Lorsqu’elle est appelée avec un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly)client, **CreateProcessAsUser** requiert le \_ nom du ASSIGNPRIMARYTOKEN se et les privilèges d' \_ \_ augmentation \_ des noms de quotas \_ , qui sont conservés par les services Windows exécutés dans le [compte LocalSystem](/windows/desktop/Services/localsystem-account).

La fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) requiert également un [*jeton d’accès principal*](/windows/desktop/SecGloss/p-gly). Un serveur peut obtenir un jeton d’accès principal pour un client en [démarrant une session de connexion](client-logon-sessions.md) pour le client ou en [usurpant l’identité du client](client-impersonation.md) et en dupliquant le [*jeton d’emprunt d’identité*](/windows/desktop/SecGloss/i-gly).

Les procédures suivantes décrivent deux façons de créer un processus client.

**Pour créer un processus client en ouvrant une session sur le client**

1.  Consignez le client sur l’ordinateur local à l’aide des [*informations d’identification*](/windows/desktop/SecGloss/c-gly) du client dans un appel à [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera). **LogonUser** produit un jeton principal pour la session de [*connexion*](/windows/desktop/SecGloss/l-gly)du client.
2.  Si le serveur doit utiliser le contexte de sécurité du client, accédez au fichier exécutable du [*processus*](/windows/desktop/SecGloss/p-gly) client à l’aide du jeton principal dans un appel à la fonction [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .
3.  Créez un processus dans le contexte de sécurité du client à l’aide du jeton principal dans un appel à [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera).

> [!Note]  
> Un processus créé à l’aide de la technique suivante peut ne pas être en mesure d’accéder aux ressources réseau, sauf s’il dispose des [*informations d’identification*](/windows/desktop/SecGloss/c-gly)du client.

 

**Pour créer un processus client en empruntant l’identité du client**

1.  Démarrez l’emprunt d’identité à l’aide d’une fonction d’emprunt d’identité, telle que [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient).
2.  Appelez la fonction [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) pour récupérer un jeton d’emprunt d’identité qui a le contexte de sécurité du client.
3.  Appelez la fonction [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) pour convertir le jeton d’emprunt d’identité en jeton principal.
4.  Utilisez le jeton principal dans un appel à la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) pour créer un processus dans le contexte de sécurité du client.

Par défaut, [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) crée le [*processus*](/windows/desktop/SecGloss/p-gly) client sur un poste de travail et une station Windows non interactive. Pour créer un processus interactif, le serveur doit d’abord définir les listes de contrôle d’accès discrétionnaire (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) de la station et du bureau interactif pour s’assurer que le client est autorisé à y accéder. Pour ce faire, la meilleure méthode consiste à enregistrer le client sur, à [récupérer l’identificateur de sécurité (SID) de la session de connexion du client](/previous-versions//aa446670(v=vs.85)), puis à utiliser ce SID dans les ACE access-allowed sur le poste de travail et la station de fenêtre interactive. Le serveur peut ensuite appeler **CreateProcessAsUser**, en spécifiant la station de fenêtre interactive et le winsta0 de bureau \\ par défaut. Pour obtenir un exemple qui illustre cette procédure, consultez [démarrage d’un processus client interactif en C++](/previous-versions//aa379608(v=vs.85)).

 

 
