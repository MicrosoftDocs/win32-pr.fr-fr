---
title: Portage des contextes de périphérique et des formats de pixel
description: Portage des contextes de périphérique et des formats de pixel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- portage vers OpenGL, pixels
- Portage OpenGL, pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106531185"
---
# <a name="porting-device-contexts-and-pixel-formats"></a><span data-ttu-id="6d7ff-105">Portage des contextes de périphérique et des formats de pixel</span><span class="sxs-lookup"><span data-stu-id="6d7ff-105">Porting Device Contexts and Pixel Formats</span></span>

<span data-ttu-id="6d7ff-106">Chaque fenêtre de l’implémentation Microsoft d’OpenGL pour Windows a son propre format de pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-106">Each window in the Microsoft implementation of OpenGL for Windows has its own current pixel format.</span></span> <span data-ttu-id="6d7ff-107">Un format de pixel est défini par une structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="6d7ff-107">A pixel format is defined by a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure.</span></span> <span data-ttu-id="6d7ff-108">Étant donné que chaque fenêtre a son propre format de pixel, vous obtenez un contexte de périphérique, définissez le format de pixel du contexte de périphérique, puis créez un contexte de rendu OpenGL pour le contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-108">Because each window has its own pixel format, you obtain a device context, set the pixel format of the device context, and then create an OpenGL rendering context for the device context.</span></span> <span data-ttu-id="6d7ff-109">Le contexte de rendu utilise automatiquement le format de pixel de son contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-109">The rendering context automatically uses the pixel format of its device context.</span></span>

<span data-ttu-id="6d7ff-110">Le système de fenêtre X utilise également une structure de données, **XVisualInfo**, pour spécifier les propriétés des pixels dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-110">The X Window System also uses a data structure, **XVisualInfo**, to specify the properties of pixels in a window.</span></span> <span data-ttu-id="6d7ff-111">Les structures **XVisualInfo** contiennent une structure de données **visuelles** qui décrit comment les ressources de couleur sont utilisées dans un écran spécifique.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-111">**XVisualInfo** structures contain a **Visual** data structure that describes how color resources are used in a specific screen.</span></span>

<span data-ttu-id="6d7ff-112">Dans le système de fenêtre X, **XVisualInfo** est utilisé pour créer une fenêtre en définissant la fenêtre au format de pixel souhaité.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-112">In the X Window System, **XVisualInfo** is used to create a window by setting the window to the pixel format you want.</span></span> <span data-ttu-id="6d7ff-113">La structure retournée est utilisée pour créer la fenêtre et un contexte de rendu.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-113">The returned structure is used to create the window and a rendering context.</span></span> <span data-ttu-id="6d7ff-114">Dans Windows, vous créez d’abord une fenêtre et vous recevez un handle vers un contexte de périphérique (HDC) de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-114">In Windows, you first create a window and get a handle to a device context (HDC) of the window.</span></span> <span data-ttu-id="6d7ff-115">Le HDC est ensuite utilisé pour définir le format de pixel de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-115">The HDC is then used to set the pixel format for the window.</span></span> <span data-ttu-id="6d7ff-116">Le contexte de rendu utilise le format de pixel de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-116">The rendering context uses the pixel format of the window.</span></span>

<span data-ttu-id="6d7ff-117">Le tableau suivant compare les fonctions de système de fenêtres X et de GLX visuelles à leurs fonctions de format de pixel Windows équivalentes.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-117">The following table compares the X Window System and GLX visual functions with their equivalent Windows pixel format functions.</span></span>



| <span data-ttu-id="6d7ff-118">X fenêtre/GLX fonction visuelle</span><span class="sxs-lookup"><span data-stu-id="6d7ff-118">X window/GLX visual function</span></span>                                                                                     | <span data-ttu-id="6d7ff-119">Fonction de format de pixel Windows</span><span class="sxs-lookup"><span data-stu-id="6d7ff-119">Windows pixel format function</span></span>                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7ff-120">XVisualInfo \* **glXChooseVisual**(Display *\* dpy*, int *Screen*, int *\* attribList*)</span><span class="sxs-lookup"><span data-stu-id="6d7ff-120">XVisualInfo\***glXChooseVisual**( Display *\*dpy*,int *screen*,int *\*attribList*)</span></span>                               | <span data-ttu-id="6d7ff-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *HDC*, PIXELFORMATDESCRIPTOR *\* PPFD*)</span><span class="sxs-lookup"><span data-stu-id="6d7ff-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                                      |
| <span data-ttu-id="6d7ff-122">int **glXGetConfig**(Display *\* dpy* *\* , XVisualInfo,* int *\* attribList*, int *\* value*)</span><span class="sxs-lookup"><span data-stu-id="6d7ff-122">int **glXGetConfig**( Display *\*dpy*,XVisualInfo *\*vis*,int *\*attribList*,int *\*value*)</span></span>                      | <span data-ttu-id="6d7ff-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *HDC*, int *iPixelFormat*, uint *nBytes*, LPPIXELFORMATDESCRIPTOR *PPFD*)</span><span class="sxs-lookup"><span data-stu-id="6d7ff-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*,int *iPixelFormat*,UINT *nBytes*,LPPIXELFORMATDESCRIPTOR *ppfd*)</span></span> |
| <span data-ttu-id="6d7ff-124">XVisualInfo \* **XGetVisualInfo**(Display *\* dpy*, long *vinfo \_ Mask*, XVisualInfo *\* vinfo \_ temp*, int *\* nItems*)</span><span class="sxs-lookup"><span data-stu-id="6d7ff-124">XVisualInfo\***XGetVisualInfo**( Display *\*dpy*,long *vinfo\_mask*,XVisualInfo *\*vinfo\_templ*,int *\*nitems*)</span></span> | <span data-ttu-id="6d7ff-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="6d7ff-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)</span></span>                                                                           |
| <span data-ttu-id="6d7ff-126">Le *visuel* retourné par **glxChooseVisual** est utilisé lors de la création d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-126">The *visual* returned by **glxChooseVisual** is used when a window is created.</span></span>                                   | <span data-ttu-id="6d7ff-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *HDC*, int *iPixelFormat*, PIXELFORMATDESCRIPTOR *\* PPFD*)</span><span class="sxs-lookup"><span data-stu-id="6d7ff-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*,int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                        |



 

<span data-ttu-id="6d7ff-128">Les sections suivantes fournissent des exemples de fragments de code de format de pixel pour un programme système X Window et le même code une fois qu’il a été porté vers Windows.</span><span class="sxs-lookup"><span data-stu-id="6d7ff-128">The following sections give examples of pixel format code fragments for an X Window System program, and the same code after it has been ported to Windows.</span></span>

-   [<span data-ttu-id="6d7ff-129">Exemple de code de format de pixel GLX</span><span class="sxs-lookup"><span data-stu-id="6d7ff-129">GLX Pixel Format Code Sample</span></span>](glx-pixel-format-code-sample.md)
-   [<span data-ttu-id="6d7ff-130">Exemple de code de format de pixel Windows</span><span class="sxs-lookup"><span data-stu-id="6d7ff-130">Windows Pixel Format Code Sample</span></span>](win32-pixel-format-code-sample.md)

<span data-ttu-id="6d7ff-131">Pour plus d’informations sur les formats de pixel, consultez [formats de pixel](pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="6d7ff-131">For more information on pixel formats, see [Pixel Formats](pixel-formats.md).</span></span>

 

 




