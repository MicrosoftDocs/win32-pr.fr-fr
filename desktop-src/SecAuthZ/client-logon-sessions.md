---
description: un serveur doté du \_ privilège SE TCB \_ NAME, tel qu’un service Windows s’exécutant dans le compte LocalSystem, peut appeler la fonction LogonUser pour authentifier un client sur l’ordinateur sur lequel le serveur s’exécute.
ms.assetid: 27328497-8f04-42e8-aadd-4c33b9907b94
title: Sessions d’ouverture de session client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baafdc46800cc5b334a5496be5502b97e18d4702bdf9b839d8431a92110c3d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783021"
---
# <a name="client-logon-sessions"></a>Sessions d’ouverture de session client

un serveur doté du \_ privilège SE TCB \_ NAME, tel qu’un service Windows s’exécutant dans le [compte LocalSystem](/windows/desktop/Services/localsystem-account), peut appeler la fonction [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) pour [*authentifier*](/windows/desktop/SecGloss/a-gly) un client sur l’ordinateur sur lequel le serveur s’exécute. La fonction **LogonUser** démarre une nouvelle [*session*](/windows/desktop/SecGloss/s-gly) de connexion et retourne un [*jeton d’accès principal*](/windows/desktop/SecGloss/p-gly) qui contient les informations de sécurité du client. Vous pouvez utiliser ce jeton principal lors de l’appel de la fonction [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) pour emprunter l’identité du client ou lors de l’appel de la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) pour créer un processus qui s’exécute dans le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) du client.

L’avantage de l’authentification du client de cette façon est que le serveur qui emprunte l’identité du client authentifié, ou un [*processus*](/windows/desktop/SecGloss/p-gly) créé dans le contexte du client authentifié, peut se connecter aux ressources réseau distantes en tant que client. Si cette authentification n’est pas effectuée, le serveur peut se connecter aux ressources réseau uniquement s’il a acquis le nom de compte et le mot de passe du client à transmettre à la fonction [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) .

L’inconvénient de l’authentification du client de cette façon est que le serveur doit avoir acquis les [*informations d’identification*](/windows/desktop/SecGloss/c-gly) du client (nom de domaine, nom d’utilisateur et mot de passe). Si un client distant fournit ces informations d’identification au serveur, il incombe au client et au serveur de s’assurer que les informations d’identification sont transmises de manière sécurisée.

 

 
