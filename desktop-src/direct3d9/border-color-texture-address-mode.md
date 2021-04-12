---
description: Le mode d’adresse de texture de couleur de la bordure, identifié par le \_ membre de bordure D3DTADDRESS du type énuméré D3DTEXTUREADDRESS, fait en sorte que Direct3D utilise une couleur arbitraire, appelée couleur de bordure, pour toutes les coordonnées de texture situées en dehors de la plage comprise entre 0,0 et 1,0 inclus.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Mode d’adresse de la texture de couleur de la bordure (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42b18d88f3b9305d0602e43a9528357a9397d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393167"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a><span data-ttu-id="f109c-103">Mode d’adresse de la texture de couleur de la bordure (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f109c-103">Border Color Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="f109c-104">Le mode d’adresse de texture de couleur de la bordure, identifié par le \_ membre de bordure D3DTADDRESS du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , fait en sorte que Direct3D utilise une couleur arbitraire, appelée couleur de bordure, pour toutes les coordonnées de texture situées en dehors de la plage comprise entre 0,0 et 1,0 inclus.</span><span class="sxs-lookup"><span data-stu-id="f109c-104">The border color texture address mode, identified by the D3DTADDRESS\_BORDER member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to use an arbitrary color, known as the border color, for any texture coordinates outside the range of 0.0 through 1.0, inclusive.</span></span>

<span data-ttu-id="f109c-105">Dans l’illustration suivante, l’application spécifie que la texture doit être appliquée à la primitive à l’aide d’une bordure rouge.</span><span class="sxs-lookup"><span data-stu-id="f109c-105">In the following illustration, the application specifies that the texture be applied to the primitive using a red border.</span></span>

![illustration d’une texture et d’une texture avec bordure rouge](images/border.png)

<span data-ttu-id="f109c-107">Les applications définissent la couleur de la bordure en appelant [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="f109c-107">Applications set the border color by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="f109c-108">Définissez le premier paramètre pour l’appel à l’identificateur de l’étape de texture souhaitée, le deuxième paramètre à la valeur d’état de l' \_ étape D3DSAMP BORDERCOLOR et le troisième paramètre à la nouvelle couleur de bordure RVBA.</span><span class="sxs-lookup"><span data-stu-id="f109c-108">Set the first parameter for the call to the desired texture stage identifier, the second parameter to the D3DSAMP\_BORDERCOLOR stage state value, and the third parameter to the new RGBA border color.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f109c-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f109c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f109c-110">Modes d’adressage de la texture</span><span class="sxs-lookup"><span data-stu-id="f109c-110">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
