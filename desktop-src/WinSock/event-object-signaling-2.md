---
description: WSPEventSelect se comporte exactement comme WSPAsyncSelect, sauf que, au lieu de provoquer l’envoi d’un message Windows à l’occurrence d’un \_ événement réseau FD xxx nommé (par exemple, FD \_ Read, FD \_ Write, etc.), un objet d’événement désigné est défini.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Signalement d’objet d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544660"
---
# <a name="event-object-signaling"></a><span data-ttu-id="36a07-103">Signalement d’objet d’événement</span><span class="sxs-lookup"><span data-stu-id="36a07-103">Event Object Signaling</span></span>

<span data-ttu-id="36a07-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) se comporte exactement comme [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , sauf que, au lieu de provoquer l’envoi d’un message Windows à l’occurrence d’un \_ événement réseau FD xxx nommé (par exemple, FD \_ Read, FD \_ Write, etc.), un objet d’événement désigné est défini.</span><span class="sxs-lookup"><span data-stu-id="36a07-104">[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) behaves exactly like [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) except that, rather than cause a Windows message to be sent upon the occurrence of any nominated FD\_XXX network event (for example, FD\_READ, FD\_WRITE, etc.), a designated event object is set.</span></span>

<span data-ttu-id="36a07-105">En outre, le fait qu’un événement réseau FD xxx particulier s’est \_ produit est mémorisé par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="36a07-105">Also, the fact that a particular FD\_XXX network event has occurred is remembered by the service provider.</span></span> <span data-ttu-id="36a07-106">Cette opération est nécessaire, car l’occurrence de tout événement réseau désigné entraîne la signalisation d’un objet d’événement unique.</span><span class="sxs-lookup"><span data-stu-id="36a07-106">This is needed since the occurrence of any and all nominated network events will result in a single event object becoming signaled.</span></span> <span data-ttu-id="36a07-107">Un appel à [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) entraîne la copie du contenu actuel de la mémoire d’événements réseau vers une mémoire tampon fournie par le client et la mémoire d’événements réseau à effacer.</span><span class="sxs-lookup"><span data-stu-id="36a07-107">A call to [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) causes the current contents of the network event memory to be copied to a client-supplied buffer and the network event memory to be cleared.</span></span> <span data-ttu-id="36a07-108">Le client peut également désigner un objet d’événement particulier à effacer de manière atomique en même temps que la mémoire de l’événement réseau.</span><span class="sxs-lookup"><span data-stu-id="36a07-108">The client may also designate a particular event object to be cleared atomically along with the network event memory.</span></span>

 

 
