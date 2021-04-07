---
description: Les types de compteurs de l’algorithme du minuteur de précision obtiennent des lectures plus précises que les minuteries du système.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Types de compteurs de l’algorithme du minuteur de précision
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759771"
---
# <a name="precision-timer-algorithm-counter-types"></a>Types de compteurs de l’algorithme du minuteur de précision

Les types de compteurs de l’algorithme du minuteur de précision obtiennent des lectures plus précises que les minuteries du système. Le service qui fournit les données fournit également un horodatage, qui élimine les erreurs qui peuvent se produire en raison de la durée de petite et de variable qui s’écoule entre la capture de l’horodateur système et la collecte des données à partir de la DLL de performance. Cet horodateur de base pour les timers de précision est une \_ propriété Timestamp de précision de performance \_ , qui doit suivre immédiatement la \_ propriété Timer de précision de performance \_ .



| @, Constante                                                                                         | Description                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Performances \_ \_ \_ Minuteur système de précision](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))décimal 541525248<br/> | Similaire au \_ minuteur de compteur de performances \_ , sauf qu’il utilise une base de temps définie par compteur au lieu de l’horodateur système.             |
| [Performances \_ \_ \_ Minuteur de précision 100](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))% décimal 542573824<br/>  | Semblable au \_ \_ minuteur 100NSEC perf, sauf qu’il utilise une base de temps définie par le compteur de 100 ns au lieu de l’horodateur de la 100 ns du système. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de compteurs de performance WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

