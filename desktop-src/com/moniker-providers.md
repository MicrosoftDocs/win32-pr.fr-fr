---
title: Fournisseurs de moniker
description: Fournisseurs de moniker
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673101"
---
# <a name="moniker-providers"></a>Fournisseurs de moniker

En général, un composant doit être un fournisseur de monikers lorsqu’il autorise l’accès à l’un de ses objets, tout en contrôlant encore le stockage de l’objet. Si un composant va distribuer des monikers qui identifient ses objets, il doit être capable d’effectuer les tâches suivantes :

-   Sur demande, créez un moniker qui identifie un objet.
-   Permet au moniker d’être lié lorsqu’un client appelle [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sur celui-ci.

Un fournisseur de monikers doit créer un moniker d’une *classe de moniker* appropriée pour identifier un objet. La classe moniker fait référence à une implémentation spécifique de l’interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) qui définit le type de moniker créé. Bien que vous puissiez implémenter **IMoniker** pour créer une nouvelle classe moniker, il est souvent inutile, car OLE fournit des implémentations de plusieurs classes de moniker, chacune avec son propre CLSID. Pour obtenir les descriptions des classes moniker fournies par OLE, consultez [implémentations de moniker OLE](ole-moniker-implementations.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients moniker](moniker-clients.md)
</dt> <dt>

[Implémentations du moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




