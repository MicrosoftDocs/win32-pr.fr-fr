---
title: Noms des fonctions OpenGL
description: De nombreuses fonctions OpenGL sont des variations les unes des autres, qui se différencient principalement dans les types de données de leurs arguments.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, noms de fonctions
- noms de fonctions OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673270"
---
# <a name="opengl-function-names"></a><span data-ttu-id="ad28c-105">Noms des fonctions OpenGL</span><span class="sxs-lookup"><span data-stu-id="ad28c-105">OpenGL Function Names</span></span>

<span data-ttu-id="ad28c-106">De nombreuses fonctions OpenGL sont des variations les unes des autres, qui se différencient principalement dans les types de données de leurs arguments.</span><span class="sxs-lookup"><span data-stu-id="ad28c-106">Many OpenGL functions are variations of each other, differing mostly in the data types of their arguments.</span></span> <span data-ttu-id="ad28c-107">Certaines fonctions diffèrent dans le nombre d’arguments associés et si ces arguments peuvent être spécifiés en tant que vecteurs ou s’ils doivent être spécifiés séparément dans une liste.</span><span class="sxs-lookup"><span data-stu-id="ad28c-107">Some functions differ in the number of related arguments and whether those arguments can be specified as a vector or must be specified separately in a list.</span></span> <span data-ttu-id="ad28c-108">Par exemple, si vous utilisez la fonction **glVertex2f** , vous devez fournir des coordonnées x et y en tant que nombres à virgule flottante 32 bits ; avec **glVertex3sv**, vous devez fournir un tableau de trois valeurs entières courtes (16 bits) pour x, y et z.</span><span class="sxs-lookup"><span data-stu-id="ad28c-108">For example, if you use the **glVertex2f** function, you need to supply x- and y-coordinates as 32-bit floating-point numbers; with **glVertex3sv**, you must supply an array of three short (16-bit) integer values for x, y, and z.</span></span> <span data-ttu-id="ad28c-109">Seul le nom de base de la fonction est utilisé dans les rubriques qui suivent.</span><span class="sxs-lookup"><span data-stu-id="ad28c-109">Only the base name of the function is used in the topics that follow.</span></span> <span data-ttu-id="ad28c-110">Un astérisque indique que le nom de fonction réel peut être plus grand que ce qui est indiqué.</span><span class="sxs-lookup"><span data-stu-id="ad28c-110">An asterisk indicates that there may be more to the actual function name than is shown.</span></span> <span data-ttu-id="ad28c-111">Par exemple, [glVertex \*](glvertex-functions.md) correspond à toutes les variantes de la fonction que vous utilisez pour spécifier des vertex : **glVertex2d**, **glVertex2f**, **glVertex2i**, etc.</span><span class="sxs-lookup"><span data-stu-id="ad28c-111">For example, [glVertex\*](glvertex-functions.md) stands for all the variations of the function you use to specify vertices: **glVertex2d**, **glVertex2f**, **glVertex2i**, and so on.</span></span>

<span data-ttu-id="ad28c-112">L’effet d’une fonction OpenGL peut varier selon que certains modes sont activés ou non.</span><span class="sxs-lookup"><span data-stu-id="ad28c-112">The effect of an OpenGL function can vary depending on whether certain modes are enabled.</span></span> <span data-ttu-id="ad28c-113">Par exemple, vous devez activer l’éclairage si les fonctions liées à l’éclairage produisent un objet correctement éclairé.</span><span class="sxs-lookup"><span data-stu-id="ad28c-113">For example, you need to enable lighting if the lighting-related functions are to produce a properly lit object.</span></span> <span data-ttu-id="ad28c-114">Pour activer un mode particulier, utilisez la fonction [**glEnable**](glenable.md) et fournissez la constante appropriée pour identifier le mode (par exemple, l’éclairage du GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="ad28c-114">To enable a particular mode, use the [**glEnable**](glenable.md) function and supply the appropriate constant to identify the mode (for example, GL\_LIGHTING).</span></span> <span data-ttu-id="ad28c-115">Pour désactiver un mode, utilisez [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="ad28c-115">To disable a mode, use [**glDisable**](gldisable.md).</span></span> <span data-ttu-id="ad28c-116">Consultez **glEnable** pour obtenir la liste complète des modes qui peuvent être activés.</span><span class="sxs-lookup"><span data-stu-id="ad28c-116">See **glEnable** for a complete list of the modes that can be enabled.</span></span>

 

 




