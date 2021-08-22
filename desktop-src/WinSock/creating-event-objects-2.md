---
description: Le \_32.dll Ws2 fournit des fonctionnalités pour la création d’objets d’événements aux applications et aux fournisseurs de services, bien que, dans la plupart des cas, les objets d’événements soient créés par des applications.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Création d’objets d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab867e6398db4b5c97303c8739431d7baaca311daf8d103f4375721e96a864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051697"
---
# <a name="creating-event-objects"></a>Création d’objets d’événement

Le \_32.dll Ws2 fournit des fonctionnalités pour la création d’objets d’événements aux applications et aux fournisseurs de services, bien que, dans la plupart des cas, les objets d’événements soient créés par des applications. les services d’objets d’événement sont mis à la disposition des fournisseurs de services de sockets Windows par le biais de [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simplement comme un mécanisme pratique pour tout traitement interne susceptible d’en tirer parti. Notez que le descripteur d’objet d’événement est valide uniquement dans le contexte du processus appelant. dans Windows environnements, la réalisation d’objets d’événements s’effectue via les services d’événements natifs fournis par le système d’exploitation.

 

 



