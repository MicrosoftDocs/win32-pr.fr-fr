---
description: Les fonctions WSAEventSelect et WSAEnumNetworkEvents sont fournies pour s’adapter aux applications telles que les démons et les services qui n’ont pas d’interface utilisateur (et donc n’utilisent pas de handles Windows).
ms.assetid: 4254937c-7ee6-49a3-9f30-09aebaf2265b
title: Notification asynchrone à l’aide d’objets d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0495507eacf0960dc98f31594d7f4881d51488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862590"
---
# <a name="asynchronous-notification-using-event-objects"></a><span data-ttu-id="0bfb5-103">Notification asynchrone à l’aide d’objets d’événement</span><span class="sxs-lookup"><span data-stu-id="0bfb5-103">Asynchronous Notification Using Event Objects</span></span>

<span data-ttu-id="0bfb5-104">Les fonctions [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) et [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) sont fournies pour s’adapter aux applications telles que les démons et les services qui n’ont pas d’interface utilisateur (et donc n’utilisent pas de handles Windows).</span><span class="sxs-lookup"><span data-stu-id="0bfb5-104">The [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) and [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) functions are provided to accommodate applications such as daemons and services that have no user interface (and hence do not use Windows handles).</span></span> <span data-ttu-id="0bfb5-105">La fonction **WSAEventSelect** se comporte exactement comme la fonction [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) .</span><span class="sxs-lookup"><span data-stu-id="0bfb5-105">The **WSAEventSelect** function behaves exactly like the [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) function.</span></span> <span data-ttu-id="0bfb5-106">Toutefois, au lieu d’envoyer un message Windows à l’occurrence d’un \_ événement réseau FD xxx (par exemple, FD \_ Read et FD \_ Write), un objet d’événement désigné par l’application est défini.</span><span class="sxs-lookup"><span data-stu-id="0bfb5-106">However, instead of causing a Windows message to be sent on the occurrence of an FD\_XXX network event (for example, FD\_READ and FD\_WRITE), an application-designated event object is set.</span></span>

<span data-ttu-id="0bfb5-107">En outre, le fait qu’un événement réseau FD xxx particulier s’est \_ produit est mémorisé par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="0bfb5-107">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="0bfb5-108">L’application peut appeler [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) pour que le contenu actuel de la mémoire d’événements réseau soit copié dans une mémoire tampon fournie par l’application et que la mémoire d’événements réseau soit automatiquement effacée.</span><span class="sxs-lookup"><span data-stu-id="0bfb5-108">The application can call [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) to have the current contents of the network event memory copied to an application-supplied buffer and to have the network event memory automatically cleared.</span></span> <span data-ttu-id="0bfb5-109">Si nécessaire, l’application peut également désigner un objet événement particulier qui est effacé avec la mémoire de l’événement réseau.</span><span class="sxs-lookup"><span data-stu-id="0bfb5-109">If needed, the application can also designate a particular event object that is cleared along with the network event memory.</span></span>

 

 



