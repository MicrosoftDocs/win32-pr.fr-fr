---
title: Opérations trame
description: Pour sélectionner la mémoire tampon dans laquelle les valeurs de couleur sont écrites, utilisez glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Pipeline de traitement OpenGL, opérations trame
- framebuffers, opérations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507122"
---
# <a name="framebuffer-operations"></a><span data-ttu-id="75ae3-105">Opérations trame</span><span class="sxs-lookup"><span data-stu-id="75ae3-105">Framebuffer Operations</span></span>

<span data-ttu-id="75ae3-106">Pour sélectionner la mémoire tampon dans laquelle les valeurs de couleur sont écrites, utilisez [**glDrawBuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="75ae3-106">To select the buffer into which color values are written, use [**glDrawBuffer**](gldrawbuffer.md).</span></span> <span data-ttu-id="75ae3-107">Vous utilisez quatre fonctions différentes pour masquer l’écriture de bits à chacun des framebuffers logiques une fois toutes les opérations par fragment effectuées :</span><span class="sxs-lookup"><span data-stu-id="75ae3-107">You use four different functions to mask the writing of bits to each of the logical framebuffers after all per-fragment operations have been performed:</span></span>

-   [<span data-ttu-id="75ae3-108">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="75ae3-108">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="75ae3-109">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="75ae3-109">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="75ae3-110">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="75ae3-110">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="75ae3-111">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="75ae3-111">**glStencilMask**</span></span>](glstencilmask.md)

<span data-ttu-id="75ae3-112">La fonction [**glAccum**](glaccum.md) contrôle l’opération de la mémoire tampon d’accumulation.</span><span class="sxs-lookup"><span data-stu-id="75ae3-112">The [**glAccum**](glaccum.md) function controls the operation of the accumulation buffer.</span></span> <span data-ttu-id="75ae3-113">Enfin, [**glClear**](glclear.md) définit chaque pixel dans un sous-ensemble spécifié des mémoires tampons sur la valeur spécifiée par [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)ou [**glClearAccum**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="75ae3-113">Finally, [**glClear**](glclear.md) sets every pixel in a specified subset of the buffers to the value specified with [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), or [**glClearAccum**](glclearaccum.md).</span></span>

 

 




