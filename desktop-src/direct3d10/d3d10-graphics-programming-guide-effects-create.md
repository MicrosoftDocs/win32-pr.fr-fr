---
description: Un effet est créé en le chargeant dans le Framework Effects.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Créer un effet (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514107"
---
# <a name="create-an-effect-direct3d-10"></a><span data-ttu-id="2be87-103">Créer un effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="2be87-103">Create an Effect (Direct3D 10)</span></span>

<span data-ttu-id="2be87-104">Un effet est créé en le chargeant dans le Framework Effects.</span><span class="sxs-lookup"><span data-stu-id="2be87-104">An effect is created by loading it into the effects framework.</span></span> <span data-ttu-id="2be87-105">Si l’effet n’a jamais été compilé, il sera compilé lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="2be87-105">If the effect has never been compiled, it will be compiled when it is created.</span></span> <span data-ttu-id="2be87-106">Les effets déjà chargés en mémoire peuvent être créés en appelant [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md).</span><span class="sxs-lookup"><span data-stu-id="2be87-106">Effects that are already loaded into memory can be created by calling [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md).</span></span> <span data-ttu-id="2be87-107">L’exemple de code suivant utilise [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) pour créer un effet à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="2be87-107">The following code example uses [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) to create an effect from a file.</span></span>


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



<span data-ttu-id="2be87-108">La lecture d’un effet requiert les mêmes paramètres que la compilation d’un effet, ainsi qu’un appareil et un pool.</span><span class="sxs-lookup"><span data-stu-id="2be87-108">Reading an effect requires the same parameters as compiling an effect, plus a device and a pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2be87-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2be87-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2be87-110">Rendu d’un effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="2be87-110">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



