---
description: Messages de qualité
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Messages de qualité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15224e147d363a6cf3f3a55971d35a3d6596d95f07b9897ab1f258cc7febad48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747699"
---
# <a name="quality-messages"></a>Messages de qualité

Les messages de qualité sont définis avec la structure de [**qualité**](/windows/win32/api/strmif/ns-strmif-quality) . Cette structure contient les membres suivants :

-   **Tapez :** Défini par l’énumération [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) ; soit famine, ce qui indique que le filtre reçoit trop peu de données, ou inondation, indiquant que le filtre reçoit trop de données.
-   **Proportion :** Ajustement demandé dans le débit de données, à partir d’une ligne de base de 1000. Par exemple, 750 indique 75% et 1500 indique 150%.
-   **Tard :** Temps de référence indiquant la date à laquelle l’exemple le plus récent est arrivé. La valeur est négative si l’exemple est arrivé tôt.
-   **Horodateur :** Horodatage de l’exemple le plus récent.

Par exemple, supposons qu’un échantillon avec un horodatage de 240 millisecondes (MS) atteigne le convertisseur à 280 ms, temps de flux. Le convertisseur crée un message de qualité de type famine. L’exemple a atteint 40 ms en retard, donc le membre **tardif** est 400000. (Toutes les durées de référence sont en unités de 100 nanosecondes.) Le membre **timestamp** est 2,4 millions.

Pour le membre de **proportion** , le convertisseur peut utiliser une moyenne en cours d’exécution pour calculer la valeur. Des exemples ont peut-être été arrivés à l’heure et cet exemple est une anomalie. Dans ce cas, le convertisseur peut demander uniquement une petite correction. En revanche, si les échantillons sont constamment en retard, le convertisseur peut demander une plus grande correction.

Le contrôle de qualité est géré par le biais de l’interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) . Il contient deux méthodes.

-   [**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): envoie un message de qualité.
-   [**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): spécifie un gestionnaire de qualité personnalisé.

Un objet qui implémente **IQualityControl** reçoit des messages de qualité par le biais de sa méthode **Notify** . Il peut soit gérer le message, soit le transmettre à un autre objet. Si l’application appelle la méthode **SetSink** de l’objet, l’objet doit déléguer le contrôle de qualité au gestionnaire de qualité spécifié.

 

 



