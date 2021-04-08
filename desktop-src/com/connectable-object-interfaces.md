---
title: Interfaces d’objets connectables
description: Interfaces d’objets connectables
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840793"
---
# <a name="connectable-object-interfaces"></a>Interfaces d’objets connectables

La prise en charge des objets connectables nécessite la prise en charge de quatre interfaces :

-   [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) sur l’objet connectable
-   [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) sur l’objet point de connexion
-   [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) sur un objet énumérateur
-   [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) sur un objet énumérateur

Les deux derniers sont définis en tant qu’énumérateurs standard pour les types **IConnectionPoint \*** et [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).

En outre, l’objet connectable peut éventuellement prendre en charge [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) et [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) pour fournir suffisamment d’informations à un client afin que le client puisse assurer la prise en charge de l’interface sortante au moment de l’exécution.

Enfin, le client doit fournir un objet récepteur qui implémente l’interface sortante, qui est une interface COM personnalisée définie par l’objet connectable.

Pour plus d'informations, voir les rubriques suivantes :

-   [Utilisation de IConnectionPointContainer](using-iconnectionpointcontainer.md)
-   [Utilisation de IConnectionPoint](using-iconnectionpoint.md)
-   [Utilisation de IProvideClassInfo](using-iprovideclassinfo.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Architecture des objets connectables](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




