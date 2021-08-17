---
title: Utilisation de IConnectionPoint
description: Utilisation de IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2449be5f1711457807666e9e2068d13defd8437bedee93402f7b974d5298d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129421"
---
# <a name="using-iconnectionpoint"></a>Utilisation de IConnectionPoint

Lorsque le client a un pointeur vers un point de connexion, il peut effectuer les opérations suivantes, comme exprimé par [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint):

-   En premier lieu, [**IConnectionPoint :: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) récupère l’IID d’interface sortante pris en charge par le point de connexion. Lorsqu’elle est utilisée conjointement avec [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints), cette méthode permet au client d’examiner les IID de toutes les interfaces sortantes prises en charge sur l’objet connectable.
-   Deuxièmement, un client peut naviguer à partir du point de connexion vers l’interface [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) de l’objet connectable par le biais de la méthode [**IConnectionPoint :: GetConnectionPointContainer**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer) .
-   Troisièmement, les méthodes les plus intéressantes pour le client sont [**IConnectionPoint :: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) et [**IConnectionPoint :: Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Lorsqu’un client souhaite connecter son propre objet récepteur à l’objet connectable, le client passe le pointeur [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) du récepteur (ou tout autre pointeur d’interface sur le même objet) à **conseiller**. Le point de connexion interroge le récepteur pour l’interface sortante spécifique qui est attendue. Si cette interface est disponible sur le récepteur, le point de connexion stocke ensuite le pointeur d’interface. À partir de ce point jusqu’à l’appel de **Unadvise** , l’objet connectable effectue des appels au récepteur via cette interface lorsque des événements se produisent. Pour déconnecter le récepteur du point de connexion, le client passe une clé retournée de la part de l' **Avertissement** à la méthode **Unadvise** . **Unadvise** doit appeler [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur l’interface du récepteur.
-   Enfin, un client peut demander à un point de connexion d’énumérer toutes les connexions qui existent avec [**IConnectionPoint :: EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections). Cette méthode crée un objet énumérateur (avec un nombre de références distinct) qui retourne un pointeur [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) vers celui-ci. Le client doit appeler [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) quand l’énumérateur n’est plus nécessaire. En outre, l’énumérateur retourne une série de structures [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata) , une pour chaque connexion. Chaque structure décrit une connexion à l’aide du pointeur [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) du récepteur, ainsi que la clé de connexion initialement retournée par la fonction [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise). Lorsque vous avez terminé avec ces pointeurs d’interface sink, le client doit appeler **Release** sur chaque pointeur retourné dans une structure **CONNECTDATA** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces d’objets connectables](connectable-object-interfaces.md)
</dt> </dl>

 

 