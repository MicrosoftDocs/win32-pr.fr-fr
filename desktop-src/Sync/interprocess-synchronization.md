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
# <a name="interprocess-synchronization"></a>Synchronisation entre processus

Plusieurs processus peuvent avoir des descripteurs sur le même objet Event, mutex, Semaphore ou Timer. ces objets peuvent donc être utilisés pour effectuer la synchronisation entre processus. Le processus qui crée un objet peut utiliser le handle retourné par la fonction de création ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**CreateSemaphore,**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)ou [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). D’autres processus peuvent ouvrir un handle vers l’objet à l’aide de son nom, ou par le biais de l’héritage ou de la duplication. Pour plus d'informations, voir les rubriques suivantes :

-   [Noms d’objets](object-names.md)
-   [Héritage d'objet](object-inheritance.md)
-   [Duplication d’objets](object-duplication.md)

 

 
