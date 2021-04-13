---
description: Direct3D gère une liste de huit textures actuelles. Elle fusionne ces textures sur l’ensemble de la primitive qu’elle rend. Seules les textures créées en tant que pointeurs d’interface de texture peuvent être utilisées dans l’ensemble des textures actuelles.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Affectation des textures actuelles (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483984"
---
# <a name="assigning-the-current-textures-direct3d-9"></a><span data-ttu-id="bb15e-105">Affectation des textures actuelles (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bb15e-105">Assigning the Current Textures (Direct3D 9)</span></span>

<span data-ttu-id="bb15e-106">Direct3D gère une liste de huit textures actuelles.</span><span class="sxs-lookup"><span data-stu-id="bb15e-106">Direct3D maintains a list of up to eight current textures.</span></span> <span data-ttu-id="bb15e-107">Elle fusionne ces textures sur l’ensemble de la primitive qu’elle rend.</span><span class="sxs-lookup"><span data-stu-id="bb15e-107">It blends these textures onto all the primitive it renders.</span></span> <span data-ttu-id="bb15e-108">Seules les textures créées en tant que pointeurs d’interface de texture peuvent être utilisées dans l’ensemble des textures actuelles.</span><span class="sxs-lookup"><span data-stu-id="bb15e-108">Only textures created as texture interface pointers can be used in the set of current textures.</span></span>

<span data-ttu-id="bb15e-109">Les applications appellent la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) pour assigner des textures à l’ensemble des textures actuelles.</span><span class="sxs-lookup"><span data-stu-id="bb15e-109">Applications call the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method to assign textures into the set of current textures.</span></span> <span data-ttu-id="bb15e-110">Le premier paramètre doit être un nombre compris entre 0-7 inclus.</span><span class="sxs-lookup"><span data-stu-id="bb15e-110">The first parameter must be a number in the range of 0-7, inclusive.</span></span> <span data-ttu-id="bb15e-111">Transmettez le pointeur d’interface de texture comme deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="bb15e-111">Pass the texture interface pointer as the second parameter.</span></span>

<span data-ttu-id="bb15e-112">L’exemple de code C++ suivant montre comment une texture peut être assignée à l’ensemble des textures actuelles.</span><span class="sxs-lookup"><span data-stu-id="bb15e-112">The following C++ code example demonstrates how a texture can be assigned to the set of current textures.</span></span>


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> <span data-ttu-id="bb15e-113">Les périphériques logiciels ne prennent pas en charge l’affectation d’une texture à plusieurs étapes de texture à la fois.</span><span class="sxs-lookup"><span data-stu-id="bb15e-113">Software devices do not support assigning a texture to more than one texture stage at a time.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bb15e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bb15e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb15e-115">Fusion de texture</span><span class="sxs-lookup"><span data-stu-id="bb15e-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
