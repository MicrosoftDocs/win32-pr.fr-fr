---
title: Formats de pixel
description: Formats de pixel
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL sur Windows, pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106536878"
---
# <a name="pixel-formats"></a><span data-ttu-id="39fff-104">Formats de pixel</span><span class="sxs-lookup"><span data-stu-id="39fff-104">Pixel Formats</span></span>

<span data-ttu-id="39fff-105">Un *format de pixel* spécifie plusieurs propriétés d’une surface de dessin OpenGL.</span><span class="sxs-lookup"><span data-stu-id="39fff-105">A *pixel format* specifies several properties of an OpenGL drawing surface.</span></span> <span data-ttu-id="39fff-106">Voici quelques-unes des propriétés spécifiées par un format de pixel :</span><span class="sxs-lookup"><span data-stu-id="39fff-106">Some of the properties specified by a pixel format are:</span></span>

-   <span data-ttu-id="39fff-107">Indique si la mémoire tampon de pixels est une mémoire tampon simple ou double.</span><span class="sxs-lookup"><span data-stu-id="39fff-107">Whether the pixel buffer is single- or double-buffered.</span></span>
-   <span data-ttu-id="39fff-108">Indique si les données de pixels sont dans le format RVBA ou index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="39fff-108">Whether the pixel data is in RGBA or color-index form.</span></span>
-   <span data-ttu-id="39fff-109">Nombre de bits utilisés pour stocker des données de couleur.</span><span class="sxs-lookup"><span data-stu-id="39fff-109">The number of bits used to store color data.</span></span>
-   <span data-ttu-id="39fff-110">Nombre de bits utilisés pour la mémoire tampon de profondeur (axe z).</span><span class="sxs-lookup"><span data-stu-id="39fff-110">The number of bits used for the depth (z-axis) buffer.</span></span>
-   <span data-ttu-id="39fff-111">Nombre de bits utilisés pour la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="39fff-111">The number of bits used for the stencil buffer.</span></span>
-   <span data-ttu-id="39fff-112">Nombre de plans de superposition et de Underlay.</span><span class="sxs-lookup"><span data-stu-id="39fff-112">The number of overlay and underlay planes.</span></span>
-   <span data-ttu-id="39fff-113">Différents masques de visibilité.</span><span class="sxs-lookup"><span data-stu-id="39fff-113">Various visibility masks.</span></span>

<span data-ttu-id="39fff-114">L’implémentation de OpenGL pour Windows par Microsoft utilise la structure de données [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pour transmettre les données au format de pixel.</span><span class="sxs-lookup"><span data-stu-id="39fff-114">Microsoft's implementation of OpenGL for Windows uses the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure to convey pixel format data.</span></span> <span data-ttu-id="39fff-115">Les membres de la structure spécifient les propriétés précédentes et plusieurs autres.</span><span class="sxs-lookup"><span data-stu-id="39fff-115">The structure's members specify the preceding properties and several others.</span></span>

<span data-ttu-id="39fff-116">Un contexte de périphérique donné peut prendre en charge plusieurs formats de pixel.</span><span class="sxs-lookup"><span data-stu-id="39fff-116">A given device context can support several pixel formats.</span></span> <span data-ttu-id="39fff-117">Windows identifie les formats de pixel qu’un contexte de périphérique prend en charge avec des valeurs d’index de base 1 consécutives (1, 2, 3, 4, etc.).</span><span class="sxs-lookup"><span data-stu-id="39fff-117">Windows identifies the pixel formats that a device context supports with consecutive one-based index values (1, 2, 3, 4, and so on).</span></span> <span data-ttu-id="39fff-118">Un contexte de périphérique peut avoir un seul format de pixel actuel, choisi dans le jeu de formats de pixel pris en charge.</span><span class="sxs-lookup"><span data-stu-id="39fff-118">A device context can have just one current pixel format, chosen from the set of pixel formats it supports.</span></span>

<span data-ttu-id="39fff-119">Chaque fenêtre a son propre format de pixel actuel dans OpenGL dans Windows.</span><span class="sxs-lookup"><span data-stu-id="39fff-119">Each window has its own current pixel format in OpenGL in Windows.</span></span> <span data-ttu-id="39fff-120">Cela signifie, par exemple, qu’une application peut afficher simultanément des fenêtres de couleurs RVBA et d’index de couleurs, ou des fenêtres OpenGL à une seule et deux mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="39fff-120">This means, for example, that an application can simultaneously display RGBA and color-index OpenGL windows, or single- and double-buffered OpenGL windows.</span></span> <span data-ttu-id="39fff-121">Cette fonctionnalité de format de pixel par fenêtre est limitée aux fenêtres OpenGL.</span><span class="sxs-lookup"><span data-stu-id="39fff-121">This per-window pixel format capability is limited to OpenGL windows.</span></span>

<span data-ttu-id="39fff-122">En général, vous obtenez un contexte de périphérique, définissez le format de pixel du contexte de périphérique, puis créez un contexte de rendu OpenGL adapté à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="39fff-122">Typically, you obtain a device context, set the device context's pixel format, and then create an OpenGL rendering context suitable for that device.</span></span>

> [!Note]  
> <span data-ttu-id="39fff-123">Vous définissez le format de pixel avant de créer un contexte de rendu, car le contexte de rendu hérite du format de pixel du contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="39fff-123">You set the pixel format before creating a rendering context because the rendering context inherits the device context's pixel format.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="39fff-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39fff-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39fff-125">Fonctions de format de pixel</span><span class="sxs-lookup"><span data-stu-id="39fff-125">Pixel Format Functions</span></span>](pixel-format-functions.md)
</dt> </dl>

 

 




