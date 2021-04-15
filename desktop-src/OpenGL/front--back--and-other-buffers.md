---
title: Mémoires tampons avant, arrière et autres
description: OpenGL stocke et manipule les données de pixels dans un trame.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL sur Windows, mémoires tampons
- framebuffers OpenGL
- mémoires tampons de couleur OpenGL
- mémoires tampons de profondeur OpenGL
- mémoires tampons d’accumulation OpenGL
- mémoires tampons de stencil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380075"
---
# <a name="front-back-and-other-buffers"></a><span data-ttu-id="a85a4-109">Mémoires tampons avant, arrière et autres</span><span class="sxs-lookup"><span data-stu-id="a85a4-109">Front, Back, and Other Buffers</span></span>

<span data-ttu-id="a85a4-110">OpenGL stocke et manipule les données de pixels dans un trame.</span><span class="sxs-lookup"><span data-stu-id="a85a4-110">OpenGL stores and manipulates pixel data in a framebuffer.</span></span> <span data-ttu-id="a85a4-111">Le trame se compose d’un ensemble de mémoires tampons logiques : couleur, profondeur, accumulation et mémoires tampons de stencil.</span><span class="sxs-lookup"><span data-stu-id="a85a4-111">The framebuffer consists of a set of logical buffers: color, depth, accumulation, and stencil buffers.</span></span> <span data-ttu-id="a85a4-112">La mémoire tampon de couleur est constituée d’un ensemble de mémoires tampons logiques ; Cet ensemble peut inclure l’avant-plan, le front-droit, l’arrière-plan, l’arrière-plan, le verso et un certain nombre de mémoires tampons auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="a85a4-112">The color buffer itself consists of a set of logical buffers; this set can include a front-left, a front-right, a back-left, a back-right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="a85a4-113">Un format de pixel particulier ou une implémentation OpenGL peut ne pas fournir toutes ces mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="a85a4-113">A particular pixel format or OpenGL implementation may not supply all of these buffers.</span></span> <span data-ttu-id="a85a4-114">Par exemple, la version actuelle de l’implémentation de OpenGL de Microsoft dans Windows ne prend pas en charge les images stéréoscopiques. par conséquent, un format de pixel ne peut pas avoir de mémoires tampons de couleur gauche et droite.</span><span class="sxs-lookup"><span data-stu-id="a85a4-114">For example, the current version of Microsoft's implementation of OpenGL in Windows does not support stereoscopic images, so a pixel format cannot have left and right color buffers.</span></span> <span data-ttu-id="a85a4-115">En outre, la version actuelle ne prend pas en charge les tampons auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="a85a4-115">In addition, the current version does not support auxiliary buffers.</span></span> <span data-ttu-id="a85a4-116">Pour plus d’informations sur les mémoires tampons OpenGL et les fonctions OpenGL qui fonctionnent sur elles, consultez le *Manuel de référence OpenGL* et le *Guide de programmation OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="a85a4-116">For more information on OpenGL buffers and the OpenGL functions that operate on them, see the *OpenGL Reference Manual* and the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="a85a4-117">L’implémentation de OpenGL par Microsoft dans Windows prend en charge la double mise en mémoire tampon des images.</span><span class="sxs-lookup"><span data-stu-id="a85a4-117">Microsoft's implementation of OpenGL in Windows supports double buffering of images.</span></span> <span data-ttu-id="a85a4-118">Il s’agit d’une technique dans laquelle une application dessine des pixels dans une mémoire tampon hors écran, puis, lorsque cette image est prête à être affichée, copie le contenu de la mémoire tampon hors écran dans une mémoire tampon à l’écran.</span><span class="sxs-lookup"><span data-stu-id="a85a4-118">This is a technique in which an application draws pixels to an off-screen buffer, and then, when that image is ready for display, copies the contents of the off-screen buffer to an on-screen buffer.</span></span> <span data-ttu-id="a85a4-119">La double mise en mémoire tampon permet de lisser les modifications d’image, ce qui est particulièrement important pour les images animées.</span><span class="sxs-lookup"><span data-stu-id="a85a4-119">Double buffering enables smooth image changes, which are especially important for animated images.</span></span>

<span data-ttu-id="a85a4-120">Deux mémoires tampons de couleur sont disponibles pour les applications qui utilisent la double mise en mémoire tampon : une mémoire tampon d’arrière-plan et une mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a85a4-120">Two color buffers are available to applications that use double buffering: a front buffer and a back buffer.</span></span> <span data-ttu-id="a85a4-121">Par défaut, les commandes de dessin sont dirigées vers la mémoire tampon d’arrière-plan (la mémoire tampon hors écran), tandis que la mémoire tampon d’avant est affichée à l’écran.</span><span class="sxs-lookup"><span data-stu-id="a85a4-121">By default, drawing commands are directed to the back buffer (the off-screen buffer), while the front buffer is displayed on the screen.</span></span> <span data-ttu-id="a85a4-122">Lorsque la mémoire tampon hors écran est prête à être affichée, vous appelez [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)et Windows copie le contenu de la mémoire tampon hors écran dans la mémoire tampon à l’écran.</span><span class="sxs-lookup"><span data-stu-id="a85a4-122">When the off-screen buffer is ready for display, you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers), and Windows copies the contents of the off-screen buffer to the on-screen buffer.</span></span>

<span data-ttu-id="a85a4-123">L’implémentation générique utilise une image bitmap indépendante du périphérique (DIB) comme mémoire tampon d’arrière-plan et l’écran s’affiche comme mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="a85a4-123">The generic implementation uses a device-independent bitmap (DIB) as the back buffer and the screen display as the front buffer.</span></span> <span data-ttu-id="a85a4-124">Les périphériques matériels et leurs pilotes peuvent utiliser des approches différentes.</span><span class="sxs-lookup"><span data-stu-id="a85a4-124">Hardware devices and their drivers may use different approaches.</span></span>

<span data-ttu-id="a85a4-125">La double mise en mémoire tampon est une propriété au format pixel.</span><span class="sxs-lookup"><span data-stu-id="a85a4-125">Double buffering is a pixel-format property.</span></span> <span data-ttu-id="a85a4-126">Pour demander une double mise en mémoire tampon pour un format de pixel, définissez l' \_ indicateur PFD DOUBLEBUFFER dans la structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) dans un appel à [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="a85a4-126">To request double buffering for a pixel format, set the PFD\_DOUBLEBUFFER flag in the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure in a call to [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

<span data-ttu-id="a85a4-127">La fonction principale OpenGL, [**glDrawBuffer**](gldrawbuffer.md), sélectionne des mémoires tampons pour l’écriture et l’effacement.</span><span class="sxs-lookup"><span data-stu-id="a85a4-127">The OpenGL core function, [**glDrawBuffer**](gldrawbuffer.md), selects buffers for writing and clearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a85a4-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a85a4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a85a4-129">Fonctions de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="a85a4-129">Buffer Functions</span></span>](buffer-functions.md)
</dt> </dl>

 

 




