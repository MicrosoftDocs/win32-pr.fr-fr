---
description: Pour déterminer si Direct3D prend en charge l’interpolation de vertex, recherchez l' \_ indicateur d’interpolation D3DVTXPCAPS dans le membre VertexProcessingCaps de la structure D3DCAPS9.
ms.assetid: b60c7f96-3752-4703-9059-486d9906c508
title: Utilisation de l’interpolation de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ca56cc521b5bff01a5d6af5c2d4ab6b02cd49e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846166"
---
# <a name="using-vertex-tweening-direct3d-9"></a><span data-ttu-id="1e8dd-103">Utilisation de l’interpolation de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1e8dd-103">Using Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="1e8dd-104">Pour déterminer si Direct3D prend en charge l’interpolation de vertex, recherchez l' \_ indicateur d’interpolation D3DVTXPCAPS dans le membre VertexProcessingCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="1e8dd-104">To determine if Direct3D supports vertex tweening, check for the D3DVTXPCAPS\_TWEENING flag in the VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="1e8dd-105">L’exemple de code suivant utilise la méthode [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) pour déterminer si l’interpolation est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1e8dd-105">The following code example uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to determine if tweening is supported.</span></span>


```
// This example assumes that m_pD3DDevice is 
// a valid pointer to a IDirect3DDevice9 interface.
//
D3DCAPS9 d3dCaps;

m_pD3DDevice->GetDeviceCaps( &d3dCaps );
if( 0 != (d3dCaps.VertexProcessingCaps & D3DVTXPCAPS_TWEENING) )
    // Vertex tweening is supported.
```



<span data-ttu-id="1e8dd-106">Pour utiliser l’interpolation vectorielle, vous devez d’abord configurer un type vertex personnalisé qui utilise une deuxième position normale ou de seconde.</span><span class="sxs-lookup"><span data-stu-id="1e8dd-106">To use vector tweening, you must first set up a custom vertex type that uses a second normal or a second position.</span></span> <span data-ttu-id="1e8dd-107">L’exemple de code suivant montre un exemple de déclaration qui comprend à la fois un deuxième point et une deuxième position.</span><span class="sxs-lookup"><span data-stu-id="1e8dd-107">The following code example shows a sample declaration that includes both a second point and a second position.</span></span>


```
struct TEX_VERTEX
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DVECTOR position2;
    D3DVECTOR normal2;
};

//Create a vertex buffer with the type TEX_VERTEX.
```



<span data-ttu-id="1e8dd-108">L’étape suivante consiste à définir la déclaration actuelle.</span><span class="sxs-lookup"><span data-stu-id="1e8dd-108">The next step is to set the current declaration.</span></span> <span data-ttu-id="1e8dd-109">L’exemple de code ci-dessous montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="1e8dd-109">The code example below shows how to do this.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    { 0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 1 },
    { 0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 1 },
    D3DDECL_END()
};
```



<span data-ttu-id="1e8dd-110">Pour plus d’informations sur la création d’un type de vertex personnalisé et d’une mémoire tampon de vertex, consultez [création d’une mémoire tampon de vertex (Direct3D 9)](creating-a-vertex-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="1e8dd-110">For more information about creating a custom vertex type and a vertex buffer, see [Creating a Vertex Buffer (Direct3D 9)](creating-a-vertex-buffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="1e8dd-111">Lorsque l’interpolation de vertex est activée, une deuxième position ou une deuxième normale doit être présente dans la déclaration actuelle.</span><span class="sxs-lookup"><span data-stu-id="1e8dd-111">When vertex tweening is enabled, a second position or a second normal must be present in the current declaration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1e8dd-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e8dd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e8dd-113">Interpolation de vertex</span><span class="sxs-lookup"><span data-stu-id="1e8dd-113">Vertex Tweening</span></span>](vertex-tweening.md)
</dt> </dl>

 

 
