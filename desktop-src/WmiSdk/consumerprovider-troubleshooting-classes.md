---
description: Le tableau suivant répertorie les classes d’événements qui sont générées par les opérations du fournisseur de consommateur d’événements.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Classes de dépannage ConsumerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536c23fb35ca6a4d2146cf87782768c51f37a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541221"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Classes de dépannage ConsumerProvider

Le tableau suivant répertorie les classes d’événements qui sont générées par les opérations du [*fournisseur de consommateur d’événements*](gloss-e.md) .

Vous pouvez vous abonner aux notifications [**\_ ProviderEvent msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) de la classe de base abstraite pour obtenir tous les événements suivants.



|                                                                                                 |                                                                                 |
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

 

 
