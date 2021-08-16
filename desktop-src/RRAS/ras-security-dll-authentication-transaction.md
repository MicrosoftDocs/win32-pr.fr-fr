---
title: Transaction d’authentification de la DLL de sécurité RAS
description: Windows le serveur RAS NT/Windows 2000 appelle la fonction RasSecurityDialogBegin de la DLL de sécurité pour commencer l’authentification d’un utilisateur distant.
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea463c56d96cad13fb55a2b6e0bbdfc154518ba012e4c71c6ab8bdd3213cd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789475"
---
# <a name="ras-security-dll-authentication-transaction"></a>Transaction d’authentification de la DLL de sécurité RAS

Windows le serveur RAS NT/Windows 2000 appelle la fonction [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) de la DLL de sécurité pour commencer l’authentification d’un utilisateur distant. Le serveur RAS est bloqué et ne peut accepter aucun autre appel tant que **RasSecurityDialogBegin** n’est pas retourné. Pour cette raison, **RasSecurityDialogBegin** doit copier les paramètres d’entrée, créer un thread pour effectuer l’authentification et retourner le plus rapidement possible.

Le thread créé par la DLL de sécurité utilise les fonctions [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) et [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) pour communiquer avec l’ordinateur distant. Ces fonctions ne sont pas disponibles pour une importation statique à partir d’une bibliothèque. Au lieu de cela, la DLL de sécurité doit utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à ces fonctions dans RASMAN.DLL.

Pendant une transaction d’authentification, le gestionnaire de connexions RAS sur l’ordinateur distant affiche une fenêtre de terminal. Le thread de la DLL de sécurité appelle [**RasSecurityDialogSend**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) pour envoyer un message à afficher dans la fenêtre de terminal. Le thread appelle ensuite [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) pour recevoir l’entrée que l’utilisateur distant tape dans la fenêtre de terminal. Le thread peut effectuer un nombre quelconque d’appels **RasSecurityDialogSend** , avec chaque appel suivi d’un appel **RasSecurityDialogReceive** . Après chaque appel à **RasSecurityDialogReceive**, le thread doit appeler l’une des fonctions d’attente, telles que [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), pour attendre que les opérations d’envoi et de réception asynchrones soient terminées. Le serveur RAS signale un objet d’événement lorsque l’opération de réception est terminée ou lorsqu’un délai d’attente facultatif s’est écoulé.

Lorsque le thread a terminé l’authentification de l’utilisateur distant, il appelle la fonction [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) . Cet appel passe une structure de [**\_ message de sécurité**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) contenant les résultats de la transaction d’authentification au serveur RAS. Le serveur RAS effectue ensuite une séquence de nettoyage qui comprend un appel à la fonction [**RasSecurityDialogEnd**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) de la dll. Cela donne à la DLL de sécurité la possibilité d’effectuer tout nettoyage nécessaire.

La DLL de sécurité peut appeler la fonction [**RasSecurityDialogGetInfo**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) pour récupérer des informations sur le port associé à une transaction d’authentification. **RasSecurityDialogGetInfo** remplit une structure d' [**\_ \_ informations de sécurité RAS**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info) qui indique l’état du dernier appel [**RasSecurityDialogReceive**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) pour le port.

 

 