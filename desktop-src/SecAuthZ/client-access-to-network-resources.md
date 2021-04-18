---
description: Explique les stratégies d’accès aux ressources réseau.
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: Accès client aux ressources réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0873a10c708f9aab2e9c250375a63e8a2167873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516066"
---
# <a name="client-access-to-network-resources"></a>Accès client aux ressources réseau

Un serveur peut utiliser les stratégies suivantes pour accéder aux ressources réseau :

-   Si le serveur a le nom de compte et le mot de passe d’un client, il peut appeler [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) avec les [*informations d’identification*](/windows/desktop/SecGloss/c-gly) du client pour mapper une lettre de lecteur local à un partage réseau.
-   Après avoir appelé [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) avec les informations d’identification du client, le serveur peut appeler la fonction [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) pour [créer un processus pour le client](processes-in-the-client-security-context.md). Ce nouveau processus client peut accéder aux ressources réseau à l’aide du [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly)du client. Par exemple, le processus peut appeler la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un fichier sur un ordinateur distant. Le système utilise le [*jeton principal*](/windows/desktop/SecGloss/p-gly) du client pour vérifier les tentatives d’accès par le processus client.
-   Un serveur peut appeler [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) avec des informations d’identification null pour établir une connexion à une ressource réseau avec un accès au serveur ou une connexion par défaut. Si le serveur s’exécute en tant que compte LocalSystem, il s’authentifie auprès de la ressource réseau dans le [*contexte de sécurité*](/windows/desktop/SecGloss/s-gly) du serveur de domaine. Si le serveur s’exécute sous un compte de service, il s’authentifie en tant que ce compte. Pour plus d’informations, consultez le [compte LocalSystem](/windows/desktop/Services/localsystem-account).

Pour plus d’informations sur la protection des mots de passe, consultez [gestion des mots de passe](/windows/desktop/SecBP/handling-passwords). Pour plus d’informations sur l’acquisition des informations d’identification, consultez [demande d’informations d’identification à l’utilisateur](/windows/desktop/SecBP/asking-the-user-for-credentials).

 

 
