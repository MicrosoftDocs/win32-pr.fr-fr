---
title: Palettes et gestionnaire de palette
description: Le gestionnaire de palette Windows, qui fait partie du GDI, cible spécifiquement des adaptateurs d’affichage 8 bits avec une palette de 256 de couleurs.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL sur Windows, gestionnaire de palette
- OpenGL sur Windows, palettes matérielles
- Gestionnaire de palette OpenGL
- palettes de matériel OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510404"
---
# <a name="palettes-and-the-palette-manager"></a><span data-ttu-id="164b6-107">Palettes et gestionnaire de palette</span><span class="sxs-lookup"><span data-stu-id="164b6-107">Palettes and the Palette Manager</span></span>

<span data-ttu-id="164b6-108">Le gestionnaire de palette Windows, qui fait partie du GDI, cible spécifiquement des adaptateurs d’affichage 8 bits avec une *palette* de 256 de couleurs.</span><span class="sxs-lookup"><span data-stu-id="164b6-108">The Windows Palette Manager, which is part of the GDI, specifically targets 8-bit display adapters with a *hardware palette* of 256 color entries.</span></span> <span data-ttu-id="164b6-109">Les pixels de l’écran sont stockés sous la forme d’un index 8 bits dans la palette matérielle.</span><span class="sxs-lookup"><span data-stu-id="164b6-109">Pixels on the screen are stored as an 8-bit index into the hardware palette.</span></span> <span data-ttu-id="164b6-110">Chaque entrée de la palette matérielle définit généralement une couleur de 24 bits (8 en rouge, vert et bleu).</span><span class="sxs-lookup"><span data-stu-id="164b6-110">Each entry in the hardware palette usually defines a 24-bit color (8 each of red, green, and blue).</span></span>

<span data-ttu-id="164b6-111">Le gestionnaire de palettes gère une *palette système* qui est une copie de la palette matérielle.</span><span class="sxs-lookup"><span data-stu-id="164b6-111">The Palette Manager maintains a *system palette* that is a copy of the hardware palette.</span></span> <span data-ttu-id="164b6-112">La palette système est divisée en deux sections : 20 couleurs réservées et les couleurs 236 restantes, que vous pouvez définir à l’aide du gestionnaire de palette.</span><span class="sxs-lookup"><span data-stu-id="164b6-112">The system palette is divided into two sections: 20 reserved colors and the remaining 236 colors, which you can set using the Palette Manager.</span></span>

<span data-ttu-id="164b6-113">Une *palette logique* par défaut de 20 couleurs est sélectionnée et réalisée dans un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="164b6-113">A default 20-color *logical palette* is selected and realized into a device context.</span></span> <span data-ttu-id="164b6-114">Vous pouvez créer et utiliser une nouvelle palette logique.</span><span class="sxs-lookup"><span data-stu-id="164b6-114">You can create and use a new logical palette.</span></span> <span data-ttu-id="164b6-115">Pour modifier la palette du système, sélectionnez et réalisez la palette logique que vous avez créée.</span><span class="sxs-lookup"><span data-stu-id="164b6-115">To change the system palette, select and realize the logical palette you created.</span></span>

<span data-ttu-id="164b6-116">Vous allez probablement créer une palette logique pour spécifier les couleurs que vous souhaitez afficher dans votre application OpenGL.</span><span class="sxs-lookup"><span data-stu-id="164b6-116">You'll probably create a logical palette to specify the colors you want displayed in your OpenGL application.</span></span> <span data-ttu-id="164b6-117">À l’aide de certains appels GDI, vous pouvez remplacer temporairement la plus grande partie de la palette système par une palette logique.</span><span class="sxs-lookup"><span data-stu-id="164b6-117">Using certain GDI calls, you can temporarily replace most of the system palette with a logical palette.</span></span> <span data-ttu-id="164b6-118">À l’aide d’une palette logique, vous pouvez définir des couleurs de pixels pour le GDI à l’aide du mode RVBA ou de l’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="164b6-118">Using a logical palette, you can define pixel colors for the GDI using either the RGBA or the color-index mode.</span></span> <span data-ttu-id="164b6-119">La taille maximale d’une palette logique est de 256 couleurs pour les appareils 8 bits et de 4 096 couleurs sur un appareil de couleur vraies (16, 24 et 32 bits).</span><span class="sxs-lookup"><span data-stu-id="164b6-119">The maximum size of a logical palette is 256 colors for 8-bit devices and 4,096 colors on a true-color device (16, 24, and 32 bits).</span></span>

<span data-ttu-id="164b6-120">Pour plus d’informations sur les modes RVBA et index des couleurs, consultez [mode RVBA et gestion de la palette Windows](rgba-mode-and-windows-palette-management.md) et [modes de couleurs OpenGL et gestion de la palette Windows](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="164b6-120">For more information on the RGBA and color-index modes, see [RGBA Mode and Windows Palette Management](rgba-mode-and-windows-palette-management.md) and [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

 

 




