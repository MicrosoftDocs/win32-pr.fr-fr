---
title: Rendre un contexte de rendu non actuel
description: Pour détacher un contexte de rendu d’un thread, rendez-le non actuel. Pour ce faire, vous pouvez appeler la fonction wglMakeCurrent avec les paramètres définis sur NULL. Voici un exemple de cette tâche simple.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL sur Windows, contextes de rendu
- contextes de rendu OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309797"
---
# <a name="making-a-rendering-context-not-current"></a><span data-ttu-id="b9014-107">Rendre un contexte de rendu non actuel</span><span class="sxs-lookup"><span data-stu-id="b9014-107">Making a Rendering Context Not Current</span></span>

<span data-ttu-id="b9014-108">Pour détacher un contexte de rendu d’un thread, rendez-le non actuel.</span><span class="sxs-lookup"><span data-stu-id="b9014-108">To detach a rendering context from a thread, make it not current.</span></span> <span data-ttu-id="b9014-109">Pour ce faire, vous pouvez appeler la fonction [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) avec les paramètres définis sur **null**.</span><span class="sxs-lookup"><span data-stu-id="b9014-109">You can do this by calling the [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) function with the parameters set to **NULL**.</span></span> <span data-ttu-id="b9014-110">Voici un exemple de cette tâche simple.</span><span class="sxs-lookup"><span data-stu-id="b9014-110">The following is a sample of this simple task.</span></span>

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




