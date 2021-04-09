---
description: La formule de type de compteur de variance de cuiseur \_ fournit la variabilité qui utilise pour caractériser la dispersion d’un jeu d’observations brutes d’une propriété dans une \_ instance de PerfRawData Win32.
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034312"
---
# <a name="cooker_variance"></a>VARIANCE de la cuiseur \_

La formule de type de compteur de variance de cuiseur \_ fournit la variabilité qui utilise pour caractériser la dispersion d’un jeu d’observations brutes d’une propriété dans une instance de [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . La variance est calculée en divisant la somme du carré de l’écart par la moyenne de chaque compteur par le nombre de compteurs. En d’autres termes, la variance est la moyenne des écarts au carré de la moyenne pour chaque compteur. Ce type de compteur est défini uniquement dans WMI et n’est pas disponible pour les technologies d’analyse des performances, telles que les [compteurs de performance Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

Pour plus d’informations sur la formule de type de compteur, consultez [types de compteurs](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).

Pour plus d’informations sur les fournisseurs et les scripts à hautes performances, consultez [types de compteurs de performance WMI](wmi-performance-counter-types.md).

## <a name="example-code"></a>Exemple de code

Pour obtenir des exemples de code, consultez [obtention de données de performances statistiques](obtaining-statistical-performance-data.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de compteurs statistiques](statistical-counter-types.md)
</dt> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> </dl>

 

 
