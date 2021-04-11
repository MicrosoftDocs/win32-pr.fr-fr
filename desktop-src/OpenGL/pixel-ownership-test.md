---
title: Test de propriété des pixels
description: Le test de propriété des pixels détermine si le contexte OpenGL actuel est propriétaire du pixel dans le trame correspondant à un fragment particulier.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Pipeline de traitement OpenGL, test de propriété de pixel
- test de propriété des pixels OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310337"
---
# <a name="pixel-ownership-test"></a><span data-ttu-id="ab895-105">Test de propriété des pixels</span><span class="sxs-lookup"><span data-stu-id="ab895-105">Pixel Ownership Test</span></span>

<span data-ttu-id="ab895-106">Le test de propriété des pixels détermine si le contexte OpenGL actuel est propriétaire du pixel dans le trame correspondant à un fragment particulier.</span><span class="sxs-lookup"><span data-stu-id="ab895-106">The pixel ownership test determines whether the current OpenGL context owns the pixel in the framebuffer corresponding to a particular fragment.</span></span> <span data-ttu-id="ab895-107">Si c’est le cas, le fragment passe au test suivant.</span><span class="sxs-lookup"><span data-stu-id="ab895-107">If so, the fragment proceeds to the next test.</span></span> <span data-ttu-id="ab895-108">Si ce n’est pas le cas, le système de fenêtre détermine si le fragment est ignoré ou si d’autres opérations de fragment seront effectuées avec ce fragment.</span><span class="sxs-lookup"><span data-stu-id="ab895-108">If not, the window system determines whether the fragment is discarded or whether any further fragment operations will be performed with that fragment.</span></span> <span data-ttu-id="ab895-109">Avec ce test, le système de fenêtre contrôle le comportement quand, par exemple, une fenêtre OpenGL est masquée.</span><span class="sxs-lookup"><span data-stu-id="ab895-109">With this test, the window system controls behavior when, for example, an OpenGL window is obscured.</span></span>

 

 




