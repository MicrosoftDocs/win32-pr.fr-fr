---
description: L’interface IInstallationProgress définit les propriétés suivantes.
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: Propriétés IInstallationProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c688694be4a791c8d3ec861cc66367ebf89922817076032527f5458e0645918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130511"
---
# <a name="iinstallationprogress-properties"></a>Propriétés IInstallationProgress

L’interface [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) définit les propriétés suivantes.



| Propriété                                                                                   | Description                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentUpdateIndex**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | Obtient une valeur d’index de base zéro qui spécifie la mise à jour en cours d’installation ou de désinstallation lorsque plusieurs mises à jour ont été sélectionnées. |
| [**CurrentUpdatePercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | Obtient la progression du processus d’installation ou de désinstallation de la mise à jour actuelle, sous forme de pourcentage.                                    |
| [**PourcentageAchevé**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | Obtient le pourcentage de progression de l’installation ou de la désinstallation globale.                                                   |



 

 

 



