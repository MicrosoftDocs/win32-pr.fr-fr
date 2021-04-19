---
description: Pour consommer des données de compteur, consultez consommation des données de compteur.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Using Performance Counters
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531701"
---
# <a name="using-performance-counters"></a>Using Performance Counters

Les **consommateurs** de compteurs de performances sont des composants logiciels qui collectent et utilisent des données de compteurs de performances. Exemples de consommateurs fournis par Microsoft : analyseur de performances (perfmon.exe), moniteur de ressource (resmon.exe), gestionnaire de journaux (logman.exe) et typeperf.exe. Les composants logiciels tiers peuvent également collecter des données de performances via des API de collecte de performances ou via des classes de compteur de performances WMI.

Les **fournisseurs** de compteurs de performances sont des composants logiciels qui publient des données de compteur de performances. Les compteurs de performances peuvent être fournis par les composants du système d’exploitation, les pilotes de périphériques et les services. De nombreux compteurs de performances sont fournis dans le cadre du système d’exploitation Windows. Des compteurs supplémentaires peuvent être fournis par des composants logiciels tiers via les API du fournisseur de compteurs de performance.

- Utilisez les [outils de compteur de performance](performance-counters-tools.md) lorsque vous souhaitez collecter ou afficher les données de compteur à partir d’un système.
- Utilisez les [API de consommateur de compteur de performance](consuming-counter-data.md) lorsque vous souhaitez écrire un programme qui collecte des données de compteur à partir du système local.
- Utilisez les [classes de compteur de performances WMI](/windows/desktop/WmiSdk/monitoring-performance-data) lorsque vous souhaitez collecter des données de compteur à partir d’un système local ou distant à l’aide de WMI.
- Utilisez les [API du fournisseur de compteurs de performance](providing-counter-data.md) lorsque vous souhaitez publier des données de compteur de performance à partir de votre composant logiciel.

## <a name="see-also"></a>Voir aussi

[À propos des compteurs de performance](about-performance-counters.md)

[Référence des compteurs de performance](performance-counters-reference.md)
