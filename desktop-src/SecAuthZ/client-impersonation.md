---
description: L’emprunt d’identité est la capacité d’un thread à s’exécuter en utilisant des informations de sécurité différentes de celles du processus propriétaire du thread.
ms.assetid: a3f74372-bdc9-43eb-b72f-7d00a43e78a8
title: Emprunt d’identité du client (autorisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 454e943b53cffbc4430c71b31e2b172095b999e2201c4cafc08b081bf1782e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783065"
---
# <a name="client-impersonation-authorization"></a>Emprunt d’identité du client (autorisation)

L' [*emprunt d’identité*](/windows/desktop/SecGloss/i-gly) est la capacité d’un thread à s’exécuter en utilisant des informations de sécurité différentes de celles du processus propriétaire du thread. En règle générale, un thread dans une application serveur emprunte l’identité d’un client. Cela permet au thread de serveur d’agir au nom de ce client pour accéder aux objets sur le serveur ou valider l’accès aux propres objets du client.

l’API Microsoft Windows fournit les fonctions suivantes pour commencer un emprunt d’identité :

-   Une application de serveur DDE peut appeler la fonction [**DdeImpersonateClient**](/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient) pour emprunter l’identité d’un client.
-   Un serveur de canaux nommés peut appeler la fonction [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) .
-   Vous pouvez appeler la fonction [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) pour emprunter l’identité du contexte de sécurité du [*jeton d’accès*](/windows/desktop/SecGloss/a-gly)d’un utilisateur connecté.
-   La fonction [**ImpersonateSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateself) permet à un thread de générer une copie de son propre jeton d’accès. Cela est utile quand une application doit modifier le contexte de sécurité d’un thread unique. Par exemple, un seul thread d’un processus doit parfois activer un [*privilège*](/windows/desktop/SecGloss/p-gly).
-   Vous pouvez appeler la fonction [**SetThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadtoken) pour faire en sorte que le thread cible s’exécute dans le contexte de sécurité d’un [*jeton d’emprunt d’identité*](/windows/desktop/SecGloss/i-gly)spécifié.
-   Une application serveur d’appel de procédure distante (RPC) Microsoft peut appeler la fonction [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) pour emprunter l’identité d’un client.
-   Un [*package de sécurité*](/windows/desktop/SecGloss/s-gly) ou un serveur d’applications peut appeler la fonction [**ImpersonateSecurityContext**](/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext) pour emprunter l’identité d’un client.

Pour la plupart de ces emprunts d’identité, le thread d’emprunt d’identité peut revenir à son propre contexte de sécurité en appelant la fonction [**RevertToSelf**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) . L’exception est l’emprunt d’identité RPC, dans lequel l’application serveur RPC appelle [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) ou [**RpcRevertToSelfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex) pour rétablir son propre contexte de sécurité.

 

 
