---
description: Un programme de contrôle de service démarre et contrôle les services.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programmes de contrôle de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb11e8224a23edcebd0688039502c5bc38da929d47cba470e6f397f4430e444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889042"
---
# <a name="service-control-programs"></a>Programmes de contrôle de service

Un programme de contrôle de service démarre et contrôle les services. Il effectue les actions suivantes :

-   Démarre un service ou un service de pilote, si le type de démarrage est \_ démarrage de la demande de service \_ .
-   Envoie des demandes de contrôle à un service en cours d’exécution.
-   Interroge l’état actuel d’un service en cours d’exécution.

Ces actions requièrent un handle ouvert pour l’objet de service. Pour obtenir le descripteur, le programme de contrôle des services doit :

1.  Utilisez la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) pour obtenir un descripteur de la base de données SCM sur une machine spécifiée.
2.  Utilisez la fonction [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) ou [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) pour obtenir un handle de l’objet de service.

Pour plus d'informations, voir les rubriques suivantes :

-   [Démarrage du service](service-startup.md)
-   [Demandes de contrôle de service](service-control-requests.md)
-   [Contrôle d’un service à l’aide de SC](controlling-a-service-using-sc.md)

 

 



