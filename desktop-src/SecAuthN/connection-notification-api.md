---
description: Le routeur multifournisseur (MPR) appelle les fonctions de notification de connexion lorsqu’il se connecte ou déconnecte une ressource réseau. Pour recevoir ces notifications, vous pouvez implémenter ces fonctions dans une DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: API de notification de connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352d5cb09923a666e3fe1474e9fd2ebe033f05be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114942"
---
# <a name="connection-notification-api"></a><span data-ttu-id="34f5b-104">API de notification de connexion</span><span class="sxs-lookup"><span data-stu-id="34f5b-104">Connection Notification API</span></span>

<span data-ttu-id="34f5b-105">Le [*routeur multifournisseur*](/windows/desktop/SecGloss/m-gly) (MPR) appelle les fonctions de notification de connexion lorsqu’il se connecte ou déconnecte une ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="34f5b-105">The [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the connection notification functions when it connects or disconnects a network resource.</span></span> <span data-ttu-id="34f5b-106">Pour recevoir ces notifications, vous pouvez implémenter ces fonctions dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="34f5b-106">To receive such notifications, you can implement these functions in a DLL.</span></span>

<span data-ttu-id="34f5b-107">Le MPR appelle la fonction [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) avant et après chaque opération d’ajout de connexion ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)ou [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span><span class="sxs-lookup"><span data-stu-id="34f5b-107">The MPR calls the [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) function before and after attempting each add-connection operation ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a), or [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span></span> <span data-ttu-id="34f5b-108">Cette fonction n’est pas appelée lorsque le MPR restaure automatiquement les connexions réseau.</span><span class="sxs-lookup"><span data-stu-id="34f5b-108">This function is not called when the MPR is automatically restoring network connections.</span></span>

<span data-ttu-id="34f5b-109">Le MPR appelle la fonction [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) avant et après chaque opération d’annulation de connexion ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) ou [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span><span class="sxs-lookup"><span data-stu-id="34f5b-109">The MPR calls the [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) function before and after attempting each cancel-connection operation ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) or [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span></span>

<span data-ttu-id="34f5b-110">Pour plus d’informations sur les fonctions WNet, consultez [mise en réseau Windows](/windows/desktop/WNet/windows-networking-wnet-).</span><span class="sxs-lookup"><span data-stu-id="34f5b-110">For more information about WNet functions, see [Windows Networking](/windows/desktop/WNet/windows-networking-wnet-).</span></span>

<span data-ttu-id="34f5b-111">Pour plus d’informations sur la création et l’inscription d’une application qui reçoit des notifications de connexion réseau, consultez réception de notifications de [connexion](receiving-connection-notifications.md) et [inscription pour recevoir des notifications de connexion](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="34f5b-111">For more information about how to create and register an application that receives network connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md) and [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 
