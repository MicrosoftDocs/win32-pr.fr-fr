---
description: Le mode d’adresse de texture clamp, identifié par le \_ membre D3DTADDRESS clamp du type énuméré D3DTEXTUREADDRESS, amène Direct3D à fixer vos coordonnées de texture à la \[ plage 0,0 1,0 \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Mode d’adresse de texture clamp (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529098"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a><span data-ttu-id="07e3b-103">Mode d’adresse de texture clamp (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="07e3b-103">Clamp Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="07e3b-104">Le mode d’adresse de texture clamp, identifié par le \_ membre D3DTADDRESS clamp du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , amène Direct3D à fixer vos coordonnées de texture à \[ la plage 0,0 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="07e3b-104">The clamp texture address mode, identified by the D3DTADDRESS\_CLAMP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to clamp your texture coordinates to the \[0.0, 1.0\] range.</span></span> <span data-ttu-id="07e3b-105">Autrement dit, il applique la texture une seule fois, puis frotte la couleur des pixels du bord.</span><span class="sxs-lookup"><span data-stu-id="07e3b-105">That is, it applies the texture once, then smears the color of edge pixels.</span></span> <span data-ttu-id="07e3b-106">Supposons, par exemple, que votre application crée une primitive carrée et assigne des coordonnées de texture (0.0, 0.0), (0.0, 3.0), (3.0, 3.0) et (3,0, 0.0) aux sommets de la primitive.</span><span class="sxs-lookup"><span data-stu-id="07e3b-106">For example, suppose that your application creates a square primitive and assigns texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0) to the primitive's vertices.</span></span> <span data-ttu-id="07e3b-107">Si vous définissez le mode d’adressage de la texture sur D3DTADDRESS \_ clamp, la texture est appliquée une seule fois.</span><span class="sxs-lookup"><span data-stu-id="07e3b-107">Setting the texture addressing mode to D3DTADDRESS\_CLAMP results in the texture being applied once.</span></span> <span data-ttu-id="07e3b-108">Les couleurs de pixel en haut des colonnes et la fin des lignes sont étendues respectivement en haut et à droite de la primitive.</span><span class="sxs-lookup"><span data-stu-id="07e3b-108">The pixel colors at the top of the columns and the end of the rows are extended to the top and right of the primitive respectively.</span></span>

<span data-ttu-id="07e3b-109">L’illustration suivante montre une texture débloquée.</span><span class="sxs-lookup"><span data-stu-id="07e3b-109">The following illustration shows a clamped texture.</span></span>

![illustration d’une texture et d’une texture débloquée](images/clamp.png)

## <a name="related-topics"></a><span data-ttu-id="07e3b-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07e3b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07e3b-112">Modes d’adressage de la texture</span><span class="sxs-lookup"><span data-stu-id="07e3b-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
