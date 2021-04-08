---
description: Le Fournisseur de données performances au format de performances élevées de WMI calcule les types de compteurs statistiques sur un nombre spécifié d’exemples de données de compteurs brutes.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Types de compteurs statistiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034839"
---
# <a name="statistical-counter-types"></a>Types de compteurs statistiques

Le [fournisseur de données performances au format](formatted-performance-data-provider.md) de performances élevées de WMI calcule les types de compteurs statistiques sur un nombre spécifié d’exemples de données de compteurs brutes. Les algorithmes pour les types de compteurs ne requièrent pas de propriétés timestamp ou Frequency héritées (telles que **timestamp \_ PerfTime** ou **Frequency \_ PerfTime**) requises par d’autres types de compteurs.

Au lieu de cela, les types de compteurs statistiques prennent en charge un **qualificateur** qui identifie le nombre d’exemples à utiliser. Un échantillon est collecté lorsque la méthode [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) est appelée pour l’objet de performance. Pour les scripts, utilisez la méthode [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) . Les données calculées contiennent le résultat du calcul effectué sur le nombre d’échantillons **SampleWindow** à partir de la propriété de données brutes. Les données brutes du calcul sont fournies par le nom de propriété spécifié dans le qualificateur de **compteur** .

Pour plus d’informations, consultez [obtention de données de performances statistiques](obtaining-statistical-performance-data.md) et [accès aux classes de performances préinstallées de WMI](accessing-wmi-preinstalled-performance-classes.md).



| @, Constante                    | Description                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [moyenne de cuiseur \_](cooker-average.md)   | Additionne les observations répétées d’une propriété dans une classe [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et divise la somme par le nombre d’observations.                              |
| [maximum de cuiseur \_](cooker-max.md)           | Plus grande valeur d’un ensemble d’observations d’une propriété dans une classe [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .                                                                    |
| [minimum de cuiseur \_](cooker-min.md)           | Plus petite valeur d’un ensemble d’observations d’une propriété dans une [**classe \_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .                                                                   |
| [plage de cuiseur \_](cooker-range.md)       | Différence entre les valeurs [minimale](cooker-min.md) et [maximale](cooker-max.md) pour un ensemble d’observations brutes d’une propriété dans une classe [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . |
| [VARIANCE de la cuiseur \_](cooker-variance.md) | Mesure de variabilité qui peut être utilisée pour caractériser la dispersion d’un jeu d’observations brutes d’une propriété dans une classe [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de compteurs de performance WMI](wmi-performance-counter-types.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> <dt>

[Actualisation des données WMI dans les scripts](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Accès aux données de performances dans le script](accessing-performance-data-in-script.md)
</dt> <dt>

[Accès aux données de performances en C++](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
