---
description: L’interface ID3DXRenderToSurface est utilisée pour généraliser le processus de rendu des surfaces.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Interface ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323306"
---
# <a name="id3dxrendertosurface-interface"></a><span data-ttu-id="06f35-103">Interface ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="06f35-103">ID3DXRenderToSurface interface</span></span>

<span data-ttu-id="06f35-104">L’interface ID3DXRenderToSurface est utilisée pour généraliser le processus de rendu des surfaces.</span><span class="sxs-lookup"><span data-stu-id="06f35-104">The ID3DXRenderToSurface interface is used to generalize the process of rendering to surfaces.</span></span>

## <a name="members"></a><span data-ttu-id="06f35-105">Membres</span><span class="sxs-lookup"><span data-stu-id="06f35-105">Members</span></span>

<span data-ttu-id="06f35-106">L’interface **ID3DXRenderToSurface** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="06f35-106">The **ID3DXRenderToSurface** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="06f35-107">**ID3DXRenderToSurface** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="06f35-107">**ID3DXRenderToSurface** also has these types of members:</span></span>

-   [<span data-ttu-id="06f35-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="06f35-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="06f35-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="06f35-109">Methods</span></span>

<span data-ttu-id="06f35-110">L’interface **ID3DXRenderToSurface** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="06f35-110">The **ID3DXRenderToSurface** interface has these methods.</span></span>



| <span data-ttu-id="06f35-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="06f35-111">Method</span></span>                                                       | <span data-ttu-id="06f35-112">Description</span><span class="sxs-lookup"><span data-stu-id="06f35-112">Description</span></span>                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06f35-113">**BeginScene**</span><span class="sxs-lookup"><span data-stu-id="06f35-113">**BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)       | <span data-ttu-id="06f35-114">Commence une scène.</span><span class="sxs-lookup"><span data-stu-id="06f35-114">Begins a scene.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="06f35-115">**EndScene**</span><span class="sxs-lookup"><span data-stu-id="06f35-115">**EndScene**</span></span>](id3dxrendertosurface--endscene.md)           | <span data-ttu-id="06f35-116">Termine une scène.</span><span class="sxs-lookup"><span data-stu-id="06f35-116">Ends a scene.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="06f35-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="06f35-117">**GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)             | <span data-ttu-id="06f35-118">Récupère les paramètres de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="06f35-118">Retrieves the parameters of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="06f35-119">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="06f35-119">**GetDevice**</span></span>](id3dxrendertosurface--getdevice.md)         | <span data-ttu-id="06f35-120">Récupère le périphérique Direct3D associé à la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="06f35-120">Retrieves the Direct3D device associated with the render surface.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="06f35-121">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="06f35-121">**OnLostDevice**</span></span>](id3dxrendertosurface--onlostdevice.md)   | <span data-ttu-id="06f35-122">Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks.</span><span class="sxs-lookup"><span data-stu-id="06f35-122">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="06f35-123">Cette méthode doit être appelée chaque fois qu’un appareil est perdu ou avant de réinitialiser un appareil.</span><span class="sxs-lookup"><span data-stu-id="06f35-123">This method should be called whenever a device is lost or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="06f35-124">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="06f35-124">**OnResetDevice**</span></span>](id3dxrendertosurface--onresetdevice.md) | <span data-ttu-id="06f35-125">Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.</span><span class="sxs-lookup"><span data-stu-id="06f35-125">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="06f35-126">Notes</span><span class="sxs-lookup"><span data-stu-id="06f35-126">Remarks</span></span>

<span data-ttu-id="06f35-127">Les surfaces peuvent être utilisées de différentes façons, notamment les cibles de rendu, le rendu hors écran ou le rendu des textures.</span><span class="sxs-lookup"><span data-stu-id="06f35-127">Surfaces can be used in a variety of ways including render targets, off-screen rendering, or rendering to textures.</span></span>

<span data-ttu-id="06f35-128">Une surface peut être configurée à l’aide d’un Viewport distinct à l’aide de la méthode [**ID3DXRenderToSurface :: BeginScene**](id3dxrendertosurface--beginscene.md) pour fournir une vue Render personnalisée.</span><span class="sxs-lookup"><span data-stu-id="06f35-128">A surface can be configured using a separate viewport using the [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md) method, to provide a custom render view.</span></span> <span data-ttu-id="06f35-129">Si la surface n’est pas une cible de rendu, une cible de rendu compatible est utilisée et le résultat est copié vers la surface à la fin de la scène.</span><span class="sxs-lookup"><span data-stu-id="06f35-129">If the surface is not a render target, a compatible render target is used, and the result is copied to the surface at the end of the scene.</span></span>

<span data-ttu-id="06f35-130">L’interface **ID3DXRenderToSurface** est obtenue en appelant la fonction [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .</span><span class="sxs-lookup"><span data-stu-id="06f35-130">The **ID3DXRenderToSurface** interface is obtained by calling the [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) function.</span></span>

<span data-ttu-id="06f35-131">Le type LPD3DXRENDERTOSURFACE est défini comme un pointeur vers l’interface **ID3DXRenderToSurface** .</span><span class="sxs-lookup"><span data-stu-id="06f35-131">The LPD3DXRENDERTOSURFACE type is defined as a pointer to the **ID3DXRenderToSurface** interface.</span></span>


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a><span data-ttu-id="06f35-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06f35-132">Requirements</span></span>



| <span data-ttu-id="06f35-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06f35-133">Requirement</span></span> | <span data-ttu-id="06f35-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="06f35-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06f35-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="06f35-135">Header</span></span><br/>  | <dl> <span data-ttu-id="06f35-136"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="06f35-136"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="06f35-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06f35-137">Library</span></span><br/> | <dl> <span data-ttu-id="06f35-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06f35-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06f35-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06f35-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f35-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="06f35-140">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
