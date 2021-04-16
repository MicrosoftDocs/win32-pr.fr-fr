---
description: Le format des données récupérées par la fonction RegQueryValueEx commence par une structure d’en-tête de longueur fixe, un \_ bloc de données perf \_ .
ms.assetid: a68fa617-834c-4ad9-b922-fac3a648ad75
title: Format des données de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88029634594843a50fd6010993eb6517dce831f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565552"
---
# <a name="performance-data-format"></a>Format des données de performances

Le format des données récupérées par la fonction [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) commence par une structure d’en-tête de longueur fixe, un [**\_ \_ bloc de données perf**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block). La structure de **\_ \_ bloc de données perf** décrit le système et les données de performances. La structure de **\_ \_ bloc de données perf** est suivie d’un nombre variable d’éléments de données d’objet de longueur variable. L’en-tête de chaque élément objet contient le décalage de l’élément objet suivant dans la liste. Le diagramme suivant illustre la structure de données de performances de base.

![structure des données de performances](images/perfdata.png)

Il existe deux formats pour les éléments de données d’objet : un qui prend en charge plusieurs instances et l’autre qui ne prend pas en charge plusieurs instances.

Chaque bloc d’éléments de données d’objet contient une structure de [**\_ \_ type d’objet perf**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) , qui décrit les données de performances de l’objet. La structure du **\_ \_ type d’objet perf** est suivie d’une liste de structures de [**définition de \_ compteur \_ de performances**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) , une pour chaque compteur défini pour l’objet. Pour un objet avec une seule instance, la liste des structures de **\_ \_ définition de compteur de performances** est suivie d’une structure de [**\_ \_ bloc de compteur de performances**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) unique, suivie des données de compteur. Chaque structure de **\_ \_ définition de compteur de performances** contient le décalage à partir du début de la structure de **\_ \_ bloc de compteur de performances** vers les données de compteur correspondantes. Le diagramme suivant illustre la structure d’un objet de performance qui ne prend pas en charge plusieurs instances.

![structure de l’objet de performance qui ne prend pas en charge plusieurs instances](images/perfnoinst.png)

Pour un type d’objet qui prend en charge plusieurs instances, la liste des structures de [**\_ \_ définition de compteur de performances**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) est suivie d’une liste de blocs d’informations d’instance (une pour chaque instance). Chaque bloc d’informations d’instance contient une structure de [**\_ \_ définition d’instance perf**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition) , le nom de l’instance et une structure de [**bloc de \_ compteur \_ de performances**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block) . Le diagramme suivant illustre la structure d’un objet de performance qui prend en charge deux instances.

![structure d’un objet de performance qui prend en charge deux instances](images/perfinst.png)

Pour obtenir un exemple qui utilise les décalages, consultez [affichage des noms d’objet, d’instance et de compteur](displaying-object-instance-and-counter-names.md).

 

 
