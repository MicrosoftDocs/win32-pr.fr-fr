---
description: Les chemins d’accès sont définis à l’aide d’unités logiques et de transformations actuelles.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformations de chemins d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973519"
---
# <a name="transformations-of-paths"></a>Transformations de chemins d’accès

Les chemins d’accès sont définis à l’aide d’unités logiques et de transformations actuelles. (Si la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) a été appelée, les unités logiques sont des unités universelles ; sinon, les unités logiques sont des unités de page.) Une application peut utiliser des transformations universelles pour mettre à l’échelle, faire pivoter, incliner, traduire et refléter les lignes et les courbes de Bézier qui définissent un tracé.

> [!Note]  
> Une transformation universelle dans un crochet de chemin d’accès affecte uniquement les lignes et les courbes dessinées après la définition de la transformation. Elle n’a aucun effet sur les lignes et les courbes qui ont été dessinées avant d’être définies. Pour obtenir une description de la transformation universelle, consultez [espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md).

 

Une application peut également utiliser [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour détailler la forme du stylet utilisé pour définir le contour d’un tracé si le stylet est un stylet géométrique. Pour obtenir une description des plumes géométriques, consultez [stylets](pens.md).

 

 



