---
description: Les chemins d’accès sont définis à l’aide d’unités logiques et de transformations actuelles.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformations de chemins d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7561cc1544a49555eaad4d58cf06d29a4763b6cd40528452c68cea551c99af34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888999"
---
# <a name="transformations-of-paths"></a>Transformations de chemins d’accès

Les chemins d’accès sont définis à l’aide d’unités logiques et de transformations actuelles. (Si la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) a été appelée, les unités logiques sont des unités universelles ; sinon, les unités logiques sont des unités de page.) Une application peut utiliser des transformations universelles pour mettre à l’échelle, faire pivoter, incliner, traduire et refléter les lignes et les courbes de Bézier qui définissent un tracé.

> [!Note]  
> Une transformation universelle dans un crochet de chemin d’accès affecte uniquement les lignes et les courbes dessinées après la définition de la transformation. Elle n’a aucun effet sur les lignes et les courbes qui ont été dessinées avant d’être définies. Pour obtenir une description de la transformation universelle, consultez [espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md).

 

Une application peut également utiliser [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) pour détailler la forme du stylet utilisé pour définir le contour d’un tracé si le stylet est un stylet géométrique. Pour obtenir une description des plumes géométriques, consultez [stylets](pens.md).

 

 



