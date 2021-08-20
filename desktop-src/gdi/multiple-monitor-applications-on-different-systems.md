---
description: Pour que votre application monitoraware fonctionne à la fois sur les systèmes avec et sans prise en charge de plusieurs moniteurs, liez votre application à multimon. h.
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: Plusieurs applications de surveillance sur différents systèmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c597261063f49b6e6856576e3528698291348afb2b8478d854a824b92d2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037717"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>Plusieurs applications de surveillance sur différents systèmes

Pour que votre application monitoraware fonctionne à la fois sur les systèmes avec et sans prise en charge de plusieurs moniteurs, liez votre application à multimon. h. Vous devez également définir \_ \_ des stubs de compilation MULTIMON dans un seul fichier C. Si le système ne prend pas en charge plusieurs analyses, cela retourne les valeurs par défaut de [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) , et les fonctions d’analyse multiples agissent comme s’il n’y a qu’un seul affichage. Sur plusieurs systèmes d’analyse, votre application fonctionnera normalement.

Étant donné que les coordonnées négatives peuvent se produire facilement dans un système multimoniteur, vous devez récupérer les coordonnées qui sont compressées dans le lParam à l’aide des macros **obtenir \_ X \_ lParam** et **obtenir \_ Y \_ lParam** .

N’utilisez pas de coordonnées négatives ou de coordonnées supérieures à SM \_ CXSCREEN et SM \_ CYSCREEN pour masquer une fenêtre. les Windows qui utilisent ces limites pour masquer peuvent apparaître sur un autre moniteur. De même, n’utilisez pas ces limites pour laisser une fenêtre visible, car cela peut entraîner l’alignement d’une fenêtre sur l’écran principal. Il est préférable de réexaminer les applications existantes à la recherche de ces problèmes. Toutefois, vous pouvez réduire les problèmes dans les applications existantes en exécutant l’application sur le moniteur principal ou en conservant le moniteur principal dans le coin supérieur gauche de l’écran virtuel.

Notez que \_ les SM CXMAXTRACK et SM \_ CYMAXTRACK sont définis pour le bureau, et pas seulement pour une seule analyse. il peut être nécessaire de redéfinir les Windows utilisant ces limites.

Une fenêtre parente ou associée peut ne pas se trouver sur le même moniteur qu’une fenêtre enfant. Pour localiser le moniteur d’une fenêtre, les applications doivent utiliser la fonction [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) .

Pour que l’écran de veille s’affiche sur toutes les analyses, liez-le à la dernière version de scrnsave. lib. Dans le cas contraire, l’écran de veille peut uniquement apparaître sur le moniteur principal et ne pas toucher aux autres moniteurs. Les économiseurs d’écran liés à la dernière version de scrnsave. lib fonctionnent sur les systèmes à écran unique et multiple. Pour avoir un autre écran de veille sur chaque moniteur, utilisez les fonctions d’analyse multiples pour gérer séparément chaque analyse.

Les périphériques d’entrée qui fournissent des coordonnées au système en coordonnées absolues, telles que les tablettes, ont leur entrée de curseur limitée à l’analyse principale. Pour basculer entre les moniteurs, consultez les instructions du fabricant d’ordinateurs OEM.

Pour mapper l’entrée de la souris qui est envoyée en coordonnées absolues à l’écran virtuel entier, utilisez la structure [**d’entrée**](/windows/win32/api/winuser/ns-winuser-input) avec MOUSEEVENTF \_ Absolute et MOUSEEVENTF \_ VIRTUALDESKTOP.

La fonction [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) fonctionne bien pour les systèmes à plusieurs écrans. Toutefois, les fonctions [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt), [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt), [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)et [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) échouent si les contextes de périphérique source et de destination sont différents.

 

 
