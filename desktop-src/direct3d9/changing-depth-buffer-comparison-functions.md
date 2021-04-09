---
description: Par défaut, lorsque le test de profondeur est effectué sur une surface de rendu, le système Direct3D met à jour la surface de la cible de rendu si la valeur de profondeur correspondante (z ou w) pour chaque point est inférieure à la valeur de la mémoire tampon de profondeur.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Modification des fonctions de comparaison du tampon de profondeur (D3D9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749061"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a><span data-ttu-id="3dab0-103">Modification des fonctions de comparaison du tampon de profondeur (D3D9)</span><span class="sxs-lookup"><span data-stu-id="3dab0-103">Changing Depth Buffer Comparison Functions (D3D9)</span></span>

<span data-ttu-id="3dab0-104">Par défaut, lorsque le test de profondeur est effectué sur une surface de rendu, le système Direct3D met à jour la surface de la cible de rendu si la valeur de profondeur correspondante (z ou w) pour chaque point est inférieure à la valeur de la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="3dab0-104">By default, when depth-testing is performed on a rendering surface, the Direct3D system updates the render-target surface if the corresponding depth value (z or w) for each point is less than the value in the depth buffer.</span></span> <span data-ttu-id="3dab0-105">Dans une application C++, vous modifiez la manière dont le système effectue des comparaisons sur les valeurs de profondeur en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/desktop/api) avec le paramètre d' *État* défini sur D3DRS \_ ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="3dab0-105">In a C++ application, you change how the system performs comparisons on depth values by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method with the *State* parameter set to D3DRS\_ZFUNC.</span></span> <span data-ttu-id="3dab0-106">Le paramètre de *valeur* doit être défini sur une valeur dans le type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="3dab0-106">The *Value* parameter should be set to a value in the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dab0-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3dab0-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dab0-108">Mémoires tampons de profondeur</span><span class="sxs-lookup"><span data-stu-id="3dab0-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
