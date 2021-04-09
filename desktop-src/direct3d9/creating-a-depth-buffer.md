---
description: Une mémoire tampon de profondeur est une propriété de l’appareil. Pour créer un tampon de profondeur géré par Direct3D, définissez les membres appropriés de la structure de \_ paramètres D3DPRESENT comme indiqué dans l’exemple de code suivant.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Création d’un tampon de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110274"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a><span data-ttu-id="4f4a0-104">Création d’un tampon de profondeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4f4a0-104">Creating a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="4f4a0-105">Une mémoire tampon de profondeur est une propriété de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4f4a0-105">A depth buffer is a property of the device.</span></span> <span data-ttu-id="4f4a0-106">Pour créer un tampon de profondeur géré par Direct3D, définissez les membres appropriés de la structure [**de \_ paramètres D3DPRESENT**](d3dpresent-parameters.md) comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="4f4a0-106">To create a depth buffer that is managed by Direct3D, set the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure as shown in the following code example.</span></span>


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



<span data-ttu-id="4f4a0-107">En affectant la **valeur true** au membre EnableAutoDepthStencil, vous indiquez à Direct3D de gérer les mémoires tampons de profondeur pour l’application.</span><span class="sxs-lookup"><span data-stu-id="4f4a0-107">By setting the EnableAutoDepthStencil member to **TRUE**, you instruct Direct3D to manage depth buffers for the application.</span></span> <span data-ttu-id="4f4a0-108">Notez que AutoDepthStencilFormat doit être défini sur un format de mémoire tampon de profondeur valide.</span><span class="sxs-lookup"><span data-stu-id="4f4a0-108">Note that AutoDepthStencilFormat must be set to a valid depth buffer format.</span></span> <span data-ttu-id="4f4a0-109">L' \_ indicateur D3DFMT D16 spécifie une mémoire tampon de profondeur de 16 bits, si celle-ci est disponible.</span><span class="sxs-lookup"><span data-stu-id="4f4a0-109">The D3DFMT\_D16 flag specifies a 16-bit depth buffer, if one is available.</span></span>

<span data-ttu-id="4f4a0-110">L’appel suivant à la méthode [**IDirect3D9 :: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crée un appareil qui crée ensuite une mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="4f4a0-110">The following call to the [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) method creates a device that then creates a depth buffer.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



<span data-ttu-id="4f4a0-111">La mémoire tampon de profondeur est définie automatiquement en tant que cible de rendu de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4f4a0-111">The depth buffer is automatically set as the render target of the device.</span></span> <span data-ttu-id="4f4a0-112">Lorsque l’appareil est réinitialisé, le tampon de profondeur est automatiquement détruit et recréé dans la nouvelle taille.</span><span class="sxs-lookup"><span data-stu-id="4f4a0-112">When the device is reset, the depth buffer is automatically destroyed and re-created in the new size.</span></span>

<span data-ttu-id="4f4a0-113">Pour créer une surface de mémoire tampon de profondeur, utilisez la méthode [**IDirect3DDevice9 :: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="4f4a0-113">To create a new depth buffer surface, use the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) method.</span></span>

<span data-ttu-id="4f4a0-114">Pour définir une nouvelle surface de mémoire tampon de profondeur pour l’appareil, utilisez la méthode [**IDirect3DDevice9 :: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .</span><span class="sxs-lookup"><span data-stu-id="4f4a0-114">To set a new depth-buffer surface for the device, use the [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) method.</span></span>

<span data-ttu-id="4f4a0-115">Pour utiliser la mémoire tampon de profondeur dans votre application, vous devez activer la mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="4f4a0-115">To use the depth buffer in your application, you need to enable the depth buffer.</span></span> <span data-ttu-id="4f4a0-116">Pour plus d’informations, consultez Activation de la [mise en mémoire tampon de profondeur (Direct3D 9)](enabling-depth-buffering.md).</span><span class="sxs-lookup"><span data-stu-id="4f4a0-116">For details, see [Enabling Depth Buffering (Direct3D 9)](enabling-depth-buffering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f4a0-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f4a0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f4a0-118">Mémoires tampons de profondeur</span><span class="sxs-lookup"><span data-stu-id="4f4a0-118">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
