---
description: Le \_32.dll Ws2 fournit des fonctionnalités pour la création d’objets d’événements aux applications et aux fournisseurs de services, bien que, dans la plupart des cas, les objets d’événements soient créés par des applications.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Création d’objets d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec202f8f17790ed85979a8287005aa65374a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513224"
---
# <a name="creating-event-objects"></a><span data-ttu-id="78c71-103">Création d’objets d’événement</span><span class="sxs-lookup"><span data-stu-id="78c71-103">Creating Event Objects</span></span>

<span data-ttu-id="78c71-104">Le \_32.dll Ws2 fournit des fonctionnalités pour la création d’objets d’événements aux applications et aux fournisseurs de services, bien que, dans la plupart des cas, les objets d’événements soient créés par des applications.</span><span class="sxs-lookup"><span data-stu-id="78c71-104">The Ws2\_32.dll provides facilities for event object creation to both applications and service providers, although in most instances event objects will be created by applications.</span></span> <span data-ttu-id="78c71-105">Les services d’objets d’événement sont mis à la disposition des fournisseurs de services Windows Sockets par le biais de [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simplement comme un mécanisme pratique pour tout traitement interne qui peut en tirer parti.</span><span class="sxs-lookup"><span data-stu-id="78c71-105">Event object services are made available to Windows Sockets service providers through [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simply as a convenience mechanism for any internal processing that may benefit from same.</span></span> <span data-ttu-id="78c71-106">Notez que le descripteur d’objet d’événement est valide uniquement dans le contexte du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="78c71-106">Note that the event object handle is only valid in the context of the calling process.</span></span> <span data-ttu-id="78c71-107">Dans les environnements Windows, la réalisation d’objets d’événements s’effectue via les services d’événements natifs fournis par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="78c71-107">In Windows environments the realization of event objects is through the native event services provided by the operating system.</span></span>

 

 



