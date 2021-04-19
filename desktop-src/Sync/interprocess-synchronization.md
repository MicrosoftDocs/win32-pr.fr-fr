---
description: Plusieurs processus peuvent avoir des descripteurs sur le même objet Event, mutex, Semaphore ou Timer. ces objets peuvent donc être utilisés pour effectuer la synchronisation entre processus.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Synchronisation entre processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c18fb26d6a64fdc2d785d16c7bccb8b007c3f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528244"
---
# <a name="interprocess-synchronization"></a><span data-ttu-id="b85a5-103">Synchronisation entre processus</span><span class="sxs-lookup"><span data-stu-id="b85a5-103">Interprocess Synchronization</span></span>

<span data-ttu-id="b85a5-104">Plusieurs processus peuvent avoir des descripteurs sur le même objet Event, mutex, Semaphore ou Timer. ces objets peuvent donc être utilisés pour effectuer la synchronisation entre processus.</span><span class="sxs-lookup"><span data-stu-id="b85a5-104">Multiple processes can have handles to the same event, mutex, semaphore, or timer object, so these objects can be used to accomplish interprocess synchronization.</span></span> <span data-ttu-id="b85a5-105">Le processus qui crée un objet peut utiliser le handle retourné par la fonction de création ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore,**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)ou [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span><span class="sxs-lookup"><span data-stu-id="b85a5-105">The process that creates an object can use the handle returned by the creation function ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea), or [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)).</span></span> <span data-ttu-id="b85a5-106">D’autres processus peuvent ouvrir un handle vers l’objet à l’aide de son nom, ou par le biais de l’héritage ou de la duplication.</span><span class="sxs-lookup"><span data-stu-id="b85a5-106">Other processes can open a handle to the object by using its name, or through inheritance or duplication.</span></span> <span data-ttu-id="b85a5-107">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b85a5-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b85a5-108">Noms d’objets</span><span class="sxs-lookup"><span data-stu-id="b85a5-108">Object Names</span></span>](object-names.md)
-   [<span data-ttu-id="b85a5-109">Héritage d'objet</span><span class="sxs-lookup"><span data-stu-id="b85a5-109">Object Inheritance</span></span>](object-inheritance.md)
-   [<span data-ttu-id="b85a5-110">Duplication d’objets</span><span class="sxs-lookup"><span data-stu-id="b85a5-110">Object Duplication</span></span>](object-duplication.md)

 

 
