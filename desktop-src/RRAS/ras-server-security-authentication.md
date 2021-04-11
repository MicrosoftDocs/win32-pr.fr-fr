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
# <a name="ras-server-security-authentication"></a><span data-ttu-id="0bd41-103">Authentification de la sécurité du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="0bd41-103">RAS Server Security Authentication</span></span>

<span data-ttu-id="0bd41-104">Lorsqu’un serveur RAS Windows NT/Windows 2000 reçoit un appel, il appelle la fonction [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) de la dll de sécurité RAS inscrite, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="0bd41-104">When a Windows NT/Windows 2000 RAS server receives a call, it invokes the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) function of the registered RAS security DLL, if there is one.</span></span> <span data-ttu-id="0bd41-105">Cet appel indique à la DLL de sécurité de commencer son authentification de l’utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="0bd41-105">This call notifies the security DLL to begin its authentication of the remote user.</span></span> <span data-ttu-id="0bd41-106">Le serveur RAS appelle **RasSecurityDialogBegin** avant d’effectuer son authentification PPP ou RAS.</span><span class="sxs-lookup"><span data-stu-id="0bd41-106">The RAS server calls **RasSecurityDialogBegin** before performing its PPP or RAS authentication.</span></span>

<span data-ttu-id="0bd41-107">L’appel [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) transmet les informations suivantes à la dll de sécurité :</span><span class="sxs-lookup"><span data-stu-id="0bd41-107">The [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) call passes the following information to the security DLL:</span></span>

-   <span data-ttu-id="0bd41-108">Handle de port pour identifier la connexion.</span><span class="sxs-lookup"><span data-stu-id="0bd41-108">A port handle to identify the connection.</span></span>
-   <span data-ttu-id="0bd41-109">Pointeurs vers les mémoires tampons à utiliser lors de la communication avec l’utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="0bd41-109">Pointers to buffers to use when communicating with the remote user.</span></span>
-   <span data-ttu-id="0bd41-110">Pointeur vers une fonction [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) à appeler lorsque l’authentification est terminée.</span><span class="sxs-lookup"><span data-stu-id="0bd41-110">A pointer to a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) function to call when the authentication has been completed.</span></span>

<span data-ttu-id="0bd41-111">Le handle de port et les pointeurs de mémoire tampon sont valides jusqu’à ce que la DLL de sécurité appelle [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) pour mettre fin à la transaction d’authentification.</span><span class="sxs-lookup"><span data-stu-id="0bd41-111">The port handle and buffer pointers are valid until the security DLL calls [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) to terminate the authentication transaction.</span></span>

<span data-ttu-id="0bd41-112">Le [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) informe le serveur RAS des résultats de l’authentification de la dll de sécurité de l’utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="0bd41-112">The [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifies the RAS server of the results of the security DLL's authentication of the remote user.</span></span> <span data-ttu-id="0bd41-113">Si la DLL de sécurité signale une réussite, le serveur RAS poursuit son authentification PPP et RAS de l’utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="0bd41-113">If the security DLL reports success, the RAS server proceeds with its PPP and RAS authentication of the remote user.</span></span> <span data-ttu-id="0bd41-114">Si la DLL de sécurité signale que l’utilisateur distant a échoué à l’authentification ou qu’une erreur s’est produite, le serveur RAS se bloque et consigne l’erreur ou l’authentification qui a échoué dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="0bd41-114">If the security DLL reports that the remote user failed the authentication, or that an error occurred, the RAS server hangs up and logs the error or failed authentication in the event log.</span></span>

 

 




