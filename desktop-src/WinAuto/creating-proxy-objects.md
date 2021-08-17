---
title: Création d’objets proxy
description: En plus de concevoir des classes qui implémentent des propriétés et des méthodes IAccessible, les développeurs de serveurs peuvent également être amenés à concevoir des objets proxy qui surveillent la durée de vie des objets accessibles.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49abceb3b38b4495d871605634c8f95353c35b4b6bcd0c54dda374c75572fbea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133892"
---
# <a name="creating-proxy-objects"></a>Création d’objets proxy

En plus de concevoir des classes qui implémentent des propriétés et des méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , les développeurs de serveurs peuvent également être amenés à concevoir des objets *proxy* qui surveillent la durée de vie des objets accessibles. Si un objet accessible dans une application est disponible pendant toute la durée d’exécution de l’application, vous n’avez pas besoin de créer un objet proxy. S’il est possible de détruire l’objet accessible pendant que l’application est en cours d’exécution, vous devez créer un objet proxy.

## <a name="in-this-section"></a>Dans cette section

-   [Que sont les objets proxy ?](what-are-proxy-objects.md)
-   [Raisons pour lesquelles les objets proxy sont nécessaires](why-proxy-objects-are-needed.md)
-   [Considérations relatives à la conception des objets proxy](design-considerations-for-proxy-objects.md)

 

 




