---
description: Pour consommer des données de compteur, consultez consommation des données de compteur.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Using Performance Counters
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 18bb017a34fb23188c20e81bce28c171c50dcb4d43cd52d458e92be99b7d03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033209"
---
# <a name="using-performance-counters"></a>Using Performance Counters

Les **consommateurs** de compteurs de performances sont des composants logiciels qui collectent et utilisent des données de compteurs de performances. Exemples de consommateurs fournis par Microsoft : analyseur de performances (perfmon.exe), moniteur de ressource (resmon.exe), gestionnaire de journaux (logman.exe) et typeperf.exe. Les composants logiciels tiers peuvent également collecter des données de performances via des API de collecte de performances ou via des classes de compteur de performances WMI.

Les **fournisseurs** de compteurs de performances sont des composants logiciels qui publient des données de compteur de performances. Les compteurs de performances peuvent être fournis par les composants du système d’exploitation, les pilotes de périphériques et les services. de nombreux compteurs de performances sont fournis dans le cadre du système d’exploitation Windows. Des compteurs supplémentaires peuvent être fournis par des composants logiciels tiers via les API du fournisseur de compteurs de performance.

- Utilisez les [outils de compteur de performance](performance-counters-tools.md) lorsque vous souhaitez collecter ou afficher les données de compteur à partir d’un système.
- Utilisez les [API de consommateur de compteur de performance](consuming-counter-data.md) lorsque vous souhaitez écrire un programme qui collecte des données de compteur à partir du système local.
- Utilisez les [classes de compteur de performances WMI](/windows/desktop/WmiSdk/monitoring-performance-data) lorsque vous souhaitez collecter des données de compteur à partir d’un système local ou distant à l’aide de WMI.
- Utilisez les [API du fournisseur de compteurs de performance](providing-counter-data.md) lorsque vous souhaitez publier des données de compteur de performance à partir de votre composant logiciel.

## <a name="see-also"></a>Voir aussi

[À propos des compteurs de performance](about-performance-counters.md)

[Référence des compteurs de performance](performance-counters-reference.md)
