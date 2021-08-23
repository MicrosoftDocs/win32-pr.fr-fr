---
title: Contrôle des appareils
description: Les périphériques basés sur UPnP sont contrôlés par les services qu’ils exposent.
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410818552f1f6563b28fcb963fcfca5c9b3067973e325adfd66ede5bffaedb75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999629"
---
# <a name="controlling-devices"></a>Contrôle des appareils

Les périphériques basés sur UPnP sont contrôlés par les services qu’ils exposent. Un service UPnP est la plus petite entité contrôlable de l’architecture UPnP. Les appareils exposent un service pour chaque fonction principale qu’ils exécutent. Les appareils complexes sont généralement composés de plusieurs services simples et d’autres périphériques.

Un service se compose d’un ensemble de variables d’État et d’un ensemble d’actions qu’une application peut appeler et qui opèrent sur ces variables d’État. Dans l’API du point de contrôle avec la technologie UPnP, les services sont représentés par des objets de **service** qui exposent l’interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .

Un type de service définit les variables d’État et les actions prises en charge par un service particulier. Par exemple, le type de service d’un service horloge définit des actions **getTime** et **setTime** , ainsi qu’une variable d’état de **temps** .

Un ID de service différencie plusieurs types de service communs au sein d’un même appareil. Par exemple, il peut y avoir deux services d’horloge dans une horloge, un pour l’horloge normale et l’autre pour l’alarme. Il doit exister un moyen de faire la distinction entre les deux services, qui ont des types de service identiques. L’ID de service offre un moyen unique d’identifier une instance d’un type de service. Ensuite, cet ID de service est utilisé pour accéder au service approprié à partir de la collection [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) , car le type de service n’est pas un identificateur unique. L’interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) permet également aux applications d’enregistrer une fonction de rappel avec l’objet de service. Lorsque la valeur de la variable d’état d’un service change, l’objet de service appelle le rappel inscrit pour notifier l’application de la modification. L’infrastructure UPnP appelle également ce rappel pour notifier les applications lorsqu’une instance de service est devenue indisponible. Le service peut devenir indisponible pour diverses raisons, notamment une défaillance réseau temporaire.

Pour plus d'informations, voir les rubriques suivantes :

-   [Obtention d’objets de service](obtaining-service-objects.md)
-   [Inscription d’un rappel](registering-a-callback.md)
-   [Interrogation des variables d’État](querying-state-variables.md)
-   [Appel d’actions](invoking-actions.md)

 

 




