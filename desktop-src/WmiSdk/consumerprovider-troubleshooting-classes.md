---
description: Le tableau suivant répertorie les classes d’événements qui sont générées par les opérations du fournisseur de consommateur d’événements.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Classes de dépannage ConsumerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740b8c0eb1884181fa84efe26e0611dda4b1712f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443610"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Classes de dépannage ConsumerProvider

Le tableau suivant répertorie les classes d’événements qui sont générées par les opérations du [*fournisseur de consommateur d’événements*](gloss-e.md) .

Vous pouvez vous abonner aux notifications [**\_ ProviderEvent msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) de la classe de base abstraite pour obtenir tous les événements suivants.



| Événement                                                                                                | Description                                                                                |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_WMIPROVIDEREVENT msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Classe parente pour tous les événements du fournisseur de consommateurs.                                  |
| [**\_WMICONSUMERPROVIDERLOADED msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Définit l’activation réussie de l’objet COM du fournisseur de consommateur d’événements.    |
| [**\_WMICONSUMERPROVIDERUNLOADED msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Définit la réussite de la désactivation de l’objet COM du fournisseur de consommateur d’événements.  |
| [**\_WMICONSUMERPROVIDERSINKLOADED msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Définit l’activation réussie de l’objet récepteur du fournisseur de consommateur d’événements.   |
| [**\_WMICONSUMERPROVIDERSINKUNLOADED msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Définit la désactivation réussie de l’objet récepteur du fournisseur de consommateur d’événements. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

Dépannage WMI
</dt> <dt>

[Réception d’un événement WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
