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
# <a name="asynchronous-notification-using-event-objects"></a>Notification asynchrone à l’aide d’objets d’événement

Les fonctions [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) et [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnetworkevents) sont fournies pour s’adapter aux applications telles que les démons et les services qui n’ont pas d’interface utilisateur (et donc n’utilisent pas de handles Windows). La fonction **WSAEventSelect** se comporte exactement comme la fonction [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) . Toutefois, au lieu d’envoyer un message Windows à l’occurrence d’un \_ événement réseau FD xxx (par exemple, FD \_ Read et FD \_ Write), un objet d’événement désigné par l’application est défini.

En outre, le fait qu’un événement réseau FD xxx particulier s’est \_ produit est mémorisé par le fournisseur de services. L’application peut appeler [**WSAEnumNetworkEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) pour que le contenu actuel de la mémoire d’événements réseau soit copié dans une mémoire tampon fournie par l’application et que la mémoire d’événements réseau soit automatiquement effacée. Si nécessaire, l’application peut également désigner un objet événement particulier qui est effacé avec la mémoire de l’événement réseau.

 

 



