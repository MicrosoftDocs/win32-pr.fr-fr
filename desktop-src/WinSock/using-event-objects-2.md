---
description: Les objets d’événement Windows Sockets sont des constructions simples qui peuvent être créées et fermées, définies et désactivées, attendues et interrogées.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Utilisation d’objets d’événement (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517494"
---
# <a name="using-event-objects-windows-sockets-2"></a><span data-ttu-id="b4c97-103">Utilisation d’objets d’événement (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="b4c97-103">Using Event Objects (Windows Sockets 2)</span></span>

<span data-ttu-id="b4c97-104">Les objets d’événement Windows Sockets sont des constructions simples qui peuvent être créées et fermées, définies et désactivées, attendues et interrogées.</span><span class="sxs-lookup"><span data-stu-id="b4c97-104">Windows Sockets event objects are simple constructs that can be created and closed, set and cleared, waited upon and polled.</span></span> <span data-ttu-id="b4c97-105">Le modèle accepté permet aux clients de créer un objet d’événement et de fournir le descripteur en tant que paramètre (ou en tant que composant d’une structure de paramètres) dans des fonctions telles que [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) et [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b4c97-105">The accepted model is for clients to create an event object and supply the handle as a parameter (or as a component of a parameter structure) in functions such as [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="b4c97-106">Lorsque la condition nommée s’est produite, le fournisseur de services utilise le handle pour définir l’objet d’événement en appelant [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span><span class="sxs-lookup"><span data-stu-id="b4c97-106">When the nominated condition has occurred, the service provider uses the handle to set the event object by calling [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span></span> <span data-ttu-id="b4c97-107">Pendant ce temps, le client Winsock SPI peut bloquer et attendre ou interroger jusqu’à ce que l’objet d’événement soit défini (signalé).</span><span class="sxs-lookup"><span data-stu-id="b4c97-107">Meanwhile, the Winsock SPI client may either block and wait or poll until the event object becomes set (signaled).</span></span> <span data-ttu-id="b4c97-108">Le client peut ensuite effacer ou réinitialiser l’objet d’événement et l’utiliser à nouveau.</span><span class="sxs-lookup"><span data-stu-id="b4c97-108">The client may subsequently clear or reset the event object and use it again.</span></span>

 

 
