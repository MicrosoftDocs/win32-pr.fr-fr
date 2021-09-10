---
title: Single-Threaded et communication multithread
description: Single-Threaded et communication multithread
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363344"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Single-Threaded et communication multithread

Un client ou un serveur qui prend en charge les cloisonnements à thread unique et multithread aura un cloisonnement multithread, contenant tous les threads initialisés en tant que threads libres et un ou plusieurs Apartments (cloisonnés) à thread unique. Les pointeurs d’interface doivent être marshalés entre les Apartments, mais ils peuvent être utilisés sans marshaling dans un cloisonnement. Les appels aux objets dans un cloisonnement à thread unique sont synchronisés par COM. Les appels aux objets dans le cloisonnement multithread ne sont pas synchronisés par COM.

Toutes les informations sur les cloisonnements à thread unique s’appliquent aux threads marqués comme modèle cloisonné, et toutes les informations sur les Apartments (multithreads) s’appliquent à tous les threads marqués comme étant libres de threads. Les règles de thread cloisonné s’appliquent à la communication entre cloisonnements, ce qui nécessite que les pointeurs d’interface soient marshalés entre les cloisonnements avec des appels à [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) et [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), comme décrit dans les [cloisonnements à thread unique](single-threaded-apartments.md).

> [!Note]  
> Certaines considérations spéciales s’appliquent lors du traitement des serveurs in-process. Pour plus d’informations, consultez [problèmes de Threading du serveur in-process](in-process-server-threading-issues.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux interfaces à travers les Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Choix du modèle de thread](choosing-the-threading-model.md)
</dt> <dt>

[Apartments (cloisonnés) multithread](multithreaded-apartments.md)
</dt> <dt>

[Problèmes liés aux threads du serveur in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processus, threads et Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Apartments (cloisonnés) à thread unique](single-threaded-apartments.md)
</dt> </dl>

 

 




