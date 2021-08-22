---
title: Quelles sont les actions de base de l’API de point de contrôle
description: Tous les points de contrôle effectuent les tâches suivantes.
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a102c389a41b32fd7a79bf749ce38f1267912c3993e2461adac9b6730ea92325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513639"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>Quelles sont les actions de base de l’API de point de contrôle ?

Tous les points de contrôle effectuent les tâches suivantes :

-   Recherchez les périphériques UPnP disponibles sur le réseau.
-   Déterminez lequel de ces appareils présente un intérêt.
-   Émettez les demandes de contrôle aux appareils intéressants et recevez les événements générés par les appareils.

Une application doit d’abord Rechercher les périphériques UPnP disponibles sur le réseau en effectuant une recherche. Étant donné que les critères de recherche définis par l’architecture UPnP sont assez larges, l’application peut trouver plus d’appareils que nécessaire. Par conséquent, l’application doit examiner les caractéristiques des appareils trouvés pour déterminer ceux qui correspondent le mieux aux critères de recherche. L’application peut ensuite émettre des demandes de contrôle à ces appareils.

Les sections suivantes expliquent comment effectuer ces opérations à l’aide de l’API de point de contrôle avec la technologie UPnP :

-   [Recherche d’appareils](finding-devices.md)
-   [Description des appareils](describing-devices.md)
-   [Contrôle des appareils](controlling-devices.md)

Pour obtenir une documentation détaillée sur chaque interface dans l’API du point de contrôle, consultez Référence de l' [API du point de contrôle](control-point-api-with-upnp-technology-reference.md).

 

 




