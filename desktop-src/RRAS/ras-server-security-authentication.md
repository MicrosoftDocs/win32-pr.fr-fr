---
title: Authentification de la sécurité du serveur RAS
description: lorsqu’un serveur ras Windows NT/Windows 2000 reçoit un appel, il appelle la fonction RasSecurityDialogBegin de la DLL de sécurité ras inscrite, le cas échéant.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532bda51d6e9ee0ea90c900fa974827e1840e7e633caf48fbadec5fe6a701a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028739"
---
# <a name="ras-server-security-authentication"></a>Authentification de la sécurité du serveur RAS

lorsqu’un serveur ras Windows NT/Windows 2000 reçoit un appel, il appelle la fonction [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) de la DLL de sécurité ras inscrite, le cas échéant. Cet appel indique à la DLL de sécurité de commencer son authentification de l’utilisateur distant. Le serveur RAS appelle **RasSecurityDialogBegin** avant d’effectuer son authentification PPP ou RAS.

L’appel [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) transmet les informations suivantes à la dll de sécurité :

-   Handle de port pour identifier la connexion.
-   Pointeurs vers les mémoires tampons à utiliser lors de la communication avec l’utilisateur distant.
-   Pointeur vers une fonction [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) à appeler lorsque l’authentification est terminée.

Le handle de port et les pointeurs de mémoire tampon sont valides jusqu’à ce que la DLL de sécurité appelle [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) pour mettre fin à la transaction d’authentification.

Le [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) informe le serveur RAS des résultats de l’authentification de la dll de sécurité de l’utilisateur distant. Si la DLL de sécurité signale une réussite, le serveur RAS poursuit son authentification PPP et RAS de l’utilisateur distant. Si la DLL de sécurité signale que l’utilisateur distant a échoué à l’authentification ou qu’une erreur s’est produite, le serveur RAS se bloque et consigne l’erreur ou l’authentification qui a échoué dans le journal des événements.

 

 




