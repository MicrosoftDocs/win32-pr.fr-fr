---
description: De nombreuses applications C++ effacent le tampon de profondeur avant de restituer chaque nouveau Frame.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Effacement des tampons de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ad415b5c92e62da4f64eb590a0e202ffa3e0c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544579"
---
# <a name="clearing-depth-buffers-direct3d-9"></a><span data-ttu-id="2816f-103">Effacement des tampons de profondeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2816f-103">Clearing Depth Buffers (Direct3D 9)</span></span>

<span data-ttu-id="2816f-104">De nombreuses applications C++ effacent le tampon de profondeur avant de restituer chaque nouveau Frame.</span><span class="sxs-lookup"><span data-stu-id="2816f-104">Many C++ applications clear the depth buffer before rendering each new frame.</span></span> <span data-ttu-id="2816f-105">Vous pouvez effacer explicitement la mémoire tampon de profondeur par le biais de Direct3D en appelant [**IDirect3DDevice9 :: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) et en spécifiant D3DCLEAR \_ ZBUFFER pour le paramètre flags.</span><span class="sxs-lookup"><span data-stu-id="2816f-105">You can explicitly clear the depth buffer through Direct3D by calling [**IDirect3DDevice9::Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) and specifying D3DCLEAR\_ZBUFFER for the Flags parameter.</span></span> <span data-ttu-id="2816f-106">La méthode **IDirect3DDevice9 :: Clear** vous permet de spécifier une valeur de profondeur arbitraire dans le paramètre Z.</span><span class="sxs-lookup"><span data-stu-id="2816f-106">The **IDirect3DDevice9::Clear** method allows you to specify an arbitrary depth value in the Z parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2816f-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2816f-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2816f-108">Mémoires tampons de profondeur</span><span class="sxs-lookup"><span data-stu-id="2816f-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
