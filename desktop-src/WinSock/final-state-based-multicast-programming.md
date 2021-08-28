---
description: Cette section décrit la programmation de la multidiffusion basée sur l’état final à l’aide d’IOCTL au lieu des options de Socket. Pour obtenir une vue d’ensemble de la façon dont la programmation de la multidiffusion basée sur l’État diffère de la programmation de multidiffusion basée sur les modifications, consultez programmation de la multidiffusion.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programmation de la multidiffusion basée sur l’état final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad31f0c840228e1fea729582f5e259ec92c4a04381752ed9ee50db2586b3b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132512"
---
# <a name="final-state-based-multicast-programming"></a>Programmation de la multidiffusion basée sur l’état final

Cette section décrit la programmation de la multidiffusion basée sur l’état final à l’aide d’IOCTL au lieu des options de Socket. Pour obtenir une vue d’ensemble de la façon dont la programmation de la multidiffusion basée sur l’État diffère de la programmation de multidiffusion basée sur les modifications, consultez programmation de la [multidiffusion](multicast-programming.md).

le tableau suivant décrit les Windows de sockets ioctl utilisés pour la programmation multidiffusion sur Windows. 

| IOCTL                       | Type d’argument                                   |
|-----------------------------|-------------------------------------------------|
| SIOCSMSFILTER               | [**Groupe \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Structure de filtre |
| SIOCGMSFILTER               | [**Groupe \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Structure de filtre |
| SIO \_ recevoir le \_ filtre de multidiffusion \_ | structure [**IP \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |
| SIO \_ définir un \_ filtre de multidiffusion \_ | structure [**IP \_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |



 

notez que les ioctl **SIOCSMSFILTER** et **SIOCGMSFILTER** sont disponibles sur Windows Vista et versions ultérieures.

L’utilisation de ces ioctl pour la programmation de la multidiffusion présente des avantages en matière de performances lorsque vous utilisez des listes de sources volumineuses. Pour plus d’informations sur les paramètres et les paramètres associés à l’utilisation de SIO Filter multicast ou d’un filtre de \_ \_ \_ \_ \_ multidiffusion SIO \_ , consultez la page de référence de [**\_ filtre de groupe**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) . Pour plus d’informations sur les paramètres et les paramètres associés à l’utilisation de SIO \_ \_ , obtenir un filtre de multidiffusion \_ ou SIO \_ définir \_ \_ un filtre de multidiffusion, consultez la page de référence [**\_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) .

 

 



