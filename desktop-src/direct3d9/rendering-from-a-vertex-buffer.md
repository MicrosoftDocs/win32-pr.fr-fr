---
description: 'Le rendu des données de vertex à partir d’une mémoire tampon de vertex requiert quelques étapes. Tout d’abord, vous devez définir la source du flux en appelant la méthode IDirect3DDevice9 :: SetStreamSource, comme indiqué dans l’exemple suivant.'
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Rendu à partir d’une mémoire tampon de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108454"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="7ba7f-104">Rendu à partir d’une mémoire tampon de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7ba7f-104">Rendering from a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="7ba7f-105">Le rendu des données de vertex à partir d’une mémoire tampon de vertex requiert quelques étapes.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-105">Rendering vertex data from a vertex buffer requires a few steps.</span></span> <span data-ttu-id="7ba7f-106">Tout d’abord, vous devez définir la source du flux en appelant la méthode [**IDirect3DDevice9 :: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-106">First, you need to set the stream source by calling the [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) method, as shown in the following example.</span></span>


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



<span data-ttu-id="7ba7f-107">Le premier paramètre de [**IDirect3DDevice9 :: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) indique à Direct3D la source du flux de données de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-107">The first parameter of [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) tells Direct3D the source of the device data stream.</span></span> <span data-ttu-id="7ba7f-108">Le deuxième paramètre est la mémoire tampon de vertex à lier au flux de données.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-108">The second parameter is the vertex buffer to bind to the data stream.</span></span> <span data-ttu-id="7ba7f-109">Le troisième paramètre est le décalage entre le début du flux et le début des données du vertex, en octets.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-109">The third parameter is the offset from the beginning of the stream to the beginning of the vertex data, in bytes.</span></span> <span data-ttu-id="7ba7f-110">Le quatrième paramètre correspond au Stride du composant, en octets.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-110">The fourth parameter is the stride of the component, in bytes.</span></span> <span data-ttu-id="7ba7f-111">Dans l’exemple de code ci-dessus, la taille d’un CUSTOMVERTEX est utilisée pour le Stride du composant.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-111">In the sample code above, the size of a CUSTOMVERTEX is used for the stride of the component.</span></span>

<span data-ttu-id="7ba7f-112">L’étape suivante consiste à informer Direct3D du nuanceur de sommets à utiliser en appelant la méthode [**IDirect3DDevice9 :: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .</span><span class="sxs-lookup"><span data-stu-id="7ba7f-112">The next step is to inform Direct3D which vertex shader to use by calling the [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) method.</span></span> <span data-ttu-id="7ba7f-113">L’exemple de code suivant définit un code de Commission sur le prix final pour le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-113">The following sample code sets an FVF code for the vertex shader.</span></span> <span data-ttu-id="7ba7f-114">Cela informe Direct3D des types de vertex qu’il traite.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-114">This informs Direct3D of the types of vertices it is dealing with.</span></span>


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



<span data-ttu-id="7ba7f-115">Après la définition de la source de flux et du nuanceur de sommets, toute méthode de dessin utilisera la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-115">After setting the stream source and vertex shader, any draw methods will use the vertex buffer.</span></span> <span data-ttu-id="7ba7f-116">L’exemple de code ci-dessous montre comment restituer des vertex à partir d’une mémoire tampon de vertex avec la méthode [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="7ba7f-116">The code example below shows how to render vertices from a vertex buffer with the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method.</span></span>


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



<span data-ttu-id="7ba7f-117">Le deuxième paramètre que [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepte est l’index du premier vecteur dans la mémoire tampon de vertex à charger.</span><span class="sxs-lookup"><span data-stu-id="7ba7f-117">The second parameter that [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepts is the index of the first vector in the vertex buffer to load.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ba7f-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ba7f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ba7f-119">Mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="7ba7f-119">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> <dt>

[<span data-ttu-id="7ba7f-120">Rendu à partir de mémoires tampons de vertex et d’index (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7ba7f-120">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
