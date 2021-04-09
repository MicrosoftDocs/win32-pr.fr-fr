---
description: Une étape de fusion est un ensemble d’opérations de texture et leurs arguments qui définissent la façon dont les textures sont mélangées.
ms.assetid: 7f9e3041-a270-44a9-a8e1-bca5ea25a71e
title: Création de phases de fusion (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f5029d540433b22b1380435dd8092546917338
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110766"
---
# <a name="creating-blending-stages-direct3d-9"></a><span data-ttu-id="a7b53-103">Création de phases de fusion (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a7b53-103">Creating Blending Stages (Direct3D 9)</span></span>

<span data-ttu-id="a7b53-104">Une étape de fusion est un ensemble d’opérations de texture et leurs arguments qui définissent la façon dont les textures sont mélangées.</span><span class="sxs-lookup"><span data-stu-id="a7b53-104">A blending stage is a set of texture operations and their arguments that define how textures are blended.</span></span> <span data-ttu-id="a7b53-105">Lors d’une phase de fusion, les applications C++ appellent la méthode [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="a7b53-105">When making a blending stage, C++ applications invoke the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="a7b53-106">Le premier appel spécifie l’opération qui est effectuée.</span><span class="sxs-lookup"><span data-stu-id="a7b53-106">The first call specifies the operation that is performed.</span></span> <span data-ttu-id="a7b53-107">Deux appels supplémentaires définissent les arguments auxquels l’opération est appliquée.</span><span class="sxs-lookup"><span data-stu-id="a7b53-107">Two additional invocations define the arguments to which the operation is applied.</span></span> <span data-ttu-id="a7b53-108">L’exemple de code suivant illustre la création d’une étape de fusion.</span><span class="sxs-lookup"><span data-stu-id="a7b53-108">The following code example illustrates the creation of a blending stage.</span></span>


```
// This example assumes that lpD3DDev is a valid pointer to an
// IDirect3DDevice9 interface.

// Set the operation for the first texture.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_ADD);

// Set argument 1 to the texture color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE);

// Set argument 2 to the iterated diffuse color.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE);
```



<span data-ttu-id="a7b53-109">Les données de Texel dans les textures contiennent des valeurs de couleur et alpha.</span><span class="sxs-lookup"><span data-stu-id="a7b53-109">Texel data in textures contain color and alpha values.</span></span> <span data-ttu-id="a7b53-110">Les applications peuvent définir des opérations distinctes pour les valeurs de couleur et alpha dans une phase de fusion unique.</span><span class="sxs-lookup"><span data-stu-id="a7b53-110">Applications can define separate operations for both color and alpha values in a single blending stage.</span></span> <span data-ttu-id="a7b53-111">Chaque opération, couleur et alpha possède ses propres arguments.</span><span class="sxs-lookup"><span data-stu-id="a7b53-111">Each operation, color, and alpha, has its own arguments.</span></span> <span data-ttu-id="a7b53-112">Pour plus d’informations, consultez [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="a7b53-112">For details, see [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

<span data-ttu-id="a7b53-113">Bien qu’il ne fasse pas partie de l’API Direct3D, vous pouvez insérer les macros suivantes dans votre application pour abréger le code requis pour créer des étapes de fusion de texture.</span><span class="sxs-lookup"><span data-stu-id="a7b53-113">Although not part of the Direct3D API, you can insert the following macros into your application to abbreviate the code required for creating texture blending stages.</span></span>


```
#define SetTextureColorStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_COLOROP, op);      \
    dev->SetTextureStageState( i, D3DTSS_COLORARG1, arg1 ); \
    dev->SetTextureStageState( i, D3DTSS_COLORARG2, arg2 );

#define SetTextureAlphaStage( dev, i, arg1, op, arg2 )     \
    dev->SetTextureStageState( i, D3DTSS_ALPHAOP, op);      \
    dev->SetTextureStageState( i, D3DTSS_ALPHAARG1, arg1 );  \
    dev->SetTextureStageState( i  D3DTSS_ALPHAARG2, arg2 );
```



## <a name="related-topics"></a><span data-ttu-id="a7b53-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7b53-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7b53-115">Fusion de texture</span><span class="sxs-lookup"><span data-stu-id="a7b53-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
