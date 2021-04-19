---
title: Impression d’une image OpenGL
description: Vous pouvez imprimer les images OpenGL rendues dans les sous-fichiers améliorés.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL sur Windows, impression
- impression d’images OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511708"
---
# <a name="printing-an-opengl-image"></a><span data-ttu-id="97641-105">Impression d’une image OpenGL</span><span class="sxs-lookup"><span data-stu-id="97641-105">Printing an OpenGL Image</span></span>

<span data-ttu-id="97641-106">Vous pouvez imprimer les images OpenGL rendues dans les sous-fichiers améliorés.</span><span class="sxs-lookup"><span data-stu-id="97641-106">You can print OpenGL images rendered in enhanced metafiles.</span></span> <span data-ttu-id="97641-107">Lorsque vous effectuez un rendu sur un appareil d’imprimante (HDC), celui-ci doit être sauvegardé par un spouleur de métafichiers.</span><span class="sxs-lookup"><span data-stu-id="97641-107">When you render to a printer device (HDC) it must be backed by a metafile spooler.</span></span> <span data-ttu-id="97641-108">OpenGL utilise de la mémoire pour la profondeur, la couleur et d’autres mémoires tampons pour stocker la sortie graphique sur une imprimante.</span><span class="sxs-lookup"><span data-stu-id="97641-108">OpenGL uses memory for depth, color, and other buffers to store graphics output to a printer.</span></span> <span data-ttu-id="97641-109">Étant donné que la résolution d’imprimante par défaut nécessite une quantité importante de mémoire pour stocker la sortie graphique, l’impression d’une image OpenGL peut nécessiter plus de mémoire que ce qui est disponible dans le système.</span><span class="sxs-lookup"><span data-stu-id="97641-109">Because typical printer resolution requires a significant amount of memory to store the graphics output, printing an OpenGL image might require more memory than is available in the system.</span></span> <span data-ttu-id="97641-110">Pour surmonter cette limitation, l’implémentation actuelle d’OpenGL imprime les graphiques OpenGL en bandes.</span><span class="sxs-lookup"><span data-stu-id="97641-110">To overcome this limitation, the current implementation of OpenGL prints OpenGL graphics in bands.</span></span> <span data-ttu-id="97641-111">Toutefois, cela augmente le temps nécessaire à l’impression des images OpenGL.</span><span class="sxs-lookup"><span data-stu-id="97641-111">However, this increases the time it takes to print OpenGL images.</span></span>

<span data-ttu-id="97641-112">Avant d’imprimer une image OpenGL, vous devez appeler la fonction [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) pour terminer l’initialisation d’un contexte de périphérique d’impression (DC).</span><span class="sxs-lookup"><span data-stu-id="97641-112">Before you print an OpenGL image, you must call the [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) function to complete the initialization of a printer device context (DC).</span></span> <span data-ttu-id="97641-113">Après avoir appelé **StartDoc**, vous pouvez créer des contextes de rendu (HGLRC) à rendre sur le périphérique d’impression.</span><span class="sxs-lookup"><span data-stu-id="97641-113">After calling **StartDoc**, you can create rendering contexts (HGLRC) to render to the printer device.</span></span> <span data-ttu-id="97641-114">Si vous créez des contextes de rendu avant d’appeler **StartDoc**, il n’existe aucun moyen de déterminer si un métafichier est mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="97641-114">If you create rendering contexts before calling **StartDoc**, there is no way to determine whether a metafile is spooled.</span></span>

<span data-ttu-id="97641-115">L’exemple de code suivant montre comment imprimer une image OpenGL :</span><span class="sxs-lookup"><span data-stu-id="97641-115">The following code sample shows how to print an OpenGL image:</span></span>

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

<span data-ttu-id="97641-116">Pour plus d’informations sur l’utilisation des métafichiers, consultez [opérations de métafichier améliorées](/windows/desktop/gdi/enhanced-metafile-operations).</span><span class="sxs-lookup"><span data-stu-id="97641-116">For more information on using metafiles, see [Enhanced Metafile Operations](/windows/desktop/gdi/enhanced-metafile-operations).</span></span>

 

 