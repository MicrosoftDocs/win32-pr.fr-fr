---
title: Portage de contextes de rendu
description: Portage de contextes de rendu
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- contextes de rendu OpenGL, Portage
- OpenGL sur Windows, contextes de rendu
- portage vers OpenGL, contextes de rendu
- Portage OpenGL, contextes de rendu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380114"
---
# <a name="porting-rendering-contexts"></a><span data-ttu-id="1fa4c-107">Portage de contextes de rendu</span><span class="sxs-lookup"><span data-stu-id="1fa4c-107">Porting Rendering Contexts</span></span>

<span data-ttu-id="1fa4c-108">Le système de fenêtre X et Windows s’affichent dans les contextes de rendu.</span><span class="sxs-lookup"><span data-stu-id="1fa4c-108">The X Window System and Windows render through rendering contexts.</span></span> <span data-ttu-id="1fa4c-109">Six fonctions GLX gèrent les contextes de rendu et cinq d’entre elles ont une fonction Windows équivalente.</span><span class="sxs-lookup"><span data-stu-id="1fa4c-109">Six GLX functions manage rendering contexts and five of them have an equivalent Windows function.</span></span>

<span data-ttu-id="1fa4c-110">Le tableau suivant répertorie les fonctions de rendu GLX et leurs fonctions Windows équivalentes.</span><span class="sxs-lookup"><span data-stu-id="1fa4c-110">The following table lists the GLX rendering functions and their equivalent Windows functions.</span></span>



| <span data-ttu-id="1fa4c-111">GLX fonction de contexte de rendu</span><span class="sxs-lookup"><span data-stu-id="1fa4c-111">GLX rendering context function</span></span>                                                                            | <span data-ttu-id="1fa4c-112">Fonction de contexte de rendu Windows</span><span class="sxs-lookup"><span data-stu-id="1fa4c-112">Windows rendering context function</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="1fa4c-113">GLXContext **glXCopyContext**(Display *\* dpy*, GLXContext *src*, GLXContext *DST*, GLuint *Mask*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-113">GLXContext **glXCopyContext**( Display *\*dpy*,GLXContext *src*,GLXContext *dst*,GLuint *mask*)</span></span>            | <span data-ttu-id="1fa4c-114">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="1fa4c-114">Not applicable.</span></span>                                                         |
| <span data-ttu-id="1fa4c-115">GLXContext **glXCreateContext**(Display *\* dpy* *\* , XVisualInfo,* GLXContext *shareList*, bool *direct*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-115">GLXContext **glXCreateContext**( Display *\*dpy*,XVisualInfo *\*vis*,GLXContext *shareList*,Bool *direct*)</span></span> | <span data-ttu-id="1fa4c-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)</span></span>          |
| <span data-ttu-id="1fa4c-117">void **glXDeleteContext**(Display *\* dpy*, GLXContext *CTX*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-117">void **glXDeleteContext**( Display *\*dpy*,GLXContext *ctx*)</span></span>                                              | <span data-ttu-id="1fa4c-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(HGLRC *HGLRC*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)</span></span>       |
| <span data-ttu-id="1fa4c-119">GLXContext **glXGetCurrentContext**(*void*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-119">GLXContext **glXGetCurrentContext**(*void*)</span></span>                                                               | <span data-ttu-id="1fa4c-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)</span></span>      |
| <span data-ttu-id="1fa4c-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span></span>                                                             | <span data-ttu-id="1fa4c-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)</span></span>                  |
| <span data-ttu-id="1fa4c-123">Bool **glXMakeCurrent**(Display *\* dpy*, GLXDrawable *Draw*, GLXContext *CTX*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-123">Bool **glXMakeCurrent**( Display *\*dpy*,GLXDrawable *draw*,GLXContext *ctx*)</span></span>                              | <span data-ttu-id="1fa4c-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *HDC*, HGLRC *HGLRC*)</span><span class="sxs-lookup"><span data-stu-id="1fa4c-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*,HGLRC *hglrc*)</span></span> |



 

<span data-ttu-id="1fa4c-125">Les types de retour et d’autres types ont des noms différents dans le système de fenêtres X que dans Windows.</span><span class="sxs-lookup"><span data-stu-id="1fa4c-125">Return types and other types have different names in the X Window System than in Windows.</span></span> <span data-ttu-id="1fa4c-126">Vous pouvez rechercher des occurrences de GLXContext pour vous aider à trouver des parties de votre code qui doivent être portées.</span><span class="sxs-lookup"><span data-stu-id="1fa4c-126">You can search for occurrences of GLXContext to help find parts of your code that need to be ported.</span></span>

<span data-ttu-id="1fa4c-127">Les sections suivantes comparent le rendu des exemples de code de contexte dans un programme système X Window et le même code une fois qu’il a été porté vers Windows.</span><span class="sxs-lookup"><span data-stu-id="1fa4c-127">The following sections compare rendering context code samples in an X Window System program and the same code after it has been ported to Windows.</span></span>

<span data-ttu-id="1fa4c-128">Pour plus d’informations sur le rendu des contextes, consultez [contextes de rendu](rendering-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="1fa4c-128">For more information on rendering contexts, see [Rendering Contexts](rendering-contexts.md).</span></span>

 

 




