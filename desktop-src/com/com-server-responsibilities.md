---
title: Responsabilités du serveur COM
description: Responsabilités du serveur COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363300"
---
# <a name="com-server-responsibilities"></a>Responsabilités du serveur COM

L’une des façons les plus importantes pour un client d’obtenir un pointeur vers un objet est que le client demande qu’un serveur soit lancé et qu’une instance de l’objet fourni par le serveur soit créée et activée. Il incombe au serveur de s’assurer que cela se produit correctement. Il existe plusieurs parties importantes.

Le serveur doit implémenter le code d’un objet de classe par le biais d’une implémentation de l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ou [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .

Le serveur doit inscrire son CLSID dans le registre système sur l’ordinateur sur lequel il se trouve et il est également possible de publier son emplacement d’ordinateur sur d’autres systèmes sur un réseau pour permettre aux clients de l’appeler sans que le client ait besoin de connaître l’emplacement du serveur.

Le serveur est principalement responsable de la sécurité ; autrement dit, dans la plupart des cas, le serveur détermine s’il doit fournir un pointeur vers l’un de ses objets à un client.

Les serveurs in-process doivent implémenter et exporter certaines fonctions qui permettent au processus client de les instancier.

Les rubriques suivantes détaillent les responsabilités du serveur COM :

-   [Implémentation de IClassFactory](implementing-iclassfactory.md)
-   [Licences et IClassFactory2](licensing-and-iclassfactory2.md)
-   [Inscription des serveurs COM](registering-com-servers.md)
-   [Assistances pour l’implémentation de serveur hors processus](out-of-process-server-implementation-helpers.md)
-   [Création et optimisations de GUID](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients et serveurs COM](com-clients-and-servers.md)
</dt> </dl>

 

 