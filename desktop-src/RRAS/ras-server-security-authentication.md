---
title: Authentification de la sécurité du serveur RAS
description: Lorsqu’un serveur RAS Windows NT/Windows 2000 reçoit un appel, il appelle la fonction RasSecurityDialogBegin de la DLL de sécurité RAS inscrite, le cas échéant.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029118"
---
# <a name="ras-server-security-authentication"></a>Authentification de la sécurité du serveur RAS

Lorsqu’un serveur RAS Windows NT/Windows 2000 reçoit un appel, il appelle la fonction [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) de la dll de sécurité RAS inscrite, le cas échéant. Cet appel indique à la DLL de sécurité de commencer son authentification de l’utilisateur distant. Le serveur RAS appelle **RasSecurityDialogBegin** avant d’effectuer son authentification PPP ou RAS.

L’appel [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) transmet les informations suivantes à la dll de sécurité :

-   Handle de port pour identifier la connexion.
-   Pointeurs vers les mémoires tampons à utiliser lors de la communication avec l’utilisateur distant.
-   Pointeur vers une fonction [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) à appeler lorsque l’authentification est terminée.

Le handle de port et les pointeurs de mémoire tampon sont valides jusqu’à ce que la DLL de sécurité appelle [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) pour mettre fin à la transaction d’authentification.

Le [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) informe le serveur RAS des résultats de l’authentification de la dll de sécurité de l’utilisateur distant. Si la DLL de sécurité signale une réussite, le serveur RAS poursuit son authentification PPP et RAS de l’utilisateur distant. Si la DLL de sécurité signale que l’utilisateur distant a échoué à l’authentification ou qu’une erreur s’est produite, le serveur RAS se bloque et consigne l’erreur ou l’authentification qui a échoué dans le journal des événements.

 

 




