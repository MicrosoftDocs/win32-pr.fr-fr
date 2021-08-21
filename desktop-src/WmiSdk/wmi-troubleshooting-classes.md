---
description: WMI fournit un ensemble de classes de dépannage que les scripts et les applications peuvent utiliser pour obtenir des informations sur l’état interne de WMI pendant les opérations de fournisseur et de noyau WMI.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Classes de résolution des problèmes WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d3c5f1d40cd5da9e61ff289fc0b137ec7613ec8156fb0acc4f225e793a8407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049857"
---
# <a name="wmi-troubleshooting-classes"></a>Classes de résolution des problèmes WMI

WMI fournit un ensemble de classes de dépannage que les scripts et les applications peuvent utiliser pour obtenir des informations sur l’état interne de WMI pendant les opérations de fournisseur et de noyau WMI. Pour plus d’informations sur la résolution des problèmes liés à WMI, consultez [Dépannage WMI](wmi-troubleshooting.md) et [classes de dépannage et de](provider-configuration-and-troubleshooting-classes.md)résolution des problèmes.

WMI propose plusieurs classes de dépannage de base pour les opérations du fournisseur et du noyau WMI :

-   [**\_Compteurs WMIPROVIDER \_ msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    Seule une de ces classes est trouvée sur chaque système informatique. Il fournit le nombre de différents types d’opérations de fournisseur sur ce système.

-   [**\_WMISELFEVENT msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    Les classes de dépannage d’événements dérivent de [**msft \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent). Les requêtes de cette classe retournent des instances de classes d’événements telles que [**msft \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) ou [**msft \_ wmiprovider \_ CreateInstanceEnumAsyncEvent \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).

    La liste suivante fournit des liens vers différentes catégories de classes d’événements dérivées de [**msft \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):

    -   [Classes de dépannage des événements du fournisseur](provider-event-troubleshooting-classes.md)
    -   [Classes de dépannage ConsumerProvider](consumerprovider-troubleshooting-classes.md)
    -   [Classes de dépannage des événements du service WMI](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

[Réception d’un événement WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
