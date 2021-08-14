---
description: Une application récupère les dimensions du rectangle englobant d’une région en appelant la fonction GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Récupération d’un rectangle englobant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b7182d7c8f48fa8629855849710a601db9f93fd7e9180f9024d798b5ce2ebe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886144"
---
# <a name="retrieving-a-bounding-rectangle"></a>Récupération d’un rectangle englobant

Une application récupère les dimensions du rectangle englobant d’une région en appelant la fonction [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) . Si la région est rectangulaire, **GetRgnBox** retourne les dimensions de la région. Si la région est elliptique, la fonction retourne les dimensions du plus petit rectangle qui peut être dessiné autour de l’ellipse. Les longs côtés du rectangle sont de la même longueur que l’axe principal de l’ellipse, et les côtés courts du rectangle sont de la même longueur que l’axe secondaire de l’ellipse. Si la région est polygonale, **GetRgnBox** retourne les dimensions du plus petit rectangle qui peut être dessiné autour du polygone entier.

 

 



