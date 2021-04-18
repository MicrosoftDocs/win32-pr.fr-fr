---
description: L’API métriques Hyper-V définit les éléments de programmation suivants.
ms.assetid: 00235614-9FCB-4161-B03D-9D557050153B
title: Informations de référence sur l’API métriques Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd4945bd390d995378c290f846335371fead753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519045"
---
# <a name="hyper-v-metrics-api-reference"></a>Informations de référence sur l’API métriques Hyper-V

L’API métriques Hyper-V définit les éléments de programmation suivants.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                    | Description                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md)<br/> | Représente les aspects de définition d’une mesure dérivée d’une autre valeur de mesure.<br/>                                                                                                                                                                                                                             |
| [**MSVM \_ AggregationMetricValue**](msvm-aggregationmetricvalue.md)<br/>           | Représente la valeur d’instance d’une mesure définie par une instance de la classe [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) .<br/>                                                                                                                                                         |
| [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)<br/>               | Représente les aspects de définition d’une mesure.<br/>                                                                                                                                                                                                                                                                       |
| [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md)<br/>                         | Représente une valeur de métrique définie par une instance de la classe [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) .<br/>                                                                                                                                                                                       |
| [**MSVM \_ MetricCollectionDependency**](msvm-metriccollectiondependency.md)<br/>   | Représente l’association entre deux définitions de métriques ou deux valeurs de métriques.<br/>                                                                                                                                                                                                                                      |
| [**MSVM \_ MetricDefForME**](msvm-metricdefforme.md)<br/>                           | Définit l’association entre un [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md) et un [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) pour définir des mesures pour ce dernier. La définition des métriques est donnée au contexte par propriété ManagedElement, ce qui explique pourquoi la définition dépend de l’élément.<br/> |
| [**MSVM \_ MetricForME**](msvm-metricforme.md)<br/>                                 | Cette association lie un élément géré aux valeurs de mesure conservées pour celui-ci.<br/>                                                                                                                                                                                                                               |
| [**MSVM \_ MetricInstance**](msvm-metricinstance.md)<br/>                           | Représente une association d’objets de valeur de métrique à leurs définitions de métriques.<br/>                                                                                                                                                                                                                                    |
| [**MSVM \_ MetricService**](msvm-metricservice.md)<br/>                             | Offre la possibilité de gérer les métriques.<br/>                                                                                                                                                                                                                                                                              |
| [**MSVM \_ MetricServiceCapabilities**](msvm-metricservicecapabilities.md)<br/>     | Décrit les fonctionnalités de l’instance [**MSVM \_ MetricService**](msvm-metricservice.md) associée.<br/>                                                                                                                                                                                                             |
| [**MSVM \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md)<br/>       | Représente les paramètres pour le service de métrique. Les propriétés de cette classe ne peuvent pas être modifiées directement. Le client doit appeler la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) pour modifier l’une de ces propriétés.<br/>                                                              |



 

 

