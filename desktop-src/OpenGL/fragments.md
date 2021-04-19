---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, fragments
- Pipeline de traitement OpenGL, fragments
- fragments OpenGL
- framebuffers, fragments modifiant les pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513472"
---
# <a name="fragments"></a><span data-ttu-id="f5cd8-107">Fragments</span><span class="sxs-lookup"><span data-stu-id="f5cd8-107">Fragments</span></span>

<span data-ttu-id="f5cd8-108">Un fragment produit par rastérisation modifie le pixel correspondant dans le trame uniquement s’il réussit les tests suivants :</span><span class="sxs-lookup"><span data-stu-id="f5cd8-108">A fragment produced by rasterization modifies the corresponding pixel in the framebuffer only if it passes the following tests:</span></span>

-   [<span data-ttu-id="f5cd8-109">Test de propriété des pixels</span><span class="sxs-lookup"><span data-stu-id="f5cd8-109">Pixel ownership test</span></span>](pixel-ownership-test.md)
-   [<span data-ttu-id="f5cd8-110">Test de ciseaux</span><span class="sxs-lookup"><span data-stu-id="f5cd8-110">Scissor test</span></span>](scissor-test.md)
-   [<span data-ttu-id="f5cd8-111">Test alpha</span><span class="sxs-lookup"><span data-stu-id="f5cd8-111">Alpha test</span></span>](alpha-test.md)
-   [<span data-ttu-id="f5cd8-112">Test de stencil</span><span class="sxs-lookup"><span data-stu-id="f5cd8-112">Stencil test</span></span>](stencil-test.md)
-   [<span data-ttu-id="f5cd8-113">Test de la mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="f5cd8-113">Depth-buffer test</span></span>](depth-buffer-test.md)

<span data-ttu-id="f5cd8-114">En cas de réussite, les données du fragment peuvent remplacer les valeurs trame existantes, ou vous pouvez les combiner avec des données existantes dans le trame, en fonction de l’état de certains modes.</span><span class="sxs-lookup"><span data-stu-id="f5cd8-114">If it passes, the fragment's data can replace the existing framebuffer values, or you can combine it with existing data in the framebuffer, depending on the state of certain modes.</span></span> <span data-ttu-id="f5cd8-115">Vous pouvez combiner le fragment avec les données de trame de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="f5cd8-115">You can combine the fragment with data in the framebuffer by:</span></span>

-   [<span data-ttu-id="f5cd8-116">Fusion</span><span class="sxs-lookup"><span data-stu-id="f5cd8-116">Blending</span></span>](blending.md)
-   [<span data-ttu-id="f5cd8-117">Tramage</span><span class="sxs-lookup"><span data-stu-id="f5cd8-117">Dithering</span></span>](dithering.md)
-   [<span data-ttu-id="f5cd8-118">Opérations logiques</span><span class="sxs-lookup"><span data-stu-id="f5cd8-118">Logical operations</span></span>](logical-operations.md)

 

 




