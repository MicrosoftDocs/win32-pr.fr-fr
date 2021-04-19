---
title: Événements SystemMonitor
description: La classe SystemMonitor a les événements suivants
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509776"
---
# <a name="systemmonitor-events"></a>Événements SystemMonitor

La classe [**systemmonitor**](systemmonitor.md) a les événements suivants :

-   [**OnCounterAdded**](systemmonitor-oncounteradded.md)
-   [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
-   [**OnCounterSelected**](-systemmonitor-oncounterselected.md)
-   [**OnDblClick**](-systemmonitor-ondblclick.md)
-   [**OnSampleCollected**](-systemmonitor-onsamplecollected.md)

> [!Note]  
> Vous devez retourner à partir du gestionnaire d’événements avant l’expiration de l' [**intervalle de mise à jour**](systemmonitor-updateinterval.md) ; dans le cas contraire, SYSMON affiche une boîte de message indiquant à l’utilisateur qu’il n’a pas pu échantillonner les valeurs de compteur pour l’intervalle de mise à jour précédent.

 

 

 




