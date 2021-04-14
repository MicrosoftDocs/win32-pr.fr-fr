---
title: Pixels
description: Les fragments sont convertis en pixels dans le trame.
ms.assetid: 1925b455-ae6e-4f95-899c-4bcac641f549
keywords:
- OpenGL, pixels
- Pipeline de traitement OpenGL, pixels
- pixels OpenGL
- framebuffers, conversion de fragments en pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6660452930683943da780fad3aeb001e531711
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380366"
---
# <a name="pixels"></a><span data-ttu-id="76ffb-107">Pixels</span><span class="sxs-lookup"><span data-stu-id="76ffb-107">Pixels</span></span>

<span data-ttu-id="76ffb-108">Les fragments sont convertis en pixels dans le trame.</span><span class="sxs-lookup"><span data-stu-id="76ffb-108">Fragments are converted to pixels in the framebuffer.</span></span> <span data-ttu-id="76ffb-109">Le trame est organisé en un ensemble de mémoires tampons logiques de la couleur, de la profondeur, du stencil et des mémoires tampons d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="76ffb-109">The framebuffer is organized into a set of logical buffers the color, depth, stencil, and accumulation buffers.</span></span> <span data-ttu-id="76ffb-110">La mémoire tampon de couleur elle-même se compose d’un avant gauche, du premier plan, du verso, de l’arrière-plan et d’un certain nombre de mémoires tampons auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="76ffb-110">The color buffer itself consists of a front left, front right, back left, back right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="76ffb-111">Vous pouvez émettre des fonctions pour contrôler ces mémoires tampons et les lire ou les copier directement à partir de celles-ci.</span><span class="sxs-lookup"><span data-stu-id="76ffb-111">You can issue functions to control these buffers, and directly read or copy pixels from them.</span></span> <span data-ttu-id="76ffb-112">(Notez que le contexte OpenGL particulier que vous utilisez peut ne pas fournir toutes ces mémoires tampons.)</span><span class="sxs-lookup"><span data-stu-id="76ffb-112">(Note that the particular OpenGL context you're using may not provide all these buffers.)</span></span>

-   [<span data-ttu-id="76ffb-113">Opérations trame</span><span class="sxs-lookup"><span data-stu-id="76ffb-113">Framebuffer Operations</span></span>](framebuffer-operations.md)
-   [<span data-ttu-id="76ffb-114">Lecture ou copie de pixels</span><span class="sxs-lookup"><span data-stu-id="76ffb-114">Reading or Copying Pixels</span></span>](reading-or-copying-pixels.md)
-   [<span data-ttu-id="76ffb-115">Référence en pixels</span><span class="sxs-lookup"><span data-stu-id="76ffb-115">Pixels Reference</span></span>](pixels-reference.md)

 

 




