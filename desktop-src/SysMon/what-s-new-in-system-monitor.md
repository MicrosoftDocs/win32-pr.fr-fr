---
title: Nouveautés du moniteur système
description: Le tableau suivant identifie les nouveautés de chaque version du moniteur système (SYSMON).
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2020
ms.locfileid: "104381620"
---
# <a name="whats-new-in-system-monitor"></a>Nouveautés du moniteur système

Le tableau suivant identifie les nouveautés de chaque version du moniteur système (SYSMON).



| Version     | Description des fonctionnalités                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version 3.7 | Cette version ajoute de nouveaux types de graphiques, la possibilité de sélectionner plusieurs compteurs, de récupérer des valeurs de compteur à partir d’un point sur le graphique, d’enregistrer les valeurs de compteur sous forme de graphique dans un fichier journal, et l’option permettant de faire défiler continuellement un graphique linéaire dans la fenêtre du graphique au lieu de s’habiller sur lui-même. Inclus dans Windows Server 2008 et Windows Vista.<br/> |



 

## <a name="version-37"></a>Version 3.7

Nouvelles propriétés et méthodes qui ont été ajoutées à [**CounterItem**](counteritem.md).

-   [**GetDataAt**](counteritem-getdataat.md)
-   [**Sélectionné**](counteritem-selected.md)
-   [**Parent**](counteritem-visible.md)
-   Plage de valeurs valides modifiées pour [ **CounterItem. Width**](counteritem-width.md)

Nouvelles propriétés et méthodes qui ont été ajoutées à [**systemmonitor**](systemmonitor.md).

-   [**BatchingLock**](systemmonitor-batchinglock.md)
-   [**ChartScroll**](systemmonitor-chartscroll.md)
-   [**ClearData**](systemmonitor-cleardata.md)
-   [**DataPointCount**](systemmonitor-datapointcount.md)
-   [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)
-   [**EnableToolTips**](systemmonitor-enabletooltips.md)
-   [**GetLogViewRange**](systemmonitor-getlogviewrange.md)
-   [**LoadSettings**](systemmonitor-loadsettings.md)
-   [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
-   [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
-   [**Rejournaliser**](systemmonitor-relog.md)
-   [**SaveAs**](systemmonitor-saveas.md)
-   [**ScaleToFit**](systemmonitor-scaletofit.md)
-   [**SetLogViewRange**](systemmonitor-setlogviewrange.md)
-   [**ShowTimeAxisLables**](systemmonitor-showtimeaxislabels.md)

Nouvelles énumérations qui ont été ajoutées.

-   [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [**SysmonFileType**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   De nouvelles valeurs de type d’affichage ont été ajoutées à [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)

 

 





