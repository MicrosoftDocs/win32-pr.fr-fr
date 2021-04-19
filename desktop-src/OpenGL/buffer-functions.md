---
title: Fonctions de mémoire tampon
description: Pour copier le contenu d’une mémoire tampon hors écran dans une mémoire tampon à l’écran, appelez SwapBuffers.
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- WGL, mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106529518"
---
# <a name="buffer-functions"></a><span data-ttu-id="126cc-104">Fonctions de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="126cc-104">Buffer Functions</span></span>

<span data-ttu-id="126cc-105">Pour copier le contenu d’une mémoire tampon hors écran dans une mémoire tampon à l’écran, appelez [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="126cc-105">To copy the contents of an off-screen buffer to an on-screen buffer, call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="126cc-106">La fonction **SwapBuffers** prend un handle vers un contexte de périphérique (Device Context).</span><span class="sxs-lookup"><span data-stu-id="126cc-106">The **SwapBuffers** function takes a handle to a device context.</span></span> <span data-ttu-id="126cc-107">Le format de pixel actuel du contexte de périphérique spécifié doit inclure une mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="126cc-107">The current pixel format for the specified device context must include a back buffer.</span></span> <span data-ttu-id="126cc-108">Par défaut, la mémoire tampon d’arrière-plan est hors écran et la mémoire tampon d’affichage est à l’écran.</span><span class="sxs-lookup"><span data-stu-id="126cc-108">By default, the back buffer is off-screen, and the front buffer is on-screen.</span></span>

> [!Note]  
> <span data-ttu-id="126cc-109">La fonction **SwapBuffers** n’échange pas vraiment le contenu des deux mémoires tampons, mais copie le contenu d’une mémoire tampon vers une autre.</span><span class="sxs-lookup"><span data-stu-id="126cc-109">The **SwapBuffers** function does not really swap the contents of the two buffers, but rather copies the contents of one buffer to another.</span></span> <span data-ttu-id="126cc-110">Le contenu de la mémoire tampon hors écran n’est pas défini après un appel à **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="126cc-110">The contents of the off-screen buffer are undefined after a call to **SwapBuffers**.</span></span> <span data-ttu-id="126cc-111">Ainsi, le résultat de deux appels consécutifs à **SwapBuffers** n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="126cc-111">Thus, the result of two consecutive calls to **SwapBuffers** is undefined.</span></span>

 

<span data-ttu-id="126cc-112">L’illustration suivante montre comment le contenu des mémoires tampons est copié lors de l’appel de **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="126cc-112">The following illustration shows how the contents of the buffers are copied when calling **SwapBuffers**.</span></span>

![Diagramme montrant les résultats non définis des appels consécutifs à la fonction SwapBuffers.](images/opengl00.png)

<span data-ttu-id="126cc-114">Plusieurs fonctions OpenGL Core gèrent également les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="126cc-114">Several OpenGL core functions also manage buffers.</span></span> <span data-ttu-id="126cc-115">La fonction [**glDrawBuffer**](gldrawbuffer.md) est celle qui est la plus pertinente pour la double mise en mémoire tampon ; Il spécifie les trame ou les mémoires tampons dans lesquelles OpenGL crée des dessins.</span><span class="sxs-lookup"><span data-stu-id="126cc-115">The [**glDrawBuffer**](gldrawbuffer.md) function is the one most relevant to double buffering; it specifies the framebuffer or buffers that OpenGL draws into.</span></span>

<span data-ttu-id="126cc-116">Les fonctions suivantes affectent également les mémoires tampons :</span><span class="sxs-lookup"><span data-stu-id="126cc-116">The following functions also affect buffers:</span></span>

-   [<span data-ttu-id="126cc-117">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="126cc-117">**glReadBuffer**</span></span>](glreadbuffer.md)
-   [<span data-ttu-id="126cc-118">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="126cc-118">**glReadPixels**</span></span>](glreadpixels.md)
-   [<span data-ttu-id="126cc-119">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="126cc-119">**glCopyPixels**</span></span>](glcopypixels.md)
-   [<span data-ttu-id="126cc-120">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="126cc-120">**glAccum**</span></span>](glaccum.md)
-   [<span data-ttu-id="126cc-121">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="126cc-121">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="126cc-122">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="126cc-122">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="126cc-123">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="126cc-123">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="126cc-124">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="126cc-124">**glStencilMask**</span></span>](glstencilmask.md)
-   [<span data-ttu-id="126cc-125">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="126cc-125">**glClearAccum**</span></span>](glclearaccum.md)
-   [<span data-ttu-id="126cc-126">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="126cc-126">**glClearColor**</span></span>](glclearcolor.md)
-   [<span data-ttu-id="126cc-127">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="126cc-127">**glClearDepth**</span></span>](glcleardepth.md)
-   [<span data-ttu-id="126cc-128">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="126cc-128">**glClearIndex**</span></span>](glclearindex.md)
-   [<span data-ttu-id="126cc-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="126cc-129">**glClearStencil**</span></span>](glclearstencil.md)

 

 




