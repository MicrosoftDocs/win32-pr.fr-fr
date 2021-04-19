---
description: Un objet d’événement est un objet de synchronisation dont l’État peut être défini explicitement comme signalé à l’aide de la fonction SetEvent. Voici les deux types d’objets d’événement.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Objets d’événement (synchronisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365b42bb7550507fe3522f07d950dac74c88843d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530885"
---
# <a name="event-objects-synchronization"></a>Objets d’événement (synchronisation)

Un *objet d’événement* est un objet de synchronisation dont l’État peut être défini explicitement comme signalé à l’aide de la fonction [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) . Voici les deux types d’objets d’événement.



| Object             | Description                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Événement de réinitialisation manuelle | Objet d’événement dont l’état reste signalé jusqu’à ce qu’il soit explicitement réinitialisé à l’état non signalé par la fonction [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) . Bien qu’il soit signalé, un nombre quelconque de threads en attente, ou des threads qui spécifient par la suite le même objet d’événement dans l’une des [fonctions d’attente](wait-functions.md), peuvent être libérés.                                                                                                        |
| Événement de réinitialisation automatique   | Objet d’événement dont l’état reste signalé jusqu’à ce qu’un seul thread en attente soit libéré, auquel cas le système définit automatiquement l’État sur non signalé. Si aucun thread n’attend, l’état de l’objet d’événement reste signalé. Si plusieurs threads sont en attente, un thread en attente est sélectionné. Ne supposez pas un ordre FIFO (premier entré, premier sorti). Les événements externes tels que les APC en mode noyau peuvent modifier l’ordre d’attente.<br/> |



 

L’objet d’événement est utile pour envoyer un signal à un thread indiquant qu’un événement particulier s’est produit. Par exemple, dans les entrées et sorties avec chevauchement, le système définit un objet d’événement spécifié à l’état signalé lorsque l’opération Overlapped est terminée. Un thread unique peut spécifier différents objets d’événement dans plusieurs opérations simultanées avec chevauchement, puis utiliser l’une des [fonctions d’attente](wait-functions.md) à plusieurs objets pour attendre que l’état de l’un des objets d’événement soit signalé.

Un thread utilise la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) ou [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) pour créer un objet d’événement. Le thread de création spécifie l’état initial de l’objet et s’il s’agit d’un objet d’événement à réinitialisation manuelle ou à réinitialisation automatique. Le thread de création peut également spécifier un nom pour l’objet d’événement. Les threads d’autres processus peuvent ouvrir un handle vers un objet d’événement existant en spécifiant son nom dans un appel à la fonction [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa) . Pour plus d’informations sur les noms des objets mutex, Event, Semaphore et Timer, consultez [synchronisation entre processus](interprocess-synchronization.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’objets d’événement](using-event-objects.md)
</dt> </dl>

 

 
