---
title: Utilisation de IConnectionPointContainer
description: Utilisation de IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a8d53e9051796cafa4a8c7825d810b18784d58a4dd5d531eb38872b87cb32c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992029"
---
# <a name="using-iconnectionpointcontainer"></a>Utilisation de IConnectionPointContainer

Un objet connectable implémente [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (et l’expose via [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) pour indiquer l’existence des interfaces sortantes. Pour chaque interface sortante, l’objet connectable gère un sous-objet de point de connexion qui implémente lui-même un [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint). L’objet connectable contient donc les points de connexion, par conséquent l’attribution de noms à **IConnectionPointContainer** et à **IConnectionPoint**.

Via [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer), un client peut effectuer deux opérations. Tout d’abord, si le client possède déjà l’IID pour une interface sortante qu’il prend en charge, il peut localiser le point de connexion correspondant pour l’IID à l’aide de [**IConnectionPointContainer :: FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint). Le client ne peut pas interroger directement le point de connexion en raison de la relation conteneur/contenu entre l’objet connectable et ses points de connexion contenus. Fondamentalement, **FindConnectionPoint** est le [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) pour les interfaces sortantes lorsque l’IID est connu du client.

Deuxièmement, le client peut énumérer tous les points de connexion dans l’objet connectable via [**IConnectionPointContainer :: EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Cette méthode retourne un pointeur d’interface [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) pour un objet énumérateur séparé. Via [**IEnumConnectionPoints :: Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next), le client peut obtenir des pointeurs d’interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) vers chaque point de connexion.

Une fois que le client a obtenu l’interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) , il doit appeler [**IConnectionPoint :: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) pour déterminer l’IID de l’interface sortante prise en charge par chaque point de connexion. Si le client prend déjà en charge cette interface sortante, il peut établir une connexion. Dans le cas contraire, il peut toujours être en mesure de prendre en charge l’interface sortante en utilisant les informations de la bibliothèque de types de l’objet connectable pour assurer la prise en charge au moment de l’exécution. Cette technique nécessite que l’objet connectable prenne en charge l’interface [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) . (Consultez [utilisation de IProvideClassInfo](using-iprovideclassinfo.md).)

Étant donné que l’énumérateur est un objet distinct, le client doit appeler **IEnumConnectionPoints :: Release** quand l’énumérateur n’est plus nécessaire. En outre, chaque point de connexion est un objet avec un nombre de références distinct de l’objet connectable contenant. Par conséquent, le client doit également appeler IConnectionPoint :: Release pour chaque point de connexion accessible via l’énumérateur ou via [**FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces d’objets connectables](connectable-object-interfaces.md)
</dt> </dl>

 

 




