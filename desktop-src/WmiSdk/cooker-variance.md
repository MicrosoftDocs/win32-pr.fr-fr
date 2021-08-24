---
description: La formule de type de compteur de variance de cuiseur \_ fournit la variabilité qui utilise pour caractériser la dispersion d’un jeu d’observations brutes d’une propriété dans une \_ instance de PerfRawData Win32.
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2133592bc3652a2e36037d89d4b2f2de0d0709d0ee23818f503e5da3c93c1f1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131481"
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

 

 
