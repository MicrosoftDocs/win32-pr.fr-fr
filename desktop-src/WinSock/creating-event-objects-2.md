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
# <a name="creating-event-objects"></a>Création d’objets d’événement

Le \_32.dll Ws2 fournit des fonctionnalités pour la création d’objets d’événements aux applications et aux fournisseurs de services, bien que, dans la plupart des cas, les objets d’événements soient créés par des applications. Les services d’objets d’événement sont mis à la disposition des fournisseurs de services Windows Sockets par le biais de [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simplement comme un mécanisme pratique pour tout traitement interne qui peut en tirer parti. Notez que le descripteur d’objet d’événement est valide uniquement dans le contexte du processus appelant. Dans les environnements Windows, la réalisation d’objets d’événements s’effectue via les services d’événements natifs fournis par le système d’exploitation.

 

 



