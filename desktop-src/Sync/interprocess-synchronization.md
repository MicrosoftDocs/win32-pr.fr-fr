---
description: Plusieurs processus peuvent avoir des descripteurs sur le même objet Event, mutex, Semaphore ou Timer. ces objets peuvent donc être utilisés pour effectuer la synchronisation entre processus.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Synchronisation entre processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0caf4818a05d526a70a1e3257ec6f86d0279f39ce3cf05a4411e49991db6ba15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886349"
---
# <a name="interprocess-synchronization"></a>Synchronisation entre processus

Plusieurs processus peuvent avoir des descripteurs sur le même objet Event, mutex, Semaphore ou Timer. ces objets peuvent donc être utilisés pour effectuer la synchronisation entre processus. Le processus qui crée un objet peut utiliser le handle retourné par la fonction de création ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore,**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)ou [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). D’autres processus peuvent ouvrir un handle vers l’objet à l’aide de son nom, ou par le biais de l’héritage ou de la duplication. Pour plus d'informations, voir les rubriques suivantes :

-   [Noms d’objets](object-names.md)
-   [Héritage d'objet](object-inheritance.md)
-   [Duplication d’objets](object-duplication.md)

 

 
