---
description: Une application récupère les dimensions du rectangle englobant d’une région en appelant la fonction GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Récupération d’un rectangle englobant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754308"
---
# <a name="retrieving-a-bounding-rectangle"></a>Récupération d’un rectangle englobant

Une application récupère les dimensions du rectangle englobant d’une région en appelant la fonction [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) . Si la région est rectangulaire, **GetRgnBox** retourne les dimensions de la région. Si la région est elliptique, la fonction retourne les dimensions du plus petit rectangle qui peut être dessiné autour de l’ellipse. Les longs côtés du rectangle sont de la même longueur que l’axe principal de l’ellipse, et les côtés courts du rectangle sont de la même longueur que l’axe secondaire de l’ellipse. Si la région est polygonale, **GetRgnBox** retourne les dimensions du plus petit rectangle qui peut être dessiné autour du polygone entier.

 

 



