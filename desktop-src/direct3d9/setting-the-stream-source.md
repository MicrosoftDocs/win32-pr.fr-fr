---
description: 'La méthode IDirect3DDevice9 :: SetStreamSource lie une mémoire tampon de vertex à un flux de données de périphérique, en créant une association entre les données de vertex et l’un des nombreux ports de flux de données qui alimentent les fonctions de traitement Primitives.'
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Définition de la source de flux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521911"
---
# <a name="setting-the-stream-source-direct3d-9"></a><span data-ttu-id="12211-103">Définition de la source de flux (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="12211-103">Setting the Stream Source (Direct3D 9)</span></span>

<span data-ttu-id="12211-104">La méthode [**IDirect3DDevice9 :: SetStreamSource**](/windows/desktop/api) lie une mémoire tampon de vertex à un flux de données de périphérique, en créant une association entre les données de vertex et l’un des nombreux ports de flux de données qui alimentent les fonctions de traitement Primitives.</span><span class="sxs-lookup"><span data-stu-id="12211-104">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="12211-105">Les références réelles aux données de flux ne se produisent pas tant qu’une méthode de dessin, telle que [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), n’est pas appelée.</span><span class="sxs-lookup"><span data-stu-id="12211-105">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="12211-106">Un flux est défini comme un tableau uniforme de données de composants, où chaque composant se compose d’un ou de plusieurs éléments représentant une entité unique, par exemple position, normal, couleur, etc.</span><span class="sxs-lookup"><span data-stu-id="12211-106">A stream is defined as a uniform array of component data, where each component consists of one or more elements representing a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="12211-107">Le paramètre Stride spécifie la taille du composant, en octets.</span><span class="sxs-lookup"><span data-stu-id="12211-107">The Stride parameter specifies the size of the component, in bytes.</span></span>

<span data-ttu-id="12211-108">Le code suivant illustre la définition de la source de flux et le dessin de son contenu.</span><span class="sxs-lookup"><span data-stu-id="12211-108">The following code demonstrates setting the stream source and drawing its contents.</span></span> <span data-ttu-id="12211-109">La \_ variable g pVB est un LPDIRECT3DVERTEXBUFFER9 qui contient des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="12211-109">The g\_pVB variable is a LPDIRECT3DVERTEXBUFFER9 that contains vertex data.</span></span>


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



<span data-ttu-id="12211-110">Pour plus d’informations sur ce code, consultez le didacticiel suivant : [didacticiel 3 : utilisation de matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="12211-110">For more information about this code see the following tutorial: [Tutorial 3: Using Matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="12211-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12211-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12211-112">Rendu des primitives</span><span class="sxs-lookup"><span data-stu-id="12211-112">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
