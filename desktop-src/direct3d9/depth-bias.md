---
description: Les polygones qui sont coplanés dans votre espace 3D peuvent apparaître comme s’ils n’étaient pas coplanés en ajoutant un biais z à chacun d’eux.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Décalage de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481561"
---
# <a name="depth-bias-direct3d-9"></a><span data-ttu-id="57766-103">Décalage de profondeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="57766-103">Depth Bias (Direct3D 9)</span></span>

<span data-ttu-id="57766-104">Les polygones qui sont coplanés dans votre espace 3D peuvent apparaître comme s’ils n’étaient pas coplanés en ajoutant un biais z à chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="57766-104">Polygons that are coplanar in your 3D space can be made to appear as if they are not coplanar by adding a z-bias to each one.</span></span> <span data-ttu-id="57766-105">Il s’agit d’une technique couramment utilisée pour s’assurer que les ombres d’une scène s’affichent correctement.</span><span class="sxs-lookup"><span data-stu-id="57766-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="57766-106">Par exemple, une ombre sur un mur aura probablement la même valeur de profondeur que le mur.</span><span class="sxs-lookup"><span data-stu-id="57766-106">For instance, a shadow on a wall will likely have the same depth value as the wall does.</span></span> <span data-ttu-id="57766-107">Si vous affichez le mur en premier, puis l’ombre, l’ombre peut ne pas être visible ou les artefacts de profondeur peuvent être visibles.</span><span class="sxs-lookup"><span data-stu-id="57766-107">If you render the wall first and then the shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span> <span data-ttu-id="57766-108">Vous pouvez inverser l’ordre dans lequel vous effectuez le rendu des objets coplanaires dans l’espoir d’inverser l’effet, mais les artefacts de profondeur sont toujours susceptibles de se produire.</span><span class="sxs-lookup"><span data-stu-id="57766-108">You can reverse the order in which you render the coplanar objects in hopes of reversing the effect, but depth artifacts are still likely.</span></span>

<span data-ttu-id="57766-109">Une application peut aider à s’assurer que les polygones sont rendus correctement en ajoutant un décalage aux valeurs z que le système utilise lors du rendu des jeux de polygones coplanaires.</span><span class="sxs-lookup"><span data-stu-id="57766-109">An application can help ensure that coplanar polygons are rendered properly by adding a bias to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="57766-110">Pour ajouter un biais z à un ensemble de polygones, appelez la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) juste avant de les afficher, en définissant le paramètre d' *État* sur D3DRS \_ DEPTHBIAS et le paramètre *value* sur une valeur float appropriée (par exemple, une valeur appropriée peut être comprise entre-1,0 et 1,0) ; pour transmettre cette valeur à **SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="57766-110">To add a z-bias to a set of polygons, call the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method just before rendering them, setting the *State* parameter to D3DRS\_DEPTHBIAS, and the *Value* parameter to a suitable float value (for example, a suitable value might be from -1.0 to 1.0); to pass this value to **SetRenderState**, you must also cast the value to a **DWORD**.</span></span> <span data-ttu-id="57766-111">Une valeur de décalage z supérieure augmente la probabilité que les polygones que vous affichez s’affichent avec d’autres polygones coplanaires.</span><span class="sxs-lookup"><span data-stu-id="57766-111">A higher z-bias value increases the likelihood that the polygons you render will be visible when displayed with other coplanar polygons.</span></span>


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



<span data-ttu-id="57766-112">où m est la pente de profondeur maximale du triangle rendu.</span><span class="sxs-lookup"><span data-stu-id="57766-112">where m is the maximum depth slope of the triangle being rendered.</span></span>


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



<span data-ttu-id="57766-113">Les unités pour les \_ États de rendu D3DRS DEPTHBIAS et D3DRS \_ SLOPESCALEDEPTHBIAS varient selon que la mise en mémoire tampon z ou w est activée.</span><span class="sxs-lookup"><span data-stu-id="57766-113">The units for the D3DRS\_DEPTHBIAS and D3DRS\_SLOPESCALEDEPTHBIAS render states depend on whether z-buffering or w-buffering is enabled.</span></span> <span data-ttu-id="57766-114">L’application doit fournir des valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="57766-114">The application must provide suitable values.</span></span>

<span data-ttu-id="57766-115">Le biais n’est appliqué à aucune ligne et primitives de point.</span><span class="sxs-lookup"><span data-stu-id="57766-115">The bias is not applied to any line and point primitive.</span></span> <span data-ttu-id="57766-116">Toutefois, cette valeur doit être appliquée aux triangles dessinés en mode filaire.</span><span class="sxs-lookup"><span data-stu-id="57766-116">However, this bias needs to be applied to triangles drawn in wireframe mode.</span></span>


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a><span data-ttu-id="57766-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57766-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57766-118">Pipeline de pixels</span><span class="sxs-lookup"><span data-stu-id="57766-118">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
