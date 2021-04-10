---
title: Extension des fonctions OpenGL
description: La bibliothèque OpenGL prend en charge plusieurs implémentations de ses fonctions.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL sur Windows, fonctions d’extension
- fonctions d’extension OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940226"
---
# <a name="extending-opengl-functions"></a><span data-ttu-id="e6cdc-105">Extension des fonctions OpenGL</span><span class="sxs-lookup"><span data-stu-id="e6cdc-105">Extending OpenGL Functions</span></span>

<span data-ttu-id="e6cdc-106">La bibliothèque OpenGL prend en charge plusieurs implémentations de ses fonctions.</span><span class="sxs-lookup"><span data-stu-id="e6cdc-106">The OpenGL library supports multiple implementations of its functions.</span></span> <span data-ttu-id="e6cdc-107">Les fonctions d’extension prises en charge dans un contexte de rendu ne sont pas nécessairement prises en charge dans un contexte de rendu différent.</span><span class="sxs-lookup"><span data-stu-id="e6cdc-107">Extension functions supported in one rendering context aren't necessarily supported in a different rendering context.</span></span> <span data-ttu-id="e6cdc-108">Pour un contexte de rendu donné dans une application à l’aide de fonctions d’extension, utilisez uniquement les adresses de fonction retournées par la fonction [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e6cdc-108">For a given rendering context in an application using extension functions, use only the function addresses returned by the [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) function.</span></span>

 

 




