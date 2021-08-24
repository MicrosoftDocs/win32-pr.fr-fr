---
description: Gère les métriques pour les éléments managés.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: Classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5fd976abf5bce91ffbc5581e73f93c2a8422fcdcbe69fd70745511362e504d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694939"
---
# <a name="cim_metricservice-class"></a>\_Classe CIM MetricService

Gère les métriques pour les éléments managés.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a>Membres

La classe **CIM \_ MetricService** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **CIM \_ MetricService** possède ces méthodes.



| Méthode                                                                   | Description                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ControlMetrics**](cim-metricservice-controlmetrics.md)               | Active et désactive la collecte des métriques.<br/>                                                                                                                          |
| [**ControlMetricsByClass**](cim-metricservice-controlmetricsbyclass.md) | Active et désactive la collection de mesures pour une classe.<br/>                                                                                                              |
| [**ControlSampleTimes**](cim-metricservice-controlsampletimes.md)       | Spécifie quand les métriques sont collectées.<br/>                                                                                                                                     |
| [**GetMetricValues**](cim-metricservice-getmetricvalues.md)             | Récupère une liste filtrée de valeurs de métriques.<br/>                                                                                                                              |
| [**ShowMetrics**](cim-metricservice-showmetrics.md)                     | Indique si la collection de mesures est activée pour les éléments managés spécifiés, et indique les métriques qui sont disponibles pour la collection pour chaque élément managé.<br/> |
| [**ShowMetricsByClass**](cim-metricservice-showmetricsbyclass.md)       | Indique les métriques disponibles pour la collecte de toutes les instances d’une classe CIM.<br/>                                                                                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> </dl>

 

 




