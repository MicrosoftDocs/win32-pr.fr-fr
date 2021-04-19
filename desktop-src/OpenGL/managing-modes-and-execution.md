---
title: Gestion des modes et de l’exécution
description: Gestion des modes et de l’exécution
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, modes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510605"
---
# <a name="managing-modes-and-execution"></a><span data-ttu-id="15066-104">Gestion des modes et de l’exécution</span><span class="sxs-lookup"><span data-stu-id="15066-104">Managing Modes and Execution</span></span>

<span data-ttu-id="15066-105">L’effet de nombreuses fonctions OpenGL varie selon qu’un mode particulier est actif ou non.</span><span class="sxs-lookup"><span data-stu-id="15066-105">The effect of many OpenGL functions depends on whether a particular mode is in effect.</span></span> <span data-ttu-id="15066-106">Les fonctions [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) définissent ces modes ; [**glIsEnabled**](glisenabled.md) détermine si un mode particulier est défini.</span><span class="sxs-lookup"><span data-stu-id="15066-106">The [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions set such modes; [**glIsEnabled**](glisenabled.md) determines whether a particular mode is set.</span></span>

<span data-ttu-id="15066-107">Vous pouvez contrôler l’exécution des fonctions OpenGL précédemment émises avec [**glFinish**](glfinish.md), ce qui force l’achèvement de toutes les fonctions, ou [**glFlush**](glflush.md), qui garantit que toutes ces fonctions seront terminées dans un laps de temps fini.</span><span class="sxs-lookup"><span data-stu-id="15066-107">You can control the execution of previously issued OpenGL functions with [**glFinish**](glfinish.md), which forces all such functions to finish, or [**glFlush**](glflush.md), which ensures that all such functions will be completed in a finite time.</span></span>

<span data-ttu-id="15066-108">Dans une implémentation particulière de OpenGL, vous pouvez contrôler certains comportements avec des indications à l’aide de [**glHint**](glhint.md).</span><span class="sxs-lookup"><span data-stu-id="15066-108">In a particular implementation of OpenGL, you may be able to control certain behaviors with hints by using [**glHint**](glhint.md).</span></span> <span data-ttu-id="15066-109">Ces comportements sont la qualité de l’interpolation des coordonnées de couleur et de texture ; précision des calculs de brouillard ; et la qualité d’échantillonnage des points, des lignes ou des polygones avec anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="15066-109">Such behaviors are the quality of color and texture coordinate interpolation; the accuracy of fog calculations; and the sampling quality of antialiased points, lines, or polygons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15066-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15066-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15066-111">Modes et référence d’exécution</span><span class="sxs-lookup"><span data-stu-id="15066-111">Modes and Execution Reference</span></span>](modes-and-execution-reference.md)
</dt> </dl>

 

 




