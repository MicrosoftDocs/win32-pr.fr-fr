---
title: Rendu d’image
description: Rendu d’image
ms.assetid: de87f288-f1bd-471c-b594-e9dbde3cff0a
keywords:
- DrawDib, rendu d’image
- DrawDib, dessin de DIB
- DrawDibDraw fonction)
- DrawDibGetBuffer fonction)
- DrawDibUpdate fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e0d3f4d770a3acc290273b14ec14ff4b6efa30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029780"
---
# <a name="image-rendering"></a><span data-ttu-id="eb5bf-108">Rendu d’image</span><span class="sxs-lookup"><span data-stu-id="eb5bf-108">Image Rendering</span></span>

<span data-ttu-id="eb5bf-109">Après avoir appelé [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) pour créer un contrôleur de périphérique DrawDib (voir [opérations DrawDib](drawdib-operations.md)), vous pouvez dessiner un DIB à l’écran à l’aide de la fonction [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .</span><span class="sxs-lookup"><span data-stu-id="eb5bf-109">After you call [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) to create a DrawDib DC (see [DrawDib Operations](drawdib-operations.md)), you can draw a DIB to the screen by using the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function.</span></span> <span data-ttu-id="eb5bf-110">**DrawDibDraw** détrame les bitmaps de couleur vraies lors de leur affichage avec des adaptateurs d’affichage 8 bits.</span><span class="sxs-lookup"><span data-stu-id="eb5bf-110">**DrawDibDraw** dithers true-color bitmaps when displaying them with 8-bit display adapters.</span></span>

<span data-ttu-id="eb5bf-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) prend également en charge les compresseurs vidéo de manière transparente lors de l’affichage des images bitmap compressées.</span><span class="sxs-lookup"><span data-stu-id="eb5bf-111">[**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) also supports video compressors transparently when displaying compressed bitmaps.</span></span> <span data-ttu-id="eb5bf-112">Vous pouvez accéder à la mémoire tampon qui contient l’image décompressée à l’aide de la fonction [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) .</span><span class="sxs-lookup"><span data-stu-id="eb5bf-112">You can access the buffer that contains the decompressed image by using the [**DrawDibGetBuffer**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetbuffer) function.</span></span> <span data-ttu-id="eb5bf-113">**DrawDibGetBuffer** retourne la **valeur null** lors du dessin d’une bitmap non compressée.</span><span class="sxs-lookup"><span data-stu-id="eb5bf-113">**DrawDibGetBuffer** returns **NULL** when drawing an uncompressed bitmap.</span></span> <span data-ttu-id="eb5bf-114">Vous devez préparer votre application pour gérer les bitmaps compressées et non compressées.</span><span class="sxs-lookup"><span data-stu-id="eb5bf-114">You should prepare your application to handle compressed and uncompressed bitmaps.</span></span>

<span data-ttu-id="eb5bf-115">Vous pouvez actualiser une image ou une partie d’une image affichée par votre application à l’aide de la macro [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) .</span><span class="sxs-lookup"><span data-stu-id="eb5bf-115">You can refresh an image or a portion of an image displayed by your application by using the [**DrawDibUpdate**](/windows/desktop/api/Vfw/nf-vfw-drawdibupdate) macro.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb5bf-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb5bf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb5bf-117">À propos des fonctions DrawDib</span><span class="sxs-lookup"><span data-stu-id="eb5bf-117">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




