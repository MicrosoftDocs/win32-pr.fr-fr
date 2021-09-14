---
title: Gestion des modes et de l’exécution
description: Gestion des modes et de l’exécution
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, modes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233609"
---
# <a name="managing-modes-and-execution"></a>Gestion des modes et de l’exécution

L’effet de nombreuses fonctions OpenGL varie selon qu’un mode particulier est actif ou non. Les fonctions [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) définissent ces modes ; [**glIsEnabled**](glisenabled.md) détermine si un mode particulier est défini.

Vous pouvez contrôler l’exécution des fonctions OpenGL précédemment émises avec [**glFinish**](glfinish.md), ce qui force l’achèvement de toutes les fonctions, ou [**glFlush**](glflush.md), qui garantit que toutes ces fonctions seront terminées dans un laps de temps fini.

Dans une implémentation particulière de OpenGL, vous pouvez contrôler certains comportements avec des indications à l’aide de [**glHint**](glhint.md). Ces comportements sont la qualité de l’interpolation des coordonnées de couleur et de texture ; précision des calculs de brouillard ; et la qualité d’échantillonnage des points, des lignes ou des polygones avec anticrénelage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modes et référence d’exécution](modes-and-execution-reference.md)
</dt> </dl>

 

 




