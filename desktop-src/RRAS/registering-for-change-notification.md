---
title: Inscription à la notification de modification
description: Un client peut s’inscrire pour recevoir une notification des modifications apportées aux informations de routage stockées dans le gestionnaire de tables de routage. Cette demande ne peut être effectuée qu’après qu’un client s’est inscrit auprès du gestionnaire de tables de routage.
ms.assetid: 90dc98eb-0d0b-4450-848b-c7cedab75a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3a98062fee73c481c1f47c32fa7eeb5465a112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309842"
---
# <a name="registering-for-change-notification"></a><span data-ttu-id="96156-104">Inscription à la notification de modification</span><span class="sxs-lookup"><span data-stu-id="96156-104">Registering for Change Notification</span></span>

<span data-ttu-id="96156-105">Un client peut s’inscrire pour recevoir une notification des modifications apportées aux informations de routage stockées dans le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="96156-105">A client can register to receive notification of changes to routing information that is stored in the routing table manager.</span></span> <span data-ttu-id="96156-106">Cette demande ne peut être effectuée qu’après qu’un client s’est inscrit auprès du gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="96156-106">This request can only be made after a client has registered with the routing table manager.</span></span>

<span data-ttu-id="96156-107">Pour s’inscrire à la notification de modification, un client doit appeler [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), en spécifiant les types de modifications pour lesquels le client doit recevoir une notification.</span><span class="sxs-lookup"><span data-stu-id="96156-107">To register for change notification, a client must call [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification), specifying the types of changes for which the client must receive notification.</span></span> <span data-ttu-id="96156-108">Si le client doit être averti de la modification de destinations spécifiques, le client appelle [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) une fois pour chaque destination.</span><span class="sxs-lookup"><span data-stu-id="96156-108">If the client must be notified of change to specific destinations, the client calls [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification) once for each destination.</span></span>

<span data-ttu-id="96156-109">Le client peut cesser de recevoir des notifications de modification en appelant [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span><span class="sxs-lookup"><span data-stu-id="96156-109">The client can stop receiving change notifications by calling [**RtmDeregisterFromChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterfromchangenotification).</span></span>

<span data-ttu-id="96156-110">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [Register for change notification](register-for-change-notification.md).</span><span class="sxs-lookup"><span data-stu-id="96156-110">For sample code that shows how to use these functions, see [Register For Change Notification](register-for-change-notification.md).</span></span>

 

 




